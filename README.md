# TAMCoin
  This is a Solidity program that creates a token with the functionality of minting and burning

## Description
  TAMCoin is a new token designed specifically to transact inside FEU. This program is a simple contract written in Solidity, a language used for smart contracts on the Etherium blockchain. This simple program shows the minting and burning mechanics of a token.

### Executing the program

  To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

  Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., ethProj.sol). Copy and paste the following code into the file:
```
  contract MyToken {
    string public coinName = "TAMCoin";
    string public coinAbrv = "TCN";
    uint public totalCoin = 0;
    mapping(address => uint) public coinBal;
    // mint function
    function coinMint (address _address, uint _val) public {
        totalCoin += _val;
        coinBal[_address] += _val;
    }
    // burn function
    function coinBurn (address _address, uint _val) public {
        if (coinBal[_address] >= _val){
        totalCoin -= _val;
        coinBal[_address] -= _val;
        }   
    }
}
```
