# Web3MintTokenHTML
Example of how to Mint ERC-721 and ERC-1155 Tokens through HTML web page using Web3 JS and Metamask

1. Enter the address and ABI of the Smart Contract you want to interact with  
You can get this from etherscan.io  
`const ABI = [{"inputs":[],"stateMutability":"nonpayable","type":"constructor"},{"anonymous":false,"inputs" ... ];`
`const ADDRESS = "0x00000000000000000000000000000000";`

2. Set the amount of ETH to be paid as the 'value' (in Wei) - this is only for index721.html  
```
document.getElementById('mint').onclick = () => {
    contract.methods.mint(account, 1).send({ from: account, value: "10000000000000000" });
}
 ```

3. the web pages MUST run on a web server! To run a simple local web server using Python, enter  
`python3 -m http.server`  

then load the web page on  
`http://localhost:8000/`


Questions?  
benwhut@gmail.com
