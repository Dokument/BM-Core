BM-Core
=======

BM-Core is a GUI-less bitmessage client that allows developers to easily interface with the bitmessage network. 

This project consists of two primary components; bm-sync and bm-core

bm-sync performs the following actions:
- Connect to the bitmessage network using the user's preference (proxy, port, etc).
- Syncronize inventory, pubkeys, and knownnodes with the bitmessage network.
	- Checking for acceptable PoW, timestamps, etc.
- Allows a secure local connection from bm-core.

bm-core performs the following actions:
- Connect to bm-sync using the secure local connection.
- Retrieve inventory items and pubkeys from bm-sync.
- Decryptable messages are kept, all others are discarded.
	- Kept messages are stored in a database.
		- All messages can be stored decrypted or using 1 encryption key.
- Sends inventory items and pubkeys to bm-sync*
	- Messages are stored decrypted or using 1 encryption key and encrypted when being sent. 
	- Messages can be sent to a bitmessage address or pubkey.
	- Allows bm-sync to mitigate attacks by design.
- Generate multiple identities
- Subscribe to multiple addresses




More About PyBitmessage: https://github.com/Bitmessage/PyBitmessage


