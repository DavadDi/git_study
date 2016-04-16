# git_study

1. Create a new repository on the command line
-----------------------------------------------

###
    $echo "# git_study" >> README.md
    $git init
    $git config user.email "dwh0403@163.com"
    $git config user.name "DavadDi"
    $git add README.md
    $git commit -m "first commit"
    $git remote add origin https://github.com/DavadDi/git_study.git
    $git push -u origin master

2. Push an existing repository from the command line
------------------------------------------------------

###
    $set user.name and email
    $git remote add origin https://github.com/DavadDi/git_study.git
    $git push -u origin master
