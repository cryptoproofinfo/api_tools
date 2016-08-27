# api_tools
Tools to easily interact with the cryptoproof.info api

## Docker container
### Build:
Clone the repo, add a copy of your SSL key named as `cert.key` into the folder and execute the command
`docker build --build-arg XPUBKEYS=<extended_public_keys> --build-arg SIGS=<signatories> -f Dockerfile_api_tool -t cryptoproof:api_tool .`

If you do not have an SSL key you can use a blank file in its place
`touch cert.key`

### Run:
`docker run --rm cryptoproof:api_tool <command>`

## Native
Provided you have [M2Crypto](https://pypi.python.org/pypi/M2Crypto) installed, you should be able to manually set the [xpubkeys]() and [sigs]() variables inside of [cryptoproof_api_tool.py]() and run the file natively.

### Run:
`python cryptoproof_api_tool.py <command>`

