# Windows Mining

Tutorial - Mine for blocks with Microsoft Windows
Mine for blocks with your Windows wallet and the following instructions.

Click here to download the file millennialglobalcoin-qt-windows.zip.

Open File Explorer and go to your downloads directory.

Extract the zip file millennialglobalcoin-qt-windows.zip

Open "Run" with the keyboard shortcut winkey + r.

Enter the following text behind "Open": notepad

Press on the button "OK".

Paste the following into notepad.

rpcuser=rpc_millennialglobalcoin
rpcpassword=dR2oBQ3K1zYMZQtJFZeAerhWxaJ5Lqeq9J2
rpcbind=0.0.0.0
rpcallowip=127.0.0.1
listen=1
server=1
addnode=37.97.179.18
addnode=102.65.230.58

Click on the menu item "File" -> "Save As...".

The open dialog box will appear, click on "Save as type" and select the option "All Files (*.*)".

Enter the following text behind "File name": millennialglobalcoin.conf

Click on the menu bar, type the following text %appdata% and press on the enter key. enter

Create the folder MillennialGlobalCoin and open the folder.

Press on the button "Save".

Create a new file with the keyboard shortcut ctrl + n.

Paste the following into notepad.

@echo off
set SCRIPT_PATH=%cd%
cd %SCRIPT_PATH%
echo Press [CTRL+C] to stop mining.
:begin
 for /f %%i in ('millennialglobalcoin-cli.exe getnewaddress') do set WALLET_ADDRESS=%%i
 millennialglobalcoin-cli.exe generatetoaddress 1 %WALLET_ADDRESS%
goto begin

Click on the menu item "File" -> "Save As...".

The open dialog box will appear, click on "Save as type" and select the option "All Files (*.*)".

Enter the following text behind "File name": mine.bat

Click on the menu bar, open the location where you extracted the zip file millennialglobalcoin-qt-windows.zip.

Press on the button "Save".

Open your wallet and execute mine.bat to mine your first block.
