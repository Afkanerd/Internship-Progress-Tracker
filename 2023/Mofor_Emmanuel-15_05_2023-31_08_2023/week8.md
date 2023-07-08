## Week 8: July 3 - July 7

### What I worked on

It's my second month already, and this week was focused on researching on platforms and commencing the implementation of their auth methods and integration.

I did the following this week:

- Researched on platforms that fit aptly into the SWOB ecosystem
- Performed criteria-based selection of platforms
- Carried out statistical analysis of platforms (Yahoo and Discord)
- Implemented the Yahoo OAuth protocol

### What I learned

Through completing these tasks, I learned the following:

- Discord and Yahoo are still in active service
- Yahoo OAuth2 flow

### Challenges I faced

- **Deciding what package to use for Yahoo auth:** After preliminary research on the Yahoo OAuth2 flow, it was bewildering when it came down to what packages and libraries to use, given there were several options to choose from.

- **Implementing Yahoo token revocation:** Throughout the Yahoo OAuth2 flow, various use cases such  as authorization, validation and token refreshing are available, except token invalidation.
I succeeded to get a revoke_url after research, but tried the following means to invalidate a token, to no avail, always ending with an `"Invalid header authorization"` error, though I did set my headers appropriately. I tried the following auth types:
  - Basic authentication
  - Bearer authentication
  - Base64 authorization by encoding of client_id and client_secret

None worked. I even used the plain `requests` package, as well as the `requests_oauthlib` package.

### How I overcame them

- **Deciding what package to use for Yahoo auth:** The packages I tried were:
  - `requests`
  - `requests_oauthlib`

I did combine both, like so:

```python
from oauthlib.oauth2 import BackendApplicationClient
from requests_oauthlib import OAuth2Session

class Methods:
    def __init__(self, origin: str) -> None:
      self.client_id = "my-client-id"
      self.yahoo = OAuth2Session(
            client=BackendApplicationClient(client_id=self.client_id)
        )

```

But kept failing, as such, resorted to using just requests_oauthlib, which has been working well so far.

- **Implementing Yahoo token revocation:** I will get to my mentor about this, and if all else fails, one tweak I have in mind is to refresh the existing access_token and dump it.

### Next steps

Moving forward,

- I plan on completing the implementation of the Yahoo platform integration
