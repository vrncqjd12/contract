pragma solidity 0.8.18;

contract MyToken {

  // Public variables

  string public name = "MyToken";
  string public symbol = "MTK";
  uint256 public totalSupply = 0;

  // Mapping of addresses to balances

  mapping(address => uint256) public balances;

  // Mint function

  function mint(address recipient, uint256 amount) public {
    require(amount > 0, "Amount must be greater than 0");
    totalSupply += amount;
    balances[recipient] += amount;
  }

  // Burn function

  function burn(address sender, uint256 amount) public {
    require(amount > 0, "Amount must be greater than 0");
    require(balances[sender] >= amount, "Not enough balance");
    totalSupply -= amount;
    balances[sender] -= amount;
  }
}
