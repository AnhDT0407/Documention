# Install Tomcat for MacOS

### Here are the easy to follow steps to get it up and running on your Mac

1. Download a binary distribution of the core module: apache-tomcat-9.0.xx from [here](http://tomcat.apache.org/download-90.cgi). I picked the **tar.gz** in Binary Distributions / Core section.

2. Opening/unarchiving the archive will create a new folder structure in your Downloads folder: (btw, this free Unarchiver app is perfect for all kinds of compressed files and superior to the built-in Archive Utility.app)

    *~/Downloads/apache-tomcat-9.0.xx*

3. Open to Terminal app to move the unarchived distribution to **/usr/local**

    `sudo mkdir -p /usr/local`

    `sudo mv ~/Downloads/apache-tomcat-9.0.xx /usr/local`

4. To make it easy to replace this release with future releases, we are going to create a symbolic link that we are going to use when referring to Tomcat (after removing the old link, you might have from installing a previous version):
    
    `sudo rm -f /Library/Tomcat`
    
    `sudo ln -s /usr/local/apache-tomcat-9.0.xx /Library/Tomcat`
    
5. Change ownership of the **/Library/Tomcat** folder hierarchy:

    `sudo chown -R <your_username> /Library/Tomcat`
    
6. Make all scripts executable:

    `sudo chmod +x /Library/Tomcat/bin/*.sh`
    
### Run Tomcat command

- Tomcat 9.x

      /Library/Tomcat/bin/startup.sh
      
      /Library/Tomcat/bin/shutdown.sh
