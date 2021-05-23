---
title: "Install Npm Node Linux Quick"
date: 2021-05-23T19:56:57+05:30
draft: false
---

I recently wanted to use node on my linux pc. It's running ubunutu 20.04.01.
Once again, I had issues installing it from the official repo. While node installed smoothly, I had no NPM. Plus, it installed some super old archic version of node.
To say the least, I wasn't happy.
I spent the next 30 minutes looking for and vetting the best solution. And I am glad to say that I did!
I am writing this post so that you dont have to go through the same.

This method lets you install node AND npm just 2 easy-peasey steps.

## Step 1
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.37.2/install.sh | bash
```
Now, close your terminal and open a new one. This, to get it ready for the next step.


## Step 2
Before you run the next command, be sure to check what is the latest version of node.
You can do so [here](https://nodejs.org/en/): https://nodejs.org/en/
Be sure to replace the `v14.17.0` with whatever the latest version is for you.
At the time of writing this post, it is `v14.17.0`

```bash
 nvm install v14.17.0
 ```

## Conclusion
And that's all folks!
Courtesy to [nelsonic](https://stackoverflow.com/questions/10075990/upgrading-node-js-to-latest-version) for providing this as a stackoverlow answer
On wait there's one more step!



## Step 3-ish
[Disco time!](https://www.youtube.com/watch?v=6QCMGKUH6Ak)
{{< youtube 6QCMGKUH6Ak >}}

