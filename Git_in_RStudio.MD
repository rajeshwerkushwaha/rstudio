## Steps to get working with Git in RStudio on Mac  
1. Install git on your machine  
    1. Download git from [Git website](https://git-scm.com/downloads) and install  
    
    2. Or use [Homebrew](https://brew.sh) to install git using the below command:  
    `$ brew install git`  
    
    3. Check location of Git  
    `$ which git`  
    
    4. Check version of Git  
    `$ git --version`  
    
    5. Set your username  
    `$ git config --global user.name "Your Name Here"`  
    
    6. Set your email address  
    `git config --global user.email "username@domain.com"`  
    
    7. Set your osxkeychain  
    `git config --global credential.helper osxkeychain`  
    
2. Install RSudio from the [Cran R-project](http://cran.us.r-project.org) website.  

3. Open RStudio and goto:  
`RSutio > Preferences > Git/SVN option`  
    1. Tick the checkbox for 'Enable version control interface for RStudio projects'  
    2. Click on Browse and select the Git executable location which you get from step 1.3  
    3. Click on 'View public key' and copy it and paste it into your Git SSH settings,  
    if you don't have RSA key then create new key and then copy and paste it into your Git SSH settings.  
    4. Click on Apply and OK.
    
4. Now you are all set to create a new project/existing project and commit your changes to your git account.

### Note:  
If you faced any issue like below:  
`error: unable to read askpass response from 'rpostback-askpass'  
fatal: could not read Username for 'https://github.groupondev.com': Device not configured`  

Instead of cloning using HTTPS try to update with SSH link in terminal like below:  
`$ git remote set-url origin git@github.groupondev.com:[username]/[your_reporsitory].git`
