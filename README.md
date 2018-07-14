# Velum Automatic Masternode Setup

Step 1: Login to your VPS and download the script using:
```
wget https://raw.githubusercontent.com/VelumPlatform/Velum-Automatic-Masternode-Setup/master/velummnautosetup.sh && chmod +x velummnautosetup.sh
```
Step 2: Run the script:
```
./velummnautosetup.sh
```

Troubleshooting & Notes:

So all steps console and error messages will be recorded to logfile. You can follow it online during script execution in second ssh session using
```
tail -f ~/velummnsetup.log
```

After script execution you can find the main status of steps execution if you filter logfile for rows containing '# '
```
more ~/velummnsetup.log | grep '# '
```

If you have slow internet connection, files may be loading for a long time, which may (with low probability) lead to ssh session timeout. To avoid this, I recommend to launch script in screen session. 
Start new screen session:
```
screen -q
```

Launch the script according to the Steps 1 and 2. 
If ssh session disconnected, script will continue working. After connection restoration, you can attach the screen session with:
```
screen -r -d
```

