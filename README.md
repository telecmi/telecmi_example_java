# TeleCMI Webhook Java

TeleCMI webhooks implementation in java. Use our simple java web server to test your webhooks and live events locally for development purpose.

## Install

Follow the below installation instructions

### Prerequisites

Prerequisites for java web server.

- <a href="https://git-scm.com/" target="_blank">git</a> (>= 2.20.1 required)
- <a href="https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html" target="_blank">Java JDK</a> (>= 8 required)
- <a href="https://gradle.org/install/" target="_blank">Gradle</a> (>= 6.0 required)


### Clone the repository

Use command __git clone__ to clone the java webserver from our <a href="https://github.com/telecmi/telecmi_example_java" target="_blank">TeleCMI github repository</a>.

```bash
$ git clone https://github.com/telecmi/telecmi_example_java.git
$ cd telecmi_example_java
```

Add this repository to your system’s Software Sources.

```bash
$ sudo add-apt-repository ppa:openjdk-r/ppa
```

```bash
$ sudo apt-get update
```
Install OpenJDK 8

```bash
$ sudo apt-get install openjdk-8-jdk
```
Install Gradle

```bash
$ sudo apt-get install gradle
```

## Run

Run your java server using the below command

```bash
$ gradle run
```
Now you can able to test our webhooks and live events, from your local server. To expose your local web server to the internet use ngrok. 

You can create a secure HTTP tunnel by providing the port number on which your web server is running. For example, your web server is running on port number 5000. you can launch your HTTP tunnel with the following command line.

```bash
$ ./ngrok http 5000
```

After exposing your local webserver to the internet using ngrok you will get the following output.

```bash
ngrok by @inconshreveable                                       (Ctrl+C to quit)
                                                                                
Session Status                online                                            
Session Expires               7 hours, 59 minutes                               
Update                        update available (version 2.3.35, Ctrl-U to update
Version                       2.3.34                                            
Region                        United States (us)                                
Web Interface                 http://127.0.0.1:4040                             
Forwarding                    http://c654b286.ngrok.io -> http://localhost:5000 
Forwarding                    https://c654b286.ngrok.io -> http://localhost:5000
                                                                                
Connections                   ttl     opn     rt1     rt5     p50     p90       
                              0       0       0.00    0.00    0.00    0.00  
```
Now you can get your dynamic URL from the above output. To configure webhooks and live events, paste your dynamic URL with correct path in webhooks section.

#### Sample URL with path
```
http://c654b286.ngrok.io/webhook/cdr
```



