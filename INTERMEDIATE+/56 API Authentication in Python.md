
---

### API Authentication in Python

- Many APIs require authentication to ensure secure access to their resources. This is typically done using tokens, keys, or OAuth (Open Authorization) protocols.

---

### Basic Authentication

- Basic Authentication involves sending a username and password with each request.
- It's less secure compared to other methods and is not recommended for sensitive data.

Example using `requests` library:

```python
import requests

url = 'https://api.example.com/endpoint'
auth = ('username', 'password')

response = requests.get(url, auth=auth)

if response.status_code == 200:
    data = response.json()
    print(data)
else:
    print(f'Error: {response.status_code}')
```

---

### API Keys

- API keys are unique identifiers provided by the API provider to authenticate requests.
- They are typically included in the request headers.

Example using `requests` library:

```python
import requests

url = 'https://api.example.com/endpoint'
headers = {'API-Key': 'YOUR_API_KEY'}

response = requests.get(url, headers=headers)

if response.status_code == 200:
    data = response.json()
    print(data)
else:
    print(f'Error: {response.status_code}')
```

---

### OAuth (Open Authorization)

- OAuth is a more secure method for third-party authentication.
- It allows applications to access resources on behalf of a user without exposing their credentials.

Example using `requests-oauthlib` library (OAuth2):

```python
from requests_oauthlib import OAuth2Session

# Set up OAuth2 session
client_id = 'YOUR_CLIENT_ID'
client_secret = 'YOUR_CLIENT_SECRET'
redirect_uri = 'https://your_redirect_uri.com'
scope = ['scope1', 'scope2']

oauth = OAuth2Session(client_id, redirect_uri=redirect_uri, scope=scope)
authorization_url, state = oauth.authorization_url('https://api.example.com/oauth/authorize')

# User authorizes the application and is redirected to redirect_uri

token_url = 'https://api.example.com/oauth/token'
oauth.fetch_token(token_url, authorization_response='https://your_redirect_uri.com?code=CODE')

# Access protected resources
response = oauth.get('https://api.example.com/protected/endpoint')

if response.status_code == 200:
    data = response.json()
    print(data)
else:
    print(f'Error: {response.status_code}')
```

---

### Note:

- Always keep sensitive information like usernames, passwords, and API keys secure.
- Use HTTPS for secure communication with the API server.

---
---
