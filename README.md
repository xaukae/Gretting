# Gretting
// SPDX-License-Identifier: GPL-3.0

pragma solidity >=0.7.0 <0.9.0;

contract Greeting {
    string public name; 
    string public greetingPrefix = "Hello ";
     constructor(string memory initialName) {
          name = initialName;
     }
     function setName(string memory newName) public {
         name = newName;
     }

     function getGreeting() public view returns (string memory) {
         return string(abi.encodePacked(greetingPrefix, name));
     } 
}
