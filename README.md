# git-training

Git and github in detail.

## Basics of Git

For Git to work properly, we need to let it know who we are so that it can link a local Git user (you) to GitHub. When working on a team, this allows people to see what you have committed and who committed each line of code.

The commands below will configure Git. Be sure to enter your own information inside the quotes (but include the quotation marks)!

```bash
git config --global user.name "Your Name"
git config --global user.email "yourname@example.com"
git add .
git commit -m "Added index.html"
git push origin main
```

#### Creating a repo

Created a repo named git-training and added a file index.html using following commands.
![](https://imgur.com/cTErh36.png)

This is how it is seen on github after adding the file
![](https://imgur.com/9EUqDQP.png)

Created four branches main, dev, alpha and beta:
![](https://imgur.com/5DPjz0Z.png)
And after creating this four branches, we need to push this branches on github using :

```bash
git push -u origin dev
git push -u origin alpha
git push -u origin beta
```

#### Visualizing branches

![](https://imgur.com/gGgnF2o.png)
