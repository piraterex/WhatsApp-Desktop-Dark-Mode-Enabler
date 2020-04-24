# WhatsApp-Desktop-Dark-Mode-Enabler
Enable dark mode in WhatsApp Desktop version of MacOS
(Although it must be similar in windows client too)

### Prerequisites

What things you need to install before starting up

```
WhatsApp Desktop Application
Homebrew
Nodejs
asar node module
```
Installing section is just to install prerequisites if you already don't have them. Otherwise skip to #### Applying Dark Mode
### Installing
 
Follow these Steps:
1. You need to install Whatsapp Desktop on your Mac(Download from [OFFICIAL WEBSITE](https://www.whatsapp.com/download) is suggested rather than app store version).
2. Open Terminal and Install Homebrew
```
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
This will install Homebrew on your Mac. To check the version type the following command.
```
$ brew -v
```
3. Install Nodejs using Homebrew
```
$ brew install node
```
If everything installed successfully then you can type in the following command in the terminal to check the Node and NPM version.
```
$ node -v
$ npm -v
```
4. Install asar node module globally
```
$ npm install -g asar
```

### Applying Dark Mode
1. Go into the app’s directory
```
$ cd /Applications/WhatsApp.app/Contents/Resources
```
2. Create a directory for our working
```
$ mkdir temp-darkmode
```
3. Unpack the app.asar file in the above directory using asar
```
$ asar extract app.asar temp-darkmode 
```
4. Open directory temp-darkmode and insert the code
```
cd temp-darkmode
```
open index.html and edit
```
nano index.html
```
find body
```
  <body class="native darwin">
```
replace it with code below
  ```
  <body class="native darwin dark">
  ```
save the file, hit ctrl+x
type y and enter
5. Pack the app.asar file
Go into the app’s directory
```
$ cd /Applications/WhatsApp.app/Contents/Resources
```
to pack type
```
sudo asar pack temp-darkmode app.asar
```
6. You are done
    
## Authors

* **piraterex**  - [hackdworld](https://www.hackdworld-lk.blogspot.in)
