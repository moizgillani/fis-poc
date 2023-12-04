## Payment requests using DCC

 This page would contain information specific to our support for using DCC

If the Cardholder Billing Amount is in a currency other that U.S. Dollars

This is a four (4) step transaction process
1.  First Pass: The merchant submits  in normal fashion. Express may respond with an 
ExpressResponseCode of 7 and ExpressResponseMessage of “DCCRequested”. This means that the 
transaction did not authorize and the merchant must prompt the user to see if they want to pay in their 
native currency.
2.  Merchant Prompts Consumer: The first pass response contains 3 fields in the <Transaction> section as 
listed below that allows the Merchant to prompt the consumer with the foreign currency, foreign 
transaction amount, and the foreign exchange rate.
3. Second Pass: The merchant submits the Sale in a second pass transaction that indicates if the 
consumer opted in or opted out. The fields passed in the request for the second pass transaction are in 
the <Transaction> section as follows below. DCCRequested is 1 to opt in and 0 to opt out. Even if the 
consumer opts out, these 4 fields must be sent. If the transaction amount is adjusted, the merchant is 
responsible for applying the conversion rate to calculate a new ForeignTransactionAmount.
4. The 2nd pass transaction should approve as normal.

### Currency Codes Supported By Worldpay's Multi Currency Processing (MCP) Product

| Currency | Currency Code |  Minor Units |
| --- | --- | --- |
| Australian Dollar | 0036 | 2  |
| Bahamian Dollar | 0044 | 2  |
| Bermudian Dollar | 0060 | 2 |
| Brazilian Rea |l 0986 | 2 |
| Canadian Dollar | 0124 | 2 |
| Chinese Yuan | 0156 | 2 |
| Danish Krone | 0208 | 2 |
| Euro | 0978 | 2 |
| Hong Kong Dollar | 0344 | 2 |
| New Israeli Shekel | 0376 | 2 |
| Japanese Yen | 0392 | 0 |
| Mexican Peso | 0484 | 2 |
| New Zealand Dollar | 0554 | 2 |
| Norwegian Krone | 0578 | 2 |
| British Pound Sterling | 0826 | 2 |
| Singapore Dollar | 0702 | 2 |
| South African Rand | 0710 | 2 |
| South Korean Won | 0410 | 0 |
| Swedish Krona | 0752 | 2 |
| Swiss Franc | 0756 | 2 |
| New Taiwan Dollar | 0901 | 2 |