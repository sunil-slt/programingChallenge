
# Implement Algorithum

## Problem Statement
We need a middle ware which enable us to rate limit the api call per minute.

1. Consider we have bucket for each API and IP of caller. (Ex. Bucket Name: user:127.0.0.1 )
2. If user calling API for first time, then init new bucket for that API and IP address combination. New Bucket will have default coins required for per api call.
2. Coins required per api call will be added to bucket every second. bucketCoins = bucketCoins + perAPICoins;
3. Max bucketCoins allowed is (60 * perAPICoins)/numberCallAllowedPerMinute
4. On Each API call we will check for number of available coins in bucket, if bucket have sufficient coins then allow api call and deduct coins from bucket for that api call, else throw limit exide error (give respone)


## Acceptance Criteria
1. Working Code 
2. Test cases written for a single API (/user) (Optional, best to have)
3. For solution submition do not fork this repository.
4. Create your repo, remove .git folder from root folder of this project.
5. Init fresh github and add your repo's remote url and push changes in your repository.
6. Share your repository URL

## Evolutions Points
1. Working code - 5
2. Coding Standard - 5