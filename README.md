A client library for the bitcoin exchange OCX
---

# Install
```
pip install ocx_client
```

# Usage
- Rest API Client: https://github.com/ocxapi/ocx-openapi-python-client/blob/master/client_sample.py
- Streaming API Client: https://github.com/ocxapi/ocx-openapi-python-client/blob/master/streaming_client_sample.py

# Example

## Public API and Private API

~~~python
from ocx_client import Client

# access public apis
public_client = Client()

print(public_client.get_public("/api/v2/markets.json"))
print(public_client.get_public("/api/v2/depth.json", params={"market_code": "btccny"}))



# access secret apis
private_client = Client(access_key="your access key",secret_key="your secret key")

print(private_client.get("/api/v2/members/me.json"))
~~~

# Licence
LGPL
