# Web3MintTokenHTML
Example of how to mint ERC-721 and ERC-1155 tokens through HTML web pages using Web3 JS and Metamask

1. Enter the address and ABI of the Smart Contract you want to interact with  
You can get this from etherscan.io  
`const ABI = [{"inputs":[],"stateMutability":"nonpayable","type":"constructor"} ... ];`  
`const ADDRESS = "0x00000000000000000000000000000000";`  

2. Set the amount of ETH to be paid as the 'value' (in Wei) - this is only for index721.html  
```
document.getElementById('mint').onclick = () => {
    contract.methods.mint(account, 1).send({ from: account, value: "10000000000000000" });
}
 ```

3. The web pages MUST run on a web server! To run a simple local web server using Python, open a terminal and enter  
`python3 -m http.server`  

    Then load the web pages on  
    `http://localhost:8000/`  

The HTML web pages are barebones (no styling) for clarity. Once you connect your Metamask wallet, it should look similar to these:  

index721.html  
![](screenshots/721.jpg?raw=true)

index1155.html  
![](screenshots/1155.jpg?raw=true)

When pressed, the mint button will trigger your Metamask wallet to interact with the smart contract and mint a token(s).

Questions?  
benwhut@gmail.com
