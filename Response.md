
# API Response Syntax
#### The API will respond to requests in one of two forms: An ERROR or an OK.
####  Responses will always be in plain text format, with the MIME type `text/plain`. Here are two example responses:

```
OK
200
UUIDBAL
849
```
#### The above is an example of a successful request for getting the balance of a Discord user UUID (Developer's ID). `OK` and `ERROR` responses will always have four lines. The first is the success indicator line, which states `OK` for success. The second is the HTTP response code sent to the client, which is always `200` for a successful response. The third is the request type, for example getting a UUID's balance `UUIDBAL`. The fourth and final line is additional information related to your request, in this case the UUID's balance is `849` which means β849 (In case you are not already aware, the currency is called Boops, denoted by β)
#### Here is another request which was successful, transferring currency from a wallet to a UUID, and you will notice there are no additional details required so they are nullified:
```
OK
200
WALLETTOUUID
NULL
```
#### Now for an `ERROR` example. In this case we are doing another transfer of currency from a wallet to a UUID:
```
ERROR
400
WALLETTOUUID
Wallet not found
```
