# api


How to use CriptoHub API
1. Register new user.

2. Authentication for registered user:
curl -X POST   https://system.criptohub.com.br/gateway/public/authenticate -H "Content-Type: application/json" -d '{"username": "123qwer@mailinator.com", "password": "123qwer", "stayLoggedIn": false}' -i

3. You will receive response with Set-Cookie: header. Put this content as a Cookie header with any request to private context:
curl -X GET   https://system.criptohub.com.br/gateway/private/settings  -H 'Cookie: Auth-Token=31f24f0023e91508RwJqJMQs_WZmxdKt2sxO4LkCYN86VFptH58oWjmkfT4wJVnWSVVQ_KMIEaPuIdt5K_kaj8d7HZ2yvCLxUJsXTQwnrGyfTN2Y8C4ePCgeqxbcvI1fzRuj2RMyNOmVYdR7QG1n4te2eJ7AQIFaQGSGjQ..' -i (edited)

4. Also, keep in mind, please, that if your guys are using curl for API access ask them not to forget overwriting:
default -d Content-Type: application/x-www-form-urlencoded header with "Content-Type: application/json" for each POST request (edited).
