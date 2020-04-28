# Mesh-PayTMGateway
===================
Android simple e-commerce with PayTM payment gateway integrated.

Backend REST API
===================
This app uses the REST API built in Laravel to list down the products, manage orders and handling PayTM payment transactions.

Refer the [Laravel PayTM](https://github.com/ravi8x/Laravel-PayTM-Server) project to know the REST API used for this project.

Changing the REST endpoint
===================
Currenlty this repo uses the demo REST API provided. You can build the backend project and change the base url in **app/build.gradle** file.
```gradle
productFlavors {
        dev {
            buildConfigField "String", "BASE_URL", "\"https://demo.androidhive.info/paytm/public/api/\""
            buildConfigField "String", "PAYTM_CALLBACK_URL", "\"https://securegw-stage.paytm.in/theia/paytmCallback?ORDER_ID=%s\""
            buildConfigField "boolean", "IS_PATM_STAGIN", "true"
        }

        prod {
            buildConfigField "String", "BASE_URL", "\"https://demo.androidhive.info/paytm/public/api/\""
            buildConfigField "String", "PAYTM_CALLBACK_URL", "\"https://securegw.paytm.in/theia/paytmCallback?ORDER_ID=%s\""
            buildConfigField "boolean", "IS_PATM_STAGIN", "false"
        }
    }
```
