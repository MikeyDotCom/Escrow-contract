# Escrow-contract
Developed with Mist and solidity

source: https://medium.com/@pranav.89/smart-contracting-simplified-escrow-in-solidity-ethereum-b19761e8fe74

This project demonstrats a simple Escrow contract developed on the Ethereum test network with mist in Solidity.

What is 'Escrow'

Escrow is a legal concept in which a financial instrument or an asset is held by a third party on behalf of two other parties that are in the process of completing a transaction. The funds or assets are held by the escrow agent until it receives the appropriate instructions or until predetermined contractual obligations have been fulfilled. Money, securities, funds, and other assets can all be held in escrow.

Read more: Escrow https://www.investopedia.com/terms/e/escrow.asp#ixzz58sXL4ESN

Installation:
1)  Download Mist: https://github.com/ethereum/mist/releases
What is Mist? Mist is the browser for decentralized web apps on the Ethereum blockchain.  

2) Extract the zip file and start the installation wizard by opening the mist.exe file

3)  Once the application installed you can open the application. The first time it will start downloading the live Ethereum blockchain. Click the "Launch application" button to start the application user interface.


Configuration:

4) In the menu bar at the top, go to: "Develop" => "Network" => Select "Rinkeby - Test network". Mist will now downlaod the Ethereum test blockchain, where you can test out Smart contracts.

5) Once the blockchain has been downloaded you have to create you accounts. In the menu bar at the left, click on the green "Wallets" icon => Click "Add account". => Click "Create new account" => enter a password and click "Ok" => A new account is added to your overview. 

6) Repeat stap 5 until you have 3 different accounts. Rename de accounts into, Escrow, Buyer and Seller. You can rename the account by clicking on the account. Then double click on Account, you can now rename your account. 

Fund accounts:

7) In order to get some Ether tokens for the test network, go to https://faucet.rinkeby.io/ and follow the instructions. Send the Ether to the Escrow account. 

8) Once you have received funds in you Escrow account, you can send 1 ether to you Buyers account. Click on the "Send" button and fill in the form.  

Run the contract:

9) Now that the Escrow and the Buyer accounts are funded, you can test the Escrow contract. Go to "Contracts" => click on the "Deploy new contract" => If the "From" field select the "Escrow" account => Left amount blank => copy the code from this repository "Escrow.sol" => Delete the example code in the "Solidity contract source code" window => Past the code you just copied.

10) At the right you now see, select a "Select contract to deploy" field. Select the "Escrow" contract => Move the "Select fee" dot to the right, for the fastest transaction time

11) Before we can run the contract we also have to provide the system with the "Constructor parameters", Buyer and Seller address. Copy the buyer adress from the account and past them in to the "Buyer adress" field. Repaet this for the Seller address.  

12) Now click the "Deploy" button => fill in your password and click "Send transaction". Once you have 1 confirmation you can continue with the next stap.

13) Now open the new contract by clicking on "Contracts" icon =>  Select the new contract under "Custom contracts".

14) Under "Write to contract" select function "Deposit" => Execute from, select "Buyer" => In "Send ether" type 1 => Click "Execute" => type your password and click "Send transaction". Once you have 1 confirmation you can continue with the next stap.

15) Now open the new contract by clicking on "Contracts" icon =>  Select the new contract under "Custom contracts". => the contract should now hold 1 ether.

16) Under "Write to contract" select function "Accept" => Execute from, select "Buyer" => Click "Execute" => type your password and click "Send transaction". Once you have 1 confirmation you can continue with the next stap.

17) Now open the new contract by clicking on "Contracts" icon =>  Select the new contract under "Custom contracts". => the contract should still hold 1 ether.

18) Under "Write to contract" select function "Accept" => Execute from, select "Seller" => Click "Execute" => type your password and click "Send transaction". Once you have 1 confirmation you can continue with the next stap.

19) Voilà, 1 Ether is subtracted form the buyer account and added to the seller account. End of process!
