## Maven Installation Steps:-

### Step 1 :- Install Java Version-11
```sudo yum install java-11-amazon-corretto -y```

### Step 2 :- Download Binary Files for Maven
``` sudo wget https://dlcdn.apache.org/maven/maven-3/3.9.6/binaries/apache-maven-3.9.6-bin.zip```

### Step 3 :- Unzip Files
```
    sudo unzip apache-maven-3.9.6-bin.zip /opt
    sudo cd /opt
    sudo mv apache-maven-3.9.6 maven
    sudo cd maven
```
### Set Up Maven Environment Variables
``` sudo vim /etc/profile.d/maven.sh ```
#### Add the following lines to "maven.sh":-
    ```export M2_HOME=/opt/maven
       export MAVEN_HOME=/opt/maven
       export PATH=${M2_HOME}/bin:${PATH}
       ```
### Make the script executable 
``` sudo chmod o+x /etc/profile.d/maven.sh```

### Load the environment variable
```sudo source /etc/profile.d/maven.sh ```
### Verify the Maven Installation
``` sudo mvn --version ```
### You should see output simillar to :-

<h4>Apache Maven 3.8.6 (cecedd343002696d0abb50b32b541b8a6ba288f9)<br>
Maven home: /opt/maven <br>
Java version: 11.0.12, vendor: Amazon.com Inc.<br>
Java home: /usr/lib/jvm/java-11-openjdk-11.0.12.7-0.amzn2.0.1.x86_64 <br>
Default locale: en_US, platform encoding: UTF-8<br>
OS name: "linux", version: "4.14.256-197.484.amzn2.x86_64", arch: "amd64", family: "unix" </h4><br>
