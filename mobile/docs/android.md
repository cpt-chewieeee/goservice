1. install java 8 
  ```
    $ sudo add-apt-repository ppa:webupd8team/java
    $ sudo apt-get update
    $ sudo apt-get install java-common oracle-java8-installer
  ```
2. set JAVA_HOME. These commands will set the correct java environment variables
  ```
    $ sudo apt-get install oracle-java8-set-default
    $ source /etc/profile
  ```
3. installing android studio 
  ```
    $ sudo add-apt-repository ppa:maarten-fonville/android-studio
    $ sudo apt update
    $ sudo apt install androi-studio
  ```
4. (optional install with umake)
  ```
    $ sudo add-apt-repository ppa:ubuntu-desktop/ubuntu-make
    $ sudo apt update
    $ sudo apt install ubuntu-make
    $ umake android --accept-license
  ```