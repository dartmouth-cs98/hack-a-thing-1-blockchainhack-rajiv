# BlockchainHack

Created a simple blockchain application on Python from following Daniel van Flymen's tutorial
https://hackernoon.com/learn-blockchains-by-building-one-117428612f46

Run with 'FLASK_APP=blockchain.py flask run'

Endpoints:

## Mining
Mine a block by submitting a GET request to `http://localhost:5000/mine`

## Adding transactions
Add transactions by submitting a POST request to `http://localhost:5000/transactions/new` with the following JSON block

```javascript
{
    "sender": "sender-address",
    "recipient": "recipient-address",
    "amount":  "12345"
}
```
## See the blockchain
See the current blockchain by submitting a GET request to `http://localhost:5000/chain`