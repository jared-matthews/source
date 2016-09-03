
DigitalRS Development Tree

DigitalRS is a fast & reliable PoS-based cryptocurrency.

Development process
===================

Developers work in their own trees, then submit pull requests when
they think their feature or bug fix is ready.

The patch will be accepted if there is broad consensus that it is a
good thing.  Developers should expect to rework and resubmit patches
if they don't match the project's coding conventions (see coding.txt)
or are controversial.

The master branch is regularly built and tested, but is not guaranteed
to be completely stable. Tags are regularly created to indicate new
stable release versions of DigitalRS. Additional checkpoints are 
updated regularly.

Feature branches are created when there are major new features being
worked on by several people.

From time to time a pull request will become outdated. If this occurs, and
the pull is no longer automatically mergeable; a comment on the pull will
be used to issue a warning of closure. The pull will be closed 15 days
after the warning if action is not taken by the author. Pull requests closed
in this manner will have their corresponding issue labeled 'stagnant'.

Issues with no commits will be given a similar warning, and closed after
15 days from their last activity. Issues closed in this manner will be 
labeled 'stale'.

Specifications
==============

Algorithm: Scrypt <br />
Type: PoS <br />
Coin Name: DigitalRs (Short for Digital Rupees) <br />
Coin Ticker: DRS <br />
Address Letter: D <br />
RPC Port: 58786 <br />
P2P Port:  58787 <br />
PoS Percentage: 8% Per Year <br />
Last PoW Block Was: 1000 <br />
Intentional Blocks Staked During Premine: 5 (To reduce the staking amount going above 500M)<br />
Coinbase Maturity: 20 blocks <br />
Block Time: 90 seconds <br />
Target Timespan: 1 block <br />
Transaction Confirmations: 6 Blocks <br />
Mined Blocks Before Confimation: 20 Blocks <br />
Min Transaction Fee: 0.0001 DRS <br />
Stage Age: 5 Hours <br />

Onion Sync
==========

Windows: Download Vidalia from https://www.torproject.org/dist/vidalia-bundles/ then Tor Expert Bundle and point your wallet <br />
towards it. The reason for this is to update the latest Tor binary inside Vidalia since it is not maintained anymore. If you <br />
prefer to use the Tor Browser bundle then it will work just fine but Vidalia is resource friendly on Windows OS. <br />

Linux: do apt-get install tor and run digitalrs-qt and use local Tor proxy IP and port. <br />
It will automatically find the Onion nodes for you and if not, the exit nodes will do the job. <br />

SURICATA IPS Rules
==================

RPC and P2P rules for DRS is kept privately at http://git.cryptoedge.net:3000 <br />
They will be uploaded to release folder once integrated with the CE Open Appliance or IPFire project. <br />
Contact the main developer if you want to test the Intrusion Detection Ruleset. <br />

Tip
===

When compiling and running DigitalRs daemon on Linux, first run pauses at block 1000 during sync for 10+ minutes. <br />
If you want to make a quick sync then do digitalrsd stop and then digitalrsd start again for immediate sync. <br />
This takes time because inactive user wallets are tried several times before next block sync is initiated at 1K block. <br />
Note that this is not a bug and initial startup procedure to create a valid peers.dat file. <br />
