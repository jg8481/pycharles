# pycharles

## Install Requirements:

Run the following to install the requirements.
```
git clone https://github.com/jg8481/pycharles.git
cd pycharles/
pip3 install -r ./requirements.txt
```

## Usage:

1. Open your desired charles session.
2. Select `File > Export Session`
3. Export as a JSON session file

```
> from pycharles.session import CharlesSession
> from pycharles.request import CharlesRequest

> session = CharlesSession(path=PATH)
> session.requests_count()  # return number of requests in the session file
> charles_request = session.query_request_with_index(n)  # return the nth request object in the file, starting from 0
> charles_request.set_header('User-Agent', 'Nokia')  # set header
> session.query_requests_with_properties({'method': 'GET', 'response.status': 200})  # query all successful GET requests in the session
> charles_request.execute()  # execute a request
```

License
-------
MIT
