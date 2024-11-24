+++
title = "When Curl Fails"
date = "2017-01-25T10:17:13-08:00"

#
# description is optional
#
# description = "An optional description for SEO. If not provided, an automatically created summary will be used."

tags = ["coding",]
+++

Every once in a while, as a programmer, you seemingly come upon a problem that flummoxes you, irritates you and takes you through a wide array of emotions - and in the end when you solve it, makes you look back and think, why did this issue even take so much time to fix.

Here’s one from my diaries: I was working for a client which dealt with lots of financial data, building an app which dealt with peer to peer wallet system and phone recharges. The app’s backend API was built using a custom PHP framework.

After having built the system, I went to my client’s office to deploy the system on their homegrown servers. One thing that I should mention is, being a company that handles lot of financial data - the entire campus was very secure. Regular audits, Access only to authorised personnel. But what struck me odd was that even the computers were not connected to Internet - A team of 20 programmers shared two computers that connected to Internet, which they used when they wanted to research the issues they were working on.

Having given a machine, I installed PHP on the servers and deployed my app - so I can start testing. This is where all the troubles started for me. For one of the methods, I had written some code to call client’s API to recharge their phone - but just no matter what happened, the API wouldn’t work.

Looking at the code, the code was written in a simple CURL snippet

    // create a new cURL resource$ch = curl_init();
    $ch = curl_init();
    // set URL and other appropriate options
    curl_setopt($ch, CURLOPT_URL, "http://www.example.com/");
    curl_setopt($ch, CURLOPT_HEADER, 0);
    // grab URL and execute it
    curl_exec($ch);
    // close cURL resource, and free up system resources
    curl_close($ch);
    

But now here’s the funny part - the same URL was accessible via the browser, postman clients and everywhere. But through the code, it would simply refuse to work.

After looking into the logs - and learning more about CURL and how it works - I added the curl\_error function to see what is failing this bit of code.

**Error 7 - Bad request. Could not connect to host.**

Ah. So now we were getting somewhere. But there could be multiple reasons why we could not connect to the host - network dropping out, Internet not accessible and so on.

That’s when it hit me like a flash of light - The entire computers at the client’s office were passing through a proxy. Now the URLs worked perfectly because the browsers were configured. I opened a terminal and typed

**curl -v www.google.com**

And truly enough - I got Error 7 again now. With a bit of more research - I was able to get it working. Adding these two lines to my code with the correct credentials got the code working.

    curl_setopt($ch, CURLOPT_PROXY, "proxyurl:proxyport");
    curl_setopt($ch, CURLOPT_PROXYUSERPWD, "username:password");
    

And I ended my 12 hours of debugging this issue - being the more wiser about proxies and a deep understanding of CURL.
