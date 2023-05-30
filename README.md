# ETH
ETH Smart conteact
pragma solidity ^0.8.0;

contract XXXToken {
    string public constant name = "XXX";
    string public constant symbol = "XXX";
    uint256 public constant totalSupply = 888 * (10 ** 18); // 888 tokens with 18 decimal places

    mapping(address => uint256) public balances;

    constructor() {
        balances[msg.sender] = totalSupply;
    }

    function balanceOf(address account) public view returns (uint256) {
        return balances[account];
    }
}
