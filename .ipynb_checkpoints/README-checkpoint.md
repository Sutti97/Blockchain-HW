![image](https://user-images.githubusercontent.com/84012921/133362759-d7eaa7f5-4307-473d-93e1-7baf996d5da1.png)

1. First step is to open up gitbash in the directory you downloaded your geth tools 
2.You will need to enter the command <mark>./puppeth.exe</mark>
You will then run 
3. Name your network and keep note of it
3. 2 
4. 1 
5. 1 
6. _Copy and paste your wallet address exclusding the first 0x and then press enter twice_
8. _number your chain ID <mark> Make Sure to Write it Down</mark>_ 
9. _Ctrl C_ 
10. _You have finished the first step!_


![image](https://user-images.githubusercontent.com/84012921/133362850-e2925a28-4aab-45c2-bec8-80a99fafe56e.png)

1. The second is quite simular ,you will need to enter the command <mark>./puppeth.exe</mark> 
You will then run: 
2. _Enter the same network name_
3. _2_ 
4. _2_  
5. _Ctrl C_ 
6. _You have finished the second step!_


![image](https://user-images.githubusercontent.com/84012921/133363055-dc11d367-d0fc-4624-b936-456b25f5bd16.png)

1. Run _./geth account new --datadir node<mark>1</mark>_ - Set a passwork and take note of it_
2. Run ./geth account new --datadir node<mark>2</mark>_ - Set a passwork and take note of it_
9. _Ctrl C_ 
10. _Third step.....Completed!_



![image](https://user-images.githubusercontent.com/84012921/133363186-5e960fb2-6f4a-46f1-94f3-acb640df6034.png)

1. _Run ./geth init <mark>INSERT YOUR NETWORK HERE</mark>.json --datadir node<mark>1</mark>_ 
2. _Run ./geth init <mark>INSERT YOUR NETWORK HERE</mark>.json --datadir node<mark>2</mark>_
 


![image](https://user-images.githubusercontent.com/84012921/133363430-2d89752d-7a75-4115-96a3-d6319f1c3d78.png)

1. _Run ./geth --datadir node1 --mine --minerthreads 1
2. _Take note of the hightlighted area, copy it as you will need it for the node_

![image](https://user-images.githubusercontent.com/84012921/133708955-763bfec8-9a43-4fc5-a2ab-bd020f59cb36.png)

1. _Run ./geth --datadir node2 --port 30304 --rpc --bootnodes "<mark>INPUT YOUR ENODE HERE</mark>" --ipcdisable

![image](https://user-images.githubusercontent.com/84012921/133363986-7c469255-de5d-4c4d-938f-6bddf658e29a.png)

Head Over to your mycrypto app and select change network on the bottom left


![image](https://user-images.githubusercontent.com/84012921/133364073-00dcebd5-747d-41eb-af4f-6842bebf1515.png)

Select Add Custome Node

![image](https://user-images.githubusercontent.com/84012921/133364204-7f8082e1-931d-46e6-8b89-22fe794a4c52.png)


Input:
1. Node name
2. Change network to Custome
3. Network name (can be the same as node name)
4. Chnage currency to ETH
5. Input the chain ID you took down earlier
6. Input _<mark>http:127.0.0.1:8545</mark>_


![image](https://user-images.githubusercontent.com/84012921/133364320-8647fa5d-97fe-497b-9f59-3f5f8707b6ac.png)

1. Login
2. Go to the tab 'Send Ether & Tokens 
3. Copy your address and input it in the 'address' section
4. Press send

![image](https://user-images.githubusercontent.com/84012921/133364826-a555f3cb-70fd-440e-9df2-6d3407db9ed8.png)

All done!




