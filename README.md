# PupperCoin

We've decided to embark on an exciting new endeavour that allows us to track dog breeding globally, in a decentralized way. This will allow pet parents to track their pets genetic trail. In order to Fund this Network we will crowdsale our `PupperCoin Token`.

For this we will be using Remix, Metamask, Ropsten Ethereum Faucet, and Ganache. 

The testnet Ethereum Faucet will give us .3 ETH, this can be done by putting your account number found in Metamask into the search bar, then hitting the `Send me test Ether` button. As shown in the diagram below.

![image](https://user-images.githubusercontent.com/83382006/136881389-40c45208-0467-4838-a231-35136af7e904.png)

Once that is complete you'll see .3 ETH available in your Metamask. 

To begin this code we created a file named `PupperCoin.sol` where in the parameters we used the standard ERC20Mintable, ERC20Detailed, and hard coded 18 as the decimals, and left the initial_supply parameter alone.

![image](https://user-images.githubusercontent.com/83382006/136881305-dc7b6b64-4a33-4799-8351-a098ada7bf16.png)

As shown below we bootstrapper the foloowing contracts using the OpenZepplin library: Specifically `Crowdsale`, `MintedCrowdsale`, `CappedCrowdsale`, `TimedCrowdsale`, `RefundablePostDeliveryCrowdsale.`
The parameters for all of these include, name, symbol, wallet and goal. 
when passing the open and close times, now, now + 24 weks was used from the PupperCoinCrowdsaleDeployer.
![image](https://user-images.githubusercontent.com/83382006/136881147-fe5dda0c-0318-49b7-b5ff-4e66f3890c50.png)

![image](https://user-images.githubusercontent.com/83382006/136881224-ab629dbb-8f06-4d1c-a9ee-36c5727ebfd7.png)

![image](https://user-images.githubusercontent.com/83382006/136881263-5fcb5d12-8075-419d-adbe-637c3b28dc81.png)

Once that was completed we compiled and deployed the Deployer and was given acces to the Token_address, and Token_sale_address. Using notepad both were saved and Using MetaMask PupperCoin was created as PUP. 

![image](https://user-images.githubusercontent.com/83382006/136877605-9091b831-8cfd-48b3-8643-8e4f2dc01ab6.png)


![image](https://user-images.githubusercontent.com/83382006/136877676-96a930d5-c177-46d6-80af-8427ad26b1e5.png)


![image](https://user-images.githubusercontent.com/83382006/136877770-add3e3ea-dd15-4be3-bd23-76f572ac265a.png)




Now to test the CrowdSale.

You can test the time functionality by replacing now with fakenow, and creating a setter function close time to be now + 5 minutes. The Deployer Network is the Ropsten network. We deploy and test the Netowrk and see how much we get. 

As seen here.
![image](https://user-images.githubusercontent.com/83382006/136877807-c0f2e00f-8d9b-4dfb-88d5-45734290f390.png)
