# [Machine Test] - Flutter Mobile App Developer

As a Flutter Developer, we will expect you to be able to make mobile applications with backend integration to our rest API. Once created, we want them deployed on the Android Play Store and Apple App Store.
## UI Designs

You can use the attached PDF as a reference for creating the UI in Flutter. We can provide you with an XD file on Demand if needed. 

[Application-Designs.pdf](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1f934460-593e-4ae1-9ab0-cffe700bbc79/Application-Designs.pdf)

## Rest API’s

You can check out the API documentation for integration. 

[Flutter Task Collection](https://documenter.getpostman.com/view/25104166/2sA3QmEvCV)

#POST
 SplashScreen- Device Info

curl --location 'http://devapiv4.dealsdray.com/api/v2/user/device/add' \
--data '{
    "deviceType": "andriod",
    "deviceId": "C6179909526098",
    "deviceName": "Samsung-MT200",
    "deviceOSVersion": "2.3.6",
    "deviceIPAddress": "11.433.445.66",
    "lat": 9.9312,
    "long": 76.2673,
    "buyer_gcmid": "",
    "buyer_pemid": "",
    "app": {
        "version": "1.20.5",
        "installTimeStamp": "2022-02-10T12:33:30.696Z",
        "uninstallTimeStamp": "2022-02-10T12:33:30.696Z",
        "downloadTimeStamp": "2022-02-10T12:33:30.696Z"
    }
}'

#Response
{
    "status": 1,
    "data": {
        "message": "Successfully Added",
        "deviceId": "66863a325120b12d7e181fdf"
    }
}

#POST
Login Screen- Otp and Resend

curl --location 'http://devapiv4.dealsdray.com/api/v2/user/otp' \
--data '{
    "mobileNumber":"9011470243",
    "deviceId":"62b341aeb0ab5ebe28a758a3"
}'

#POST
Otp Screen- Otp verfication
curl
curl --location 'http://devapiv4.dealsdray.com/api/v2/user/otp/verification' \
--data '{
    "otp":"9879",
    "deviceId":"62b43472c84bb6dac82e0504",
    "userId":"62b43547c84bb6dac82e0525"
}'

#POST
Register Screen- Email with referral
curl
curl --location 'http://devapiv4.dealsdray.com/api/v2/user/email/referral' \
--data-raw '{
    "email":"muhammedrafnasvk@gmail.com",
    "password":"1234Rafnas",
    "referralCode":12345678,
    "userId":"62a833766ec5dafd6780fc85"
}'

#GET
Home Screen - fetch products
curl
curl --location 'http://devapiv4.dealsdray.com/api/v2/user/home/withoutPrice'
