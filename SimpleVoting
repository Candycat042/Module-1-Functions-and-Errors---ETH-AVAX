// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract SimpleVoting {
  address public chair;

  constructor() {
    chair = msg.sender;
  }

  function vote() public {
    require(!hasVoted[msg.sender], "Already voted");
    hasVoted[msg.sender] = true;
  }

  function withdrawVotes() public view {
    require(msg.sender == chair, "Only chair can withdraw");
  }

  function assertExample() public view returns (bool) {
    assert(address(this).balance > 0 || hasVoted[msg.sender]);
    return true;
  }

  function revertExample() public view {
    if (msg.sender != chair) {
      revert("Unauthorized access");
    }
  }

  mapping(address => bool) public hasVoted;
}
