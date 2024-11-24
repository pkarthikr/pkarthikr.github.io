+++
title = "Regexp With Mysql"
date = "2016-12-21T10:14:04-08:00"

#
# description is optional
#
# description = "An optional description for SEO. If not provided, an automatically created summary will be used."

tags = ["coding",]
+++

In one of the recent projects that I have been working on, I had to look for a word in a phrase - but the challenge was to rank an occurrence of the phrase higher when it’s an individual word as compared to when it was part of a word.

For ex : Food Blogger should rate higher than Ardent Foodie, because in the first example - Food is an individual word as compared to latter where it is part of a whole word.

At times like this, I find MySQL’s [REGEXP](https://dev.mysql.com/doc/refman/5.7/en/regexp.html) quite useful, as I can use different regular expressions to fit my criteria. So here’s what I did here

I first looked for an individual occurrence of a word.

`select * from table_name where search_term REGEXP '[[:<:]]food[[:>:]]';`

Here, \[\[:<:\]\] & \[\[:>:\]\] are markers that stand for word boundaries. They match the beginning and end of words, respectively. Now, as a next step, I follow it by this query.

`select * from table_name where search_term LIKE '%food%';`

But when the first case happens, it gets an higher priority as compared to the second case - so I reworked the query to this

    select table_name.title, (case when search_term REGEXP '[[:<:]]food[[:>:]]'  
    then 100 when search_term LIKE '%food%' then 99 else 1 end) as priority  
    from table_name order by `priority` desc;  
    

That way, results that have the word as a standalone rank higher up as compared to when they are part of a phrase.
