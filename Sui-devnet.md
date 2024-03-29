# install Cargo version 1.60.0 or higher in order to build and install Sui on your machine https://docs.sui.io/build/install
````
  curl https://sh.rustup.rs/ -sSf | sh
  cargo --version
  ````
# To develop in Sui, you will need the Sui binaries. After installing cargo, run
````
  cargo install --locked --git https://github.com/MystenLabs/sui.git --branch "devnet" sui
````
# Confirm the install with: $ echo $PATH
   And ensure the .cargo/bin directory appears.

# Integrated Development Environment , install Analyzer language 
````
  cargo install --git https://github.com/move-language/move move-analyzer
````
   To confirm that you've installed the language server program successfully,
  execute : $ move-analyzer --version , You should see the output :  move-analyzer 0.0.0.

# download Sui source code 
````
   git clone https://github.com/MystenLabs/sui.git
````
# Create Sui wallet 

  execute on the command line : $ wallet

  The wallet will print the following line if the wallet is starting up the first time :

   Config file ["/Users/dir/.sui/sui_config/wallet.conf"] doesn't exist, do you want to connect to a Sui Gateway [y/n]? 

  Type 'y' and then press 'Enter'. You should see the following output:

   Sui Gateway Url (Default to Sui DevNet if not specified) : 

  The wallet will prompt for the Gateway URL, press 'Enter' and it will default to the DevNet, or enter the URL if you want to connect to a Gateway hosted elsewhere.

If you have used the wallet before, you will have an existing wallet.conf configuration file. Change the configured Gateway URL to DevNet by using:
  wallet switch --gateway https://gateway.devnet.sui.io:9000

The following commands are supported by the wallet:
active-address        Default address used for commands when none specified
addresses             Obtain the addresses managed by the wallet
call                  Call Move function
clear                 Clear screen (interactive only)
create-example-nft    Create an example NFT
echo                  Write arguments to the console output (interactive only)
env                   Print environment (interactive only)
exit                  Exit the interactive shell (interactive only)
gas                   Obtain all gas objects owned by the address
help                  Print this message or the help of the given subcommand(s)
history               Print history
merge-coin            Merge two coin objects into one coin
new-address           Generate new address and keypair
object                Get object info
objects               Obtain all objects owned by the address
publish               Publish Move modules
split-coin            Split a coin object into multiple coins
switch                Switch active address
sync                  Synchronize client state with authorities
transfer-coin         Transfer coin object

# Genesis
   check if ~/.sui/sui_config exists → remove it
   initiate genesis: $ sui genesis

# use the command active-address 
````
wallet active-address
````
# coppy active-address , join discord Sui faucet coin test

# mint NFT 
````
   wallet create-example-nft
````
see output resembling:
Successfully created an ExampleNFT:

Owner: AddressOwner(k#66af3898e7558b79e115ab61184a958497d1905a)
Version: 1
ID: 70874F1ABD0A9A0126726A626FF48374F7B2D9C6
Readonly: false
Type: 0x2::DevNetNFT::DevNetNFT

Check https://explorer.devnet.sui.io/

ok ok

