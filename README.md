# UrlShortener
URL Shortener is used to create short URLs that can be easily shared, tweeted, or emailed to friends whcic is built using Google Cloud functions, Cloud hosting and firestore

You Can check the UI Here

> Web UI written in Vue.Js [PonnamKarthik/Url-Shortener-UI](https://github.com/PonnamKarthik/Url-Shortener-UI)


> Android App written in Java [PonnamKarthik/Url-Shortener-Android-App](https://github.com/PonnamKarthik/Url-Shortener-Android-App)



# API endpoints

## */data*

Endpont returns all short links added by particular user

> example url

> **/data?uid=[USER_ID]**

```json
[
    {
        "code": "code1",
        "views": 0,
        "url": "url1",
        "uid": "USER_ID"
    },
    {
        "code": "code2",
        "views": 0,
        "url": "url2",
        "uid": "USER_ID"
    }
]
```

## */add*

Endpont returns all short links added by particular user

> example url

> **/add?uid=[USER_ID]&auto=[true|false]&code=[UNIQUE_CODE]&url=[URL]**

Query | Description
------------ | -------------
uid | unique user id
code | unique short link code (Optional)
url | link to short
auto | to generate unique code automatically [true|false]


```json
{
    "error": "[true/false]",
    "msg": "[Success / Failure]",
    "short_url": "[short url if no error]"
}
```


## */delete*

Endpont returns all short links added by particular user

> example url

> **/delete?uid=[USER_ID]&code=[UNIQUE_CODE]**

Query | Description
------------ | -------------
uid | unique user id
code | unique short link code 


```json
{
    "error": "[true/false]",
    "msg": "[Success / Failure]"
}
```

## */:code*

> Short Url


## Demo UI for this Project

> [PonnamKarthik/Url-Shortener-UI](https://github.com/PonnamKarthik/Url-Shortener-UI)

## Note

> This repo contains demo ui in public folder 