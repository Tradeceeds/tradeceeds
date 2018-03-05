
# Tradeceeds API (Beta)
Our transfer request service allows you to transfer qualified bitshares assets (listed below) to other blockchains.

| Bitshares Asset |Blockchain  | Keyword on memo
|--|--|--|
| BTCCORE |Bitcoin  | btccx
| ETHERIA|Ethereum| ethcx

This preliminary release is on beta version. Please report [**Issues**](https://github.com/Tradeceeds/tradeceeds/issues) immediately.

## Request Bitcoin Address to link to a Bitshares Account Name

Input via POST

Variable | Description
------------ | -------------
apikey | Your API Key
btsacct| Bitshares Account Name
callbackurl | Where to post results

Send POST request to https://tradeceeds.com/bitcoin/

Output

Variable | Description
------------ | -------------
success | Status of request
btcaddr | Bitcoin Address linked to your Bitshares Address
btsacct| Bitshares Account Name

**NOTICE TO BTCCORE OWNERS**

*Once you have received your bitcoin address, initialize it by depositing **at least 0.01 BTC**. Each address or bitshares account is qualified to make a transfer request from a minimum of 0.00001 up to 3 times the total amount received by the linked bitcoin address. Do not request if you have never funded your account.*

## Transfer Request

Input via POST request

Variable | Description
------------ | -------------
apikey | Your API Key
rate | Bitcoin Rate
from | Bitshares Account Name
blockno | Block Number
transid | Transaction ID
recipient | Bitshares Account Name of Recipient
memo | Memo containing keyword
callbackurl | Where to send the status of this request
amount | Amount being transferred
asset | Bitshares Asset
sandbox | default value: true. Please set to false for real-time processing

Send POST request to https://tradeceeds.com/api/

Output

Variable | Description
------------ | -------------
success | Provides information whether your request was successfully processed
trxhash | Transaction Hash of your Bitcoin Transfer
sandbox | Sandbox status
transid | Related Transaction ID on the Bitshares Blockchain

Please report [**Issues**](https://github.com/Tradeceeds/tradeceeds/issues) immediately.
