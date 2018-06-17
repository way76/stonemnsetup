# Stone Masternode Setup Guide: 5 step simple guide EXPERIENCED - Beginners scroll down to the next section.

1. Open latest release Stone wallet found [HERE](https://github.com/stonecoinproject/Stonecoin/releases) Open Tools> Debug Console and type `masternode genkey` Copy the result.

2. `wget -q https://raw.githubusercontent.com/stonecoinproject/stonemnsetup/master/stonemnsetup.sh`

3. `bash stonemnsetup.sh` Paste your masternode genkey when prompted.

4. In windows wallet go to Tools> Open Masternode configuration file and fill out the form:
`# Format: alias IP:port masternodeprivkey collateral_output_txid collateral_output_index
mn1 YOUR_IP:22323 93HaYBVUCYjEMeeH1Y4sBGLALQZE1Yc1K64xiqgX37tGBDQL8Xg 2bcd3c84c84f87eaa86e4e56834c92927a07f9e18718810b92e0d0324456a67c 0` Save and close.

5. Settings> Options> Wallet> Check "Show Masternodes Tab" then restart wallet. Open masternodes tab, right click your masternode and "start alias." It will read PRE-ENABLED and will turn to ENABLED in a few minutes.

**Congratulations, you're now setup! Enjoy collecting your pebbles, trade them, accept them, Hodl them and may someday they turn into valuable Stones! Thank you for supporting the Stonecoin Rockchain!!**

**Stone donations go towards development**
* STONE: `Si8dAZHaP1utVqxJJf1t2KVU6cBkk6FrVz`

# Stone Masternode Setup Guide (Ubuntu 16.04) BEGINNERS
This guide will assist you in setting up a Stone Masternode on a Linux Server running Ubuntu 16.04 with a cold wallet, the safest way to run a masternode. (Use at your own risk)

If you require further assistance contact the support team @ [Discord](https://discord.gg/2pr33nF)
***
## Requirements
1) **1,500 Stone.**
2) **A DigitalOcean VPS running Linux Ubuntu 16.04.** [DigitalOcean](https://m.do.co/c/6a9081c1f9a2)
3) **A Windows local wallet.** [Stone GitHub](https://github.com/stonecoinproject/Stonecoin/releases)
4) **An SSH client such as [puTTY](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)**
***
## Contents
* **Section A**: Creating the VPS within [DigitalOcean](https://m.do.co/c/6a9081c1f9a2) $10 free when using this link!.
* **Section B**: Downloading and installing puTTY.
* **Section C**: Connecting to the VPS and installing the MN script via puTTY.
* **Section D**: Preparing the local wallet.
* **Section E**: Connecting & Starting the masternode.
***

## Section A: Creating the VPS within [DigitalOcean](https://m.do.co/c/6a9081c1f9a2) $10 credit!
***Step 1***
* Register at [DigitalOcean](https://m.do.co/c/6a9081c1f9a2) with two months free using this link.
***

***Step 2***
* After you have linked your payment click Create > Droplets
![Example-OS](https://i.imgur.com/wAhrss6.png)
***

***Step 3***
* Choose a server type: Ubuntu 16.04
![Example-OS](https://i.imgur.com/65ExYns.png)
***

***Step 4***
* Choose a server size: $5/mo will be fine 
![Example-OS](https://i.imgur.com/cGW1S1F.png)
***

***Step 5*** 
* Choose a server location (preferably somewhere close to you)
![Example-Location](https://i.imgur.com/ecXeDvK.png)
***

***Step 6*** 
* Choose a Hostname & Label (name it whatever you want)
* Click "Create"
![Example-hostname](https://i.imgur.com/pJC80jj.png)
***

***Step 7***
* Check your email for the password and IP address.
***


## Section B: Downloading and installing puTTY. 

***Step 1***
* Download puTTY [here](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)
***

***Step 2***
* Download the correct installer depending upon your operating system. Then follow the install instructions. 
***


## Section C: Connecting to the VPS & Installing the MN script via puTTY.

***Step 1***
* Copy your VPS IP (you can find this by going to the Droplets tab within DigitalOcean or the email sent after creating.
***

***Step 2***
* Open the puTTY application and fill in the "HostName(or IP address)" box with the IP of your VPS. SSH port is 22.
***

***Step 3***
* Save the address to puTTY by typing a name under "Saved Sessions" then press the "Save" button on the right. You can now connect to this server anytime by selecting it from the list, pressing "load", then "Open".
***

***Step 4***
* Once connected, type "root" as the login/username.
***

***Step 5*** 
* Paste the password into the puTTY terminal by right clicking (it will not show the password so just press enter)
***

***Step 6*** 
* The server will have you create a new password; right click again to paste the old password, then enter your new password twice. This should be a complex passphrase and don't forget to write it down!  
***

***Step 7***
* Paste the code below into the puTTY terminal then press enter (it will just go to a new line)

`wget -q https://raw.githubusercontent.com/stonecoinproject/stonemnsetup/master/stonemnsetup.sh`
***

***Step 8***
* Paste the code below into the puTTY terminal then press enter

`bash stonemnsetup.sh`

***

***Step 9***
* Sit back and wait for the install (this will take 10-20 mins)
***

***Step 10***
* When prompted to enter your GEN key - press enter

***

***Step 11***
* You will now see all of the relavant information for your server.
* Keep this terminal open as we will need the info for the wallet setup.
***

## Section D: Preparing the Local wallet

***Step 1***
* Download and install the Stone wallet [here](https://github.com/stonecoinproject/Stonecoin/releases)
* Go to the receive tab and type in a name then press request payment. Copy the address from the window.
***

***Step 2***
* Send EXACLY 1,500 Stone to address you copied.
***

***Step 3***
* Create a text document to temporarily store information that you will need. 
***

***step 4***
* Go to the debug console within the wallet; Tools>Debug Console
***

***Step 5***
* Type the command below and press enter 

`masternode outputs` 

***

***Step 6***
* Copy the long key (this is your transaction ID) and the 0 or 1 at the end (this is your output index)
* Paste these into the text document you created earlier as you will need them in the next step.
***

# Section E: Connecting & Starting the masternode 

***Step 1***
* Go to the tools > "masternode configuration file" 

***

***Step 2***

* Fill in the form. 
* For `Alias` type something like "MN1" **don't use spaces**
* The `Address` is the IP:port of your server (this will be in the puTTY terminal that you still have open; 206.81.12.251:13058).
* The `PrivKey` is your masternode private key (This is also in the puTTY terminal that you have open).
* The `TxHash` is the transaction ID/long key that you copied to the text file aka "masternode outputs".
* The `Output Index` is the 0 or 1 that you copied to your text file.

Click "File Save" or ctrl+s to save.
***

***Step 3***
* Close the wallet and reopen.
* Click on the Masternodes tab "My masternodes"
* Click start all in the masternodes tab or right click the masternode and click "Start-alias".
***

***step 4***
* Check the status of your masternode within the VPS by using the command below:

`stone-cli masternode status`

* You should see ***"Masternode successfully started"***

If you do, congratulations! You have now setup a masternode. If you have any questions or need troubleshooting reach out on [Discord] (https://discord.gg/2pr33nF)
If you this worked for you please donate to help keep these easy to use methods alive and up to date!

* BTC: `3QFJ9UTJGbBHBYqZsqTzXHyxifML44Wdyp`
* XMR: `445kB5Mxzj5LKeTt6RrgTvciqnPVT4HgyE4zN3grJTvaEyrCMuCPAyx7Kah3bq2RBZMoTauDDVFVvBuKcer5NnCKDoeT9DW`
* LTC: `LgdPXvnYRvQoAVGZq2SUomZwkbv4Hjecok`
* Bcash: `LOL`
* RAVEN: `RKUaCMEKqJi3ERnbEXXh9M3LKTK79hJuSt`
* STONE: `Si8dAZHaP1utVqxJJf1t2KVU6cBkk6FrVz`
***
