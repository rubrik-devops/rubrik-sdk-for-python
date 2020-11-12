# get_accounts_azure

Retrieves Azure account information from Polaris

```py
def get_accounts_azure(self, filter=""):
```

## Arguments

| Name        | Type | Description                                                                 | Choices |
|-------------|------|-----------------------------------------------------------------------------|---------|
| filter  | str | Search string to filter results |  |


## Returns

| Type | Return Value                                                                                  |
|------|-----------------------------------------------------------------------------------------------|
| list | List of Azure accounts in Polaris |



## Example

```py
from rubrik_polaris import PolarisClient


domain = 'my-company'
username = 'john.doe@example.com'
password = 's3cr3tP_a55w0R)'


client = PolarisClient(domain, username, password, insecure=True)

aws_accounts = client.get_accounts_azure("staging")

```