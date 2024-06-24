# Creatting a token naming 'Improved Token'.

The ImprovedToken contract is a implementation of a token smart contract on the Ethereum blockchain. It offers the fundamental features for minting and burning tokens as well as keeping track of token holder's balances.

##  Details
Token Name: "Token Balance" 

Token Abbreviation: "TB"

initially the token balance is taken as zero.

Above variables are public.

## Usage
### Create Tokens
Tokens can be created and associated with addresses using the mint function. The total number of tokens that are available is increased by this.


### Mint Tokens
After tokens are created,  we can add tokens to the current balance of the tokens.


### Burn Tokens
We can use the burn function to lower the total number of tokens available if necessary. As a result, tokens are taken out of particular addresses, so decreasing their supply.


## Functions used.


### Mint function

```
function mint (address _address,uint amount) public {

availableAmount += amount;

balances[_address] += amount;


}
```
### Burn function
```
 function burn (address _address,uint amount) public {
        if (balances[_address] >= amount) {
            availableAmount -= amount;
            balances[_address] -= amount;
        }
```
## Code 
```
contract ImprovedToken {

    // public variables here
    string public tokenName = "Token Balance";
    string public  tokenAbbrv = "TB";
    uint public availableAmount = 0;

    // mapping variable here
    mapping (address => uint) public balances;

    // mint function
    function mint (address _address,uint amount) public {
        availableAmount += amount;
        balances[_address] += amount;
    }

    // burn function
    function burn (address _address,uint amount) public {
        if (balances[_address] >= amount) {
            availableAmount -= amount;
            balances[_address] -= amount;
        }
    }

}
```
## Where to run?

You can effectively compile, deploy, and manage the ImprovedToken contract by interacting with this code on "https://remix.ethereum.org/," an intuitive web platform created especially for creating and testing Ethereum smart contracts.

Moreover for detailed explantion, here's an explanatory video regarding the code, https://www.loom.com/share/5854ee8872b94f86b560c68564164959?sid=40080817-6d7b-4c12-96ee-7b296cdbaff1
kindly refer to the following link for the detailed explantion. 
## THANK YOU!



