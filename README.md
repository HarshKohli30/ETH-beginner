# CREATE TOKEN
The "Create Token" project creates a new cryptocurrency called "Solid Star" (SST) with coin and burning functionality. It manages token balances by mapping addresses.
## DescriptionThe "Create Token" project involves the deployment of a smart contract on the Ethereum blockchain to create a new cryptocurrency token called "CryptoCoin(CC). The contract includes features for minting new tokens, increasing the total supply, and for burning tokens, decreasing the total supply, with balances managed via a mapping of addresses.

## Getting Started
### Executing programTo run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.
Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

      
       // SPDX-License-Identifier: MIT
    pragma solidity 0.8.18;
    contract MyToken {
    string public tokenName="Crypto Coin";    string public tokenAbbrv="CC";
    uint public totalSupply=0;
    // mapping variable here    mapping(address => uint) public starbalances;
    // mint function
    function mint(address _address,uint _value) public{        totalSupply += _value;
        starbalances[_address] += _value;    }

    // burn function     function burn(address _address,uint _value) public{
        if(starbalances[_address] >=_value){          totalSupply -= _value;
        starbalances[_address] -= _value;
        }
    }
     }
    
 To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile Hello.sol" button.
Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "HelloWorld" contract from the dropdown menu, and then click on the "Deploy" button.
## Authors
```Harsh Kohli
harshkohli30.9.2002@gmail.com
