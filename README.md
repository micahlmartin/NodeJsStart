# Getting Started with NodeJS

## Tools
- Install NodeJS [http://nodejs.org/](http://nodejs.org/)
- Install Sublime Text 2: [http://www.sublimetext.com/2](http://www.sublimetext.com/2)
- Install Sublime Package Manager [http://wbond.net/sublime_packages/package_control/installation](http://wbond.net/sublime_packages/package_control/installation)  
```  
import urllib2,os; pf='Package Control.sublime-package'; ipp=sublime.installed_packages_path(); os.makedirs(ipp) if not os.path.exists(ipp) else None; urllib2.install_opener(urllib2.build_opener(urllib2.ProxyHandler())); open(os.path.join(ipp,pf),'wb').write(urllib2.urlopen('http://sublime.wbond.net/'+pf.replace(' ','%20')).read()); print('Please restart Sublime Text to finish installation')
```   


From the command prompt or terminal run these commands to install coffeescript and the less compiler with the node package manager  
```
npm install -g coffee-script   
npm install -g less  
```  

In order to get some of the tools to work within sublime you will likely need to make sure they are installed in your path.
In sublime press CMD+SHIFT+P (or CTRL+SHIFT+P in windows) and type `install package`. From there you can install any available packages.  

## Sublime packages to install

- less-build
- less
- coffee-compile
- coffeescript
- coffeelint

### Configure coffeescript to compile within sublime  
To edit your coffeescript build package, on your menu go to `Sublime Text 2 -> Preferences -> Browse Packages` and open the file `CoffeeScript.sublime-build`.  
Replace it's contents with the following:  


Mac Users:  
```  
{
    "cmd": ["coffee", "-c", "$file"],
    "selector" : "source.coffee",
    "path" : "/usr/local/bin"
}
```

Windows Users:  
```  
{
    "cmd": ["coffee.cmd","-c","$file"],
    "file_regex": "^(...*?):([0-9]*):?([0-9]*)",
    "selector": "source.coffee"
}  
```  

