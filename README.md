# StoneCoin Masternode Setup Guide: 3 step simple guide EXPERIENCED - Beginners scroll down to the next section.

1. `wget -O - https://raw.githubusercontent.com/stonecoinproject/stonemnsetup/master/stonemnsetup.sh | bash`

2. In windows wallet go to Tools> Open Masternode configuration file and fill out the form using the green line from the script:

`# Format: alias IP:port masternodeprivkey collateral_output_txid collateral_output_index
mn1`

`MN1 YOUR_IP:22323 93HaYBVUCYjEMeeH1Y4sBGLALQZE1Yc1K64xiqgX37tGBDQL8Xg 2bcd3c84c84f87eaa86e4e56834c92927a07f9e18718810b92e0d0324456a67c 0` Save and close.

3. Open masternodes tab, right click your masternode and "start alias." It will read PRE-ENABLED and will turn to ENABLED in about 15 minutes.

**Congratulations, you're now setup! Enjoy collecting your pebbles, trade them, accept them, Hodl them and may someday they turn into valuable Stones! Thank you for supporting the Stonecoin Rockchain!!**

**Stone donations go towards development**
* STONE: `Si8dAZHaP1utVqxJJf1t2KVU6cBkk6FrVz`

# Stone Masternode Setup Guide (Ubuntu 16.04) BEGINNERS
This guide will assist you in setting up a Stone Masternode on a Linux Server running Ubuntu 16.04 with a cold wallet, the safest way to run a masternode. (Use at your own risk)

If you require further assistance contact the support team @ [Discord](https://discord.gg/2pr33nF)
***
## Requirements
1) **1,500 Stone.**
2) **A VPS running Linux Ubuntu 16.04.** Get $10 free with [DigitalOcean](https://m.do.co/c/6a9081c1f9a2)
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
* Choose a server location (preferably somewhere close to you).
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

## Section C: Preparing the Local wallet

***Step 1***
* Download and install the Stone wallet [here](https://github.com/stonecoinproject/Stonecoin/releases)
* Navigate to Settings > Options > Wallet tab check and make sure the "Show Masternodes Tab" is checked.
***

***Step 2***
* Go to the receive tab and type in a name then press request payment. Copy the address from the window.
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
***Step 5***
* Copy the two part result without any special characters. The first number is the masternode TX ID(Long) and the second is the Output index number(1 or 0). These will be used in the next section.
***

## Section D: Connecting to the VPS & Installing the MN script via puTTY.

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
* The server will have you create a new password; right click again to paste the old password, then enter your new password twice. This should be a complex passphrase. If you forget, there is always the forgot password function in the digital ocean dashboard.  
***

***Step 7***
* Paste the code below into the puTTY terminal then press enter.

`wget -O - https://raw.githubusercontent.com/stonecoinproject/stonemnsetup/master/stonemnsetup.sh | bash`
***

***Step 8***
* Sit back and wait for the install (this could take 10-20 mins).
***

***Step 9***
* The script will walk you through 3 prompts:
`Give your masternode a name:`
* Enter any name you want, this will be the alias used when you receive payments.
`Paste the transaction ID from masternode outputs:`
* Enter the long hex you copied to your text file
`Enter the output index number from masternode outputs 0 or 1:`
* Enter the 1 or 0 you copied to your text file
* Finally hit enter when you're ready to continue
***

***Step 10***
* You will now see all of the relavant information for your server.
* Copy the green line that starts with the name you gave your masternode, circled in red in the image.
![Example-OS](https://i.imgur.com/3rJA10P.png)
***

## Section E: Completing local setup and starting the masternode remotely

***Step 1***
* Go to the tools > "masternode configuration file" 
***

***Step 2***
* Paste the green text line on a new line in this document then Save and Close.
***

***Step 3***
* Re-open your local wallet.
* In wallet main window, click on the Masternodes tab "My masternodes"
* Click start all in the masternodes tab or right click the masternode and click "Start-alias".
***

***step 4***
* Check the status of your masternode within the VPS by using the command below:

`stonecoin-cli masternode status`

* You should see ***"Masternode successfully started"***

If you do, congratulations! You have now setup a masternode. If you have any questions or need troubleshooting reach out on [Discord] (https://discord.gg/2pr33nF)
If you this worked for you please donate to help keep these easy to use methods alive and up to date!

* BTC: `3QFJ9UTJGbBHBYqZsqTzXHyxifML44Wdyp`
* XMR: `445kB5Mxzj5LKeTt6RrgTvciqnPVT4HgyE4zN3grJTvaEyrCMuCPAyx7Kah3bq2RBZMoTauDDVFVvBuKcer5NnCKDoeT9DW`
* LTC: `LgdPXvnYRvQoAVGZq2SUomZwkbv4Hjecok`
* RAVEN: `RKUaCMEKqJi3ERnbEXXh9M3LKTK79hJuSt`
* STONE: `Si8dAZHaP1utVqxJJf1t2KVU6cBkk6FrVz`
***
