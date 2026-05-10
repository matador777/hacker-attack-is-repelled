# hacker-attack-is-repelled 
Safety above all
joint efforts
pragma solidity ^0.8.0;

contract BaseSimpleNFT {

    string public name = "Base Simple NFT";
    string public symbol = "BSNFT";

    uint256 public totalSupply;
    uint256 public constant MAX_SUPPLY = 1000;

    mapping(uint256 => address) public ownerOf;
    mapping(address => uint256) public balanceOf;

    event Transfer(address indexed from, address indexed to, uint256 indexed tokenId);

    function mint() external {
        require(totalSupply < MAX_SUPPLY, "Max supply reached");

        totalSupply += 1;
        ownerOf[totalSupply] = msg.sender;
        balanceOf[msg.sender] += 1;

        emit Transfer(address(0), msg.sender, totalSupply);
    }
}
Start earning today, don't waste your time
Builder Network
