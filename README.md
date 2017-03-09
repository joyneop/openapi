# zaoshu SpinnyWeaver Open API 

*WARNING: This version is for demonstration and not production-ready, and so is this documentation, which is only for early access developers.*

*If you want to fetch and parse some open website pages, but don't know nothing about web-spider-programming, We'd love to introduce our WebUI Beta version at [zaoshu.io](https://zaoshu.io) to you, give it a try!*

## V1 (alpha)

### Access Endpoint: 

    scheme: https 
    host: openapi.zaoshu.io
    entry: /v1

### Access Key

To get authorized, compose the query path as `/v1/u_${YOUR_ACCESS_KEY}/`, for example:

    https://openapi.zaoshu.io/v1/u_9083adfb6d50484b8c2ee3c504012def

You can retrieve your access key in the `Developer Features` card at [`Settings`](http://dashboard.zaoshu.io/?settings)

### The one and the only API for now

#### Fetch latest result instance

    entry: /v1/u_${ACCESS_KEY}/instance_${INSTANCE_ID}/downloadLatest/${CONTENT_TYPE}

* ${INSTANCE_ID}: 
    * Description: You can get your instance ID at the bottom of your instance detail page
    * VarType: String
* ${CONTENT_TYPE}: 
    * Description: The file type of your result
    * Options: csv/xls/json/xml
    * VarType: String

Example:

    https://openapi.zaoshu.io/v1/ \
        u_9083adfb6d50484b8c2ee3c504012def/ \ 
        instance_77c35ed148134a67b091deb258efeade/ \
        downloadLatest/json

*NOTICE: If the instance is running with `Deep Crawling` feature on, the result file format will be `zip`, and the package contains files with specific file type*
        

