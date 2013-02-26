# Getting Started with NodeJS

## Tools
- Install NodeJS [http://nodejs.org/](http://nodejs.org/)
- Install Sublime Text 2: [http://www.sublimetext.com/2](http://www.sublimetext.com/2)
- Install Sublime Package Manager [http://wbond.net/sublime_packages/package_control/installation](http://wbond.net/sublime_packages/package_control/installation)  
```  
import urllib2,os; pf='Package Control.sublime-package'; ipp=sublime.installed_packages_path(); os.makedirs(ipp) if not os.path.exists(ipp) else None; urllib2.install_opener(urllib2.build_opener(urllib2.ProxyHandler())); open(os.path.join(ipp,pf),'wb').write(urllib2.urlopen('http://sublime.wbond.net/'+pf.replace(' ','%20')).read()); print('Please restart Sublime Text to finish installation')
```   
- From the command prompt or terminal run these commands to install coffee script with the node package manager  
```
npm install -g coffee-script   
```  
- Install the less compiler  
```
npm install -g less  
```  

In order to get some of the tools to work within sublime you will likely need to make sure they are installed in your path.
