## ECommerce (Card Not Present)

 
Ecommerce—a term derived from “electronic commerce”—refers to the buying and selling of goods and services online. It involves a variety of online transaction types, including online shopping, electronic payments, online auctions, and more. Ecommerce has become increasingly popular in recent years, with more consumers and businesses turning to online transactions for everything from consumer goods to B2B software subscriptions.

### Ecommerce payment processing: step-by-step
Ecommerce payment processing involves several parties, including the customer, the online store, the payment gateway, and the payment processor. When first laid out, the step-by-step process can seem complicated, but every part is designed to ensure that payments are authorized, approved, and settled securely and as quickly as possible.

Here’s a breakdown of the steps involved in ecommerce payment processing:

#### Customer places order
The customer browses an online store, selects the products they wish to purchase, and proceeds to check out.

#### Customer enters payment information
At checkout, the customer enters their payment information, such as credit or debit card details, into your online store.

#### Payment authorization
You send a request to **authorize** a payment
* this confirms the validity of the account and the transaction.
* it also verifies that a customer has enough funds or credit to cover the amount of the transaction.

You would typically use this endpoint:
| endpoint | description |
| --- | --- |
|[/payments/authorize]($e/Payments/authorize) | this single endpoint supports all of the payment methods (ex Card, Digital Wallet, etc that you are setup to use |

#### Payment approval / Order confirmation
If the payment information is verified and authorized, we will return an approval message and you can send a confirmation message to the customer.

#### Product Delivery
It is now safe to deliver the ordered product to the customer.

#### Capture
You want to complete the authorization and initiate funds movement for partial or the full authorized amount after goods are shipped.
You can perform a capture for the full amount if you deliver all the goods at the same time.
If you need to ship parts of the order at different times, you would issue a capture **for each shipment**.

You would typically use either of these endpoints:  
| endpoint                                                                                                                                  | description                                                                                                                              |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| [/payments/capture]($e/Payments/capture)                                                              | Using this endpoint you need to send in all information about the payment | 
| [/payments/{wpAuthorizationId}/capture]($e/Payments/referencedCapture)| Use this method if you saved the **wpPaymentId** returned in the response to the original request <br>  You only need to send in the data that has changed,  |

#### Settlement
Worldpay will **settle** by depositing the funds in your bank account.  This normally occurs within 1-3 business days after the **Capture**

#### Payment reconciliation
The online store reconciles the payment with the order and ensures that the payment matches the order amount.