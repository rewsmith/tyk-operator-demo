curl -X POST -H "x-tyk-authorization: CHANGEME" \
-s \
-H "Content-Type: application/json" \
-X POST \
-d '{
"rate": 5,
"per": 60,
"expires": -1,
"quota_max": -1,
"org_id": "default",
"quota_renews": 1449051461,
"quota_remaining": -1,
"quota_renewal_rate": 60,
"access_rights": {
"httpbin": {
"api_id": "httpbin",
"api_name": "httpbin",
"versions": ["Default"]
}
},
"meta_data": {}
}' http://localhost:8080/tyk/keys/create | python -mjson.tool