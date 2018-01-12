# BlockchainHack

Created a simple blockchain application on Python from following Daniel van Flymen's tutorial:
`https://hackernoon.com/learn-blockchains-by-building-one-117428612f46`

I was able to learn a lot abot how to setup a blockchain database and how transactions are verified. I think it would be a great technology to use in a final project that involves any sort of voting or social network platform or simply as a way of securely storing information. 

Run with `FLASK_APP=blockchain.py flask run` after setting up your venv

## Endpoints:

### Mining
Mine a block by submitting a GET request to `http://localhost:5000/mine`

### Adding transactions
Add transactions by submitting a POST request to `http://localhost:5000/transactions/new` with the following JSON block

```javascript
{
    "sender": "sender-address",
    "recipient": "recipient-address",
    "amount":  "12345"
}
```
### See the blockchain
See the current blockchain by submitting a GET request to `http://localhost:5000/chain`.

A single block is represented below:

```javascript
block = {
    'index': 1,
    'timestamp': 1506057125.900785,
    'transactions': [
        {
            'sender': "8527147fe1f5426f9dd545de4b27ee00",
            'recipient': "a77f5cdfa2934df3954a5c7c7da5df1f",
            'amount': 5,
        }
    ],
    'proof': 324984774000,
    'previous_hash': "2cf24dba5fb0a30e26e83b2ac5b9e29e1b161e5c1fa7425e73043362938b9824"
}
```
## Takeaways

I found the tutorial I followed to be fairly straightforward and easy to follow, and it helped me better understand what blockchain actually is, how it works, and what Proof of Work and Consensus algorithms are. The person who made the tutorial did make a mistake in implementing his Proof of Work algorithm so I had to figure out how to fix it to incorporate previous blocks in the blockchain and I found a helpful link online here: `https://github.com/dvf/blockchain/issues/10`. 
I believe that I could incorporate a database like these fairly easily, especially for any front end application my project may require going forward. I wasn't able to get an example of the Consensus algorithm up and running since I didn't spin up another node to add transactions and blocks to the chain, but I will do this soon and continue to hack this and follow more tutorials to learn more. 