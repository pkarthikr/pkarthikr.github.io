+++
title = "Deploying With Deploybot"
date = "2016-12-05T10:09:40-08:00"

#
# description is optional
#
# description = "An optional description for SEO. If not provided, an automatically created summary will be used."

tags = ["coding"]
+++

I vividly remember the first time, I messed up a production server. It was my early days of being a programmer, and we had got our first client.

Back then, my deployment strategy was basically to upload files using FTP and then run any commands on the server via the shell. During a routine deployment, I noticed a file which remained in the server, and in trying to remove it, I typed `sudo rm -rf /`.

On the Production.

I watched the next few minutes in horror as the entire client’s machine was wiped clean and the site went down. Fortunately, my client was understanding, and we had backups - so there was not much of damage - but I had to spend the next 3 days fixing the mess (and contemplating if I am really cut out for this job.)

My biggest learning from the incident was to be very careful when on Production. Over the time, I learned Git and other tools, which made deployments more easier and safer. As someone developing in Laravel, and leading a team of Laravel developers - I am always on the look out to make deployments easier.

And I have tried everything from custom bash scripts to git workflows, where we would git pull on server. None of them however stuck primarily due to the complexities they bought in

And after much experimentation - my team and I zeroed down to [DeployBot](https://deploybot.com/).

DeployBot allows you to deploy code from anywhere. It takes your code from your Github / Bitbucket or self hosted Git repositories and deploys to any server. At QICE, we primarily use Digital Ocean and AWS - both of which are supported by DeployBot and make it an ease to integrate in our projects.

Here’s how DeployBot has helped us

**Continuous Deployment**

Over the day, we make 2-3 deployments to our sandboxes on certain projects. And these are fairly large commits. DeployBot seamlessly gets the new commits and automatically ( or manual for production setups ) deploys the latest files to the server.

My team now does not have to worry about deploying to server. All we have to do is push to a branch, and we know it will end up being on the server.

**Rollbacks**

Despite much preparation, there are moments, when things don’t work on the production for weird reasons. Deploybot has a rollback to a specific version feature, which is quite nifty at times like these.

**Pre and Post Deployment Commands**

After deployment, we run a few commands ex : Gulp, Migrations and Composer updates.

Deploybot allows us to specify what commands to run before and after deployment. That means, more developer peace and not worrying about switching to server and typing in each command on production machines.

**Modifying Configuration Files**

Even after all this, you may have to sometimes go to the server to edit your configuration files.

Deploybot eliminates this as well, by asking you to enter your configuration files. Just ensure all the changes are in your configuration file before you deploy, and they are deployed in your next deployment.

**Notifications**

Pretty much every web app these days has Slack / Email integration - and so does Deploybot. It notifies us everytime there is a deployment in our Slack channels.

No more informing the entire team that the production is done and they can resume their work.

**Amazing Support & Reliability**

This is something of importance to us. In the past one year, that we used Deploybot, we faced a downtime of exactly 1 minute, where we couldn’t deploy to production. We reached out to Support and got a reply back within the next minute telling us that the issue has been fixed.

Thanks to Deploybot, my team and I can now focus on building stuff than worrying about getting it to our customers. If you are into developing web apps, it is an invaluable part of your toolset and takes care of all your deployment worries.