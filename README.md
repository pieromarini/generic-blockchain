# Generic Blockchain

* Written in Python
* Flask web server (Development Only)
* Adds Blocks
* Adds Transactions
* The only valid chain is the longest one. (Auto resolves conflicts)
* Proof Of Work -> Find a number 'p' such that when hashed with the previous block's hash solution, it has 4 leading 0's


### API Endpoints

* /nodes/register
* /nodes/resolve
* /mine
* /transactions/new
* /chain

```bash
# Mine a new Block
curl http://0.0.0.0:5000/mine

# Visualize the chain
curl http://0.0.0.0:5000/chain

curl -X POST -H "Content-Type: application/json" "http://0.0.0.0:5000/transactions/new" -d '{ "sender": "ADDRESS", "recipient": "OTHER-ADDRESS", "amount": 2 }' 

```
