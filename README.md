# Project Resources

Why?   
Many people need resources to educate and guide them on planning/deployment/collaboration.  

**Simply put, a guide for everything about coding that isn't writing code.**

What?  
This will be a document with step by step guides that will help you get your project done.  

### Project structure.  
[Damn good template](https://github.com/Madmous/Trello-Clone)  
1. mkdir projectname
2. cd projectname  
3. create-react-app client  
4. mkdir server  

### Hosting a full stack application.
The best/cheapest way to professionally host your application is going to be on amazon web services (aws).  
Amazon web services can be intimidating compared to heroku, we will create a simple setup here that will make it easy using continuous deployment with travis CI.  

[aws](https://www.amazon.com/ap/signin?openid.assoc_handle=aws&openid.return_to=https%3A%2F%2Fsignin.aws.amazon.com%2Foauth%3Fresponse_type%3Dcode%26client_id%3Darn%253Aaws%253Aiam%253A%253A015428540659%253Auser%252Fawssignupportal%26redirect_uri%3Dhttps%253A%252F%252Fportal.aws.amazon.com%252Fbilling%252Fsignup%253Fredirect_url%253Dhttps%25253A%25252F%25252Faws.amazon.com%25252Fregistration-confirmation%2526state%253DhashArgs%252523%2526isauthcode%253Dtrue%26noAuthCookie%3Dtrue&openid.mode=checkid_setup&openid.ns=http://specs.openid.net/auth/2.0&openid.identity=http://specs.openid.net/auth/2.0/identifier_select&openid.claimed_id=http://specs.openid.net/auth/2.0/identifier_select&openid.pape.preferred_auth_policies=MultifactorPhysical&openid.pape.max_auth_age=0&openid.ns.pape=http://specs.openid.net/extensions/pape/1.0&server=/ap/signin&forceMobileApp=&forceMobileLayout=&pageId=aws.ssop&ie=UTF8)  
1. Follow the prompts to create an account on aws.   
2. Once you are in the console, select 'Services' from the drop down menu.  
3. Select 'Elastic Beanstalk'  
4. Select 'Get Started'  
5. Choose 'Node.js' from the platform dropdown
6. Choose an application name. (Aside: Applications are groups of instances, you could just name this 'project' if you want, and later name the instance the name of your app.)  
7. Click 'Configure more options'
8. Click 'Environment Settings'
9. Create a name for your application.
10. Click 'Create app'



[travis](https://travis-ci.org/)
1. Create an account
2. Click the plus button in the top left
3. Toggle the correct repo
4. Add a .travis.yml file to your project

```javascript

```


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

# get fancy
git branch -u origin/master # now you only need 'git push' as opposed to 'git push origin master'
```

### Use a .gitignore to keep your project clean.
This one is pretty useful for me and my naming conventions.  
```javascript
# Node files
node_modules

# Debug logs
*.log*

# Mac trash
DS_STORE

# Yarn versioning
yarn.lock

# Istanbul reports
coverage
.nyc_output

# Production build
dist

# Assets
assets

# Test cache
C:UsersUsernodejsnpm-cache
public
```

### Use commitizen and semantic release to keep git commit messages clean and automatically create changelogs.
