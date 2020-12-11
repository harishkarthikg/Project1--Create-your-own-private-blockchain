# Create-Your-Own-Private-Blockchain
In this project, we are trying to create a test application that will allow to register stars as well as ensuring that the application knows who owned each star

## Libraries
    - "bitcoinjs-lib": "^4.0.3",
    - "bitcoinjs-message": "^2.0.0",
    - "body-parser": "^1.18.3",
    - "crypto-js": "^3.1.9-1",
    - "express": "^4.16.4",
    - "hex2ascii": "0.0.3",
    - "morgan": "^1.9.1",
    - "tiny-secp256k1": "^1.1.5"

## Architecture of Solution: 
- Solution mainly consists of two main parts- Block.js & Blockchain.js
- In Block.js file we are going to implement the following:
    - Validate()- Method to validate if the block has been tampered or not 
    - getBData()- Auxillary method to return block body
- In Blockchain.js we are going to implement the following:
    - _addblock(block)- To store a block in blockchain
    - requestMessageOwnershipVerification(address)- Request a message to sign with the wallet
    - submitStar(address, message, signature, star)- Allow users to register a new star
    - getblockbyHash()- To return a promise that will resolve with the Block 
    - getwalletaddress()- To resolve with array of stars and owner to the wallet passed as parameter
    - validateChain()- To resolve error when validating chain 


## Implementation of Architecture: 
1. Run application using 'node app.js'
     - Following output will be displayed
          - 'Server Listening for port: 8000'

2. Using POSTMAN, request genesis block using GET- http://localhost:8000/block/0 

3. Using POSTMAN, make request of ownership sending the wallet address- 
    - POST- http://localhost:8000/requestValidation

4. Sign the message in Electrum wallet with the address & message

5. Using POSTMAN, submitstar - POST- localhost:8000/submitstar

6. Using POSTMAN request star- POST - localhost:8000/blocks/15zo6J8P1i6Tbtw8aEKmWQSLS11BCcvgL9



### Conclusion: 
In this project, we learned how to implement an own private Blockchain. Also gained hands on experience on using Bitcoincore, Electrum wallet, POSTMAN

### Credits: 
- Udacity knowledge board
- [Bitcoin Forum](https://bitcoin.org/en/community)
- [Github Community](github.com)
    
