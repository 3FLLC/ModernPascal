==**Linux Binaries**==

Each ZIP will contain one of the following binaries:
* mp2 (Modern Pascal v2.0) latest commandline interpreter
* coderunner2 (Modern Pascal v2.0) latest standalone script server, like node.js but faster and larger scale
* libmod_mp2.so (Modern Pascal v2.0) latest Apache Module script engine, like PHP but for structured pascal

Normally I install the **mp2** COMMAND LINE INTERFACE (CLI) binary in either /bin, /usr/bin or /usr/local/bin depending upon the OS structure.

Same with coderunner2, then I create a coderunner script in the /etc/init.d/ folder, or I launch it in /etc/rc.local.
* it looks in the local folder for coderunner.conf if not found, looks in /etc/coderunner.conf
* Structure of coderunner2.conf:
```
    [Listeners]
    Servers=2
    
    [Listener1]
    Port=6400
    Blocking=no
    Nagle=no
    OnConnect=/home/onixon/bbs/quickbbs3.p
    
    [Listener2]
    Port=110
    OnConnect=/home/onixon/email/pop3.p
```

**Latest Changes**

Decided to make CLI and CodeRunner FREE release to include OpenSSL support. More and more sites are demanding SSL connections, so instead of making SSL/TLS a feature of the registered product (for client connections/sessions), I have decided to push the feature forward to the public FREE release.

From 2018 to now, there is are two new units - **bbs** (contains DXJAM (J.A.M. Message Base format), and **cipher** (contains a handful of encryption algorithms).
