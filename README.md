# Project Resources

Why?   
Many people need resources to educate and guide them on planning/deployment/collaboration.  

**Simply put, everything about coding that isn't writing code.**

What?  
This will be a document with step by step guides that will help you get your project done.  

### Hosting a full stack application.


### Using a linter to enforce consistent style.

Use a linter. This is a tool which enforces a style around your code. It doesn't matter if 1 or 30 people are working on your project, a consistent style is a good way to stay sane. **No way is 'right'.**    
If you are just starting, use standard JS guide. If you want to go further, make a decision about what is best to solve the problem at hand.  

Here's how to get started.
```bash
npm i -g eslint
eslint --init
> choose a popular style guide
> standard
> javascript
```

How is it used? The best way is to have linting in your own editor.  

How to use linting in atom with packages.  
1. install 'linter'   
2. install 'linter-eslint'  

If you are unable to do this, run eslint in the command line.  
[eslint](http://eslint.org/)

### Simple git commands.  
**examples**  
```bash
# project startup
git init
git remote add origin https://github.com/Chingu-cohorts/project-resources.git  

# new branch
git checkout -b develop
git branch

# committing
git add .
git commit -m 'hello world'
git push origin master

# oh shit
git reset HEAD~
```
