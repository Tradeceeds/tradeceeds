# Tradeceeds API

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


## Transfer Request

Inputs via POST request

Variable | Description
------------ | -------------
apikey | Your API Key
rate | Bitcoin Rate
from | Bitshares Account Name
transid | Transaction ID
recipient | Bitshares Account Name of Recipient
memo | Memo containing keyword
callbackurl | Where to send the status of this request
amount | Amount being transferred
asset | Bitshares Asset
blockno | Block Number
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
