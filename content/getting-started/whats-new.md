## Changelog

WorldPay is committed to continually improve our products and add new features to our platform. 

When we introduce changes to our APIs, we make every effort **not** to impact our existing integrations. 

For example, for our REST APIs, we follow the API expand-contract pattern to add new elements without changing the version.

While we strive to reduce impact to existing integrations, we sometimes have to introduce changes that are not compatible with existing API versions. Doing so enables us to keep our APIs consistent and to improve the quality and developer experience.



| Version | Date | Description  |
| --- | --- | --- |
| x.x.y  |  1.Dec.2023 | - Renamed 3ds to ThreeDS <br> - added emvResponseData to AuthorizePaymentResponse <br> - in POSCardPaymentEntryMethodEmv renamed track2Data to track2EquivalentData |
| x.x.y  |  30.Nov.2023 | TBD |
| x.x.y  |  27.Nov.2023 | Changed path for recurring payments endpoints <br> from: /recurringPaymentsMgmt<br> to: /payments/recurring |
| x.x.y  |  25.Nov.2023 | Implemented System Endpoint group  <br> /ping <br> /healthCheck|
| x.x.y  |  22.Nov.2023 | Renamed GiftCardMerchant  to BasicMerchant  <br> corrected payload of QuerySchedule endpoint |
| x.x.y  |  21.Nov.2023 | Comp Impl of Gift Card Mgmt endpints and payloads  <br> addl work on Recurring Pymt Mgmt endpoints (Express Only)|
| x.x.y  |  20.Nov.2023 | Rename all enhanced data objects from *Data to *EnhancedData <br> completed impl of FleetEnhancedData <br> addl impl of queryAvailableBalance for HealthCare <br> Initial Rough-in of Recurring Payments Endpoints (Express Only)|
| x.x.y  |  16.Nov.2023 |  Initial Rough-in of Gift Card Mgmt Endpoints <br>  Initial Rough-in of Fleet Enhanced Data  |
| x.x.y  |  15.Nov.2023 |  Completed adding support for BNPLs <br>  renamed softDeclineAddlInfo to  additionalProductData <br> removed InitiateSession endpoint |
| x.x.y  |  11.Nov.2023 |  Initial Rough-in of BNPL support <br>  removed wpAuthorizationId   <br>   Initial Rough-in of Balance Inquiry endpoint |
| x.x.y  |  7.Nov.2023 |  Added response Header: X-Idempotent-Response  |
| x.x.y  |  27.Oct.2023 | wpPaymentId format chaned from Guid to NanoId  <br> added multiple request examples |

Talk about x,x vs x.x.x versioning

Talk about version in request URL
Talk about version in response header

Talk about breaking vs non-breaking changes....