# Project Title  
Create a Token.

# Description  
The goal of this project is to use Solidity, a programming language for Ethereum smart contract creation, to create a digital token. The "Sunidhi" token, often known by its acronym "SUNN," has standard features including minting and burning tokens. It guarantees compatibility with compiler versions of Solidity ranging from 0.6.12 to 0.9.0. By initializing token characteristics, assigning balances to addresses, and offering actions for minting and burning tokens, the contract controls the token's lifespan. To provide accurate and safe token supply management, this framework is crucial for applications in digital currencies, loyalty programs, and decentralized finance (DeFi) systems.

# Getting Started

## Installing  
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

```javascript
pragma solidity >=0.6.12 <0.9.0;

contract MyToken {

    string public token_name="Sunidhi";
    string public token_abbrv = "SUNN";
    uint public total_supply = 0;
    mapping(address => uint)public balances;
    function mint(address a_address, uint v_value) public {
        total_supply += v_value;
        balances[a_address] +=v_value;
    }
    function burn(address a_address, uint v_value) public {
        if(balances[a_address] >= v_value){
           total_supply -= v_value;
           balances[a_address] -= v_value;
        }
    } 
}
```

## Executing program    
### How to Run the Program      
Navigate to the project directory  
Compile the Solidity contract  
Deploy the contract using your preferred Ethereum development environment   

#### For Remix:    
Open Remix IDE.  
Upload MyToken.sol.  
Compile and deploy the contract.  


## Any advise for common problems or issues.   
Ensure your Solidity compiler version matches the specified range.  
If you encounter issues with the compiler, try updating to a compatible version.  
Verify the Ethereum development environment is correctly set up.  

# Authors  
Sunidhi Singh @Sunidhi2430

# License  
This project is licensed under the MIT License - see the LICENSE.md file for details.  

We have established a solidity contract with this code. 
