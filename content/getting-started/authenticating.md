## How to Authenticate to the API?

# 📝Authentication

Each request to the API must include two (2) important data elements:

*  [ ] An **APIKey** value in the **X-API-KEY** HTTP header.
*  [ ] The **merchantId** that is included in the **merchantData** section in the payload.

You can use [these instructions](page:getting-started/how-to-get-a-test-account) to setup a test account and [these instructions](page:getting-started/go-live-checklist) to prepare to go live.  

*Note: Your production API-Key and merchantId will be different than the ones you use for testing.*


![auth header](https://res.cloudinary.com/apimatic/image/upload/v1701097840/63ad9a7735191778f8a5d33c/63ad9a7735191778f8a5d33c--auth%20header.png)

Hint: To use the **Try It Out** button in the portal, you enter your **APIKEY** by clicking on the **Configure** button