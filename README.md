# honeypot
Reentrancy Attack on a Smart Contract This document describes the exercise assignments for the "Blockchain development" course @ Kingsland University. In this lesson we learned the basics of Solidity programming language. The goal of this exercise is to get practical skills in writing simple smart contracts in Solidity, publishing and testing contracts in the Remix IDE.

Got it to compile for version 0.4.26+commit.4563c3fc

HoneyPot get() function sends ether to the address that called it only if this contract has any ether as balance. When HoneyPot sends ether to HoneyPotCollect the fallback function is triggered. If the HoneyPot balance is more than the value that it was sent to, the fallback function calls get() function once again and the cycle repeats.
Recall that within the get() function the code that sets the balance to zero comes only after sending the transaction. This tricks the HoneyPot contract into sending money to the HoneyPotCollect address repeatedly until HoneyPot is depleted of almost all its ether.
What to Submit?
Create a zip file (e.g. your-username-honeypotcollect-attack.zip) with the source code and an image with an address with at least 100+ ethers.


Unfortunately this contract will not deploy for any value over 0.  I am moving on.