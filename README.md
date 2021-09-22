1. First step was to reate accounts for two nodes for the network with a separate datadir for each using geth.  
   run the ./geth --datadir node1 account new and run ./geth --datadir node2 account new and set a password 
   for each node.
  
  <img src="Screen Shots/Nodes Setup.png" width="700" height="500"> 


2. Next, generate genesis block.
    Run puppeth using ./puppeth.
    Name network(I named it adrianbisutti)
    Follow prompts to configure a new genesis block.(Input 2 and 1 for the 2 first questions)
    Choose the Clique (Proof of Authority) consensus algorithm.(Input 2)
    Paste both account addresses(nodes) from the first step one at a time into the list of accounts to seal.(Copy and 
    Paste them again in the list of accounts to pre-fund. 
    Choose no for pre-funding the pre-compiled accounts (0x1 .. 0xff) with wei. This keeps the genesis cleaner.
    Complete the rest of the prompts, and when back at the main menu, choose the "Manage existing genesis" option 
    by inputing 2 twice.
    Export genesis configurations by creating a networkname.json.(mine is adrianbisutti)

<img src="Screen Shots/Step 2 PArt 1.png" width="700" height="500"> 



<img src="Screen Shots/Step 2 PArt 2.png" width="700" height="500">

3. With the genesis block creation completed now I needed to initialize the nodes with the genesis' json file.
   Using geth, initialize each node with the new networkname.json.

    ./geth --datadir node1 adrianbisutti.json
    ./geth --datadir node2 adrianbisutti.json
    

<img src="Screen Shots/Initialize Nodes.png" width="700" height="500"> 
 
     
  
4.  Run the nodes in separate terminal windows with the commands:

    ./geth --datadir node1 --unlock "SEALER_ONE_ADDRESS" --mine --rpc --allow-insecure-unlock
    ./geth --datadir node2 --unlock "SEALER_TWO_ADDRESS" --mine --port 30304 --bootnodes   
    "enode://SEALER_ONE_ENODE_ADDRESS@127.0.0.1:30303" --ipcdisable --allow-insecure-unlock
    
<img src="Screen Shots/Mining Node 1.png" width="700" height="500"> 

<img src="Screen Shots/Mining Node 2.png" width="700" height="500"> 
  

5. Open the MyCrypto app, then click Change Network at the bottom left

<img src="Screen Shots/Change Network.png" width="700" height="500"> 

6. Click "Add Custom Node", then add the custom network information that you set in the genesis.
   ***Note My Node Nname and Network Name is adrianbisutti***
   
<img src="Screen Shots/Set Up Your Custom Node.png" width="700" height="500"> 
  
7. Type ETH in the Currency box. Then in the Chain ID box, type the chain id you generated during genesis creation. In the URL box type: http://127.0.0.1:8545.  This points to the default RPC port on local machine. Finally, click Save & Use Custom Node.

<img src="Screen Shots/Set Up Your Custom Node.png" width="700" height="500"> 

<img src="Screen Shots/SAve and Use custom node.png" width="700" height="500"> 



8. On the next screen, click Select Wallet File, then navigate to the keystore directory inside Node1 directory, select the file located there, provide password when prompted and then click Unlock.

<img src="Screen Shots/Access Node1.png" width="700" height="500"> 

9. In the To Address box, type the account address from Node2, then fill in an arbitrary amount of ETH. Click Send Tranaction to complete tranasaction.

<img src="Screen Shots/Sending ETH to Node 1.png" width="700" height="500"> 

10. Confirm the status of the Transaction is succesful.

<img src="Screen Shots/Transaction Confirmation Part 1.png" width="700" height="500"> 

<img src="Screen Shots/Transaction Confirmation Part 2.png" width="700" height="500"> 