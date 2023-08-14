# Web store order processor example robot

Swag order robot. Places orders at https://www.saucedemo.com/ by processing a
spreadsheet of orders and ordering the specified products using browser
automation. Uses local or Control Room's Vault for credentials.

## Configure local vault (not recommended)

See https://robocorp.com/docs/development-guide/variables-and-secrets/vault

Paste this content in the vault file:

```json
{
  "swaglabs": {
    "username": "standard_user",
    "password": "secret_sauce"
  }
}
```

In [*devdata/env-local.json*](./devdata/env-local.json), edit the `RPA_SECRET_FILE`
variable to point to your *vault.json* file on your filesystem. On macOS / Linux,
use normal file paths (e.g.: `"/Users/<username>/vault.json"` or
`"/home/<username>/vault.json"`). On Windows, you need to escape the path:
`"C:\\Users\\User\\vault.json"`.

> Make sure you rename the *env-local.json* file into *env.json* if you want it picked
automatically by VSCode when the extension is not connected to the cloud, otherwise
the extension will be able to pick them up from Control Room's online Vault if
connected to the Workspace.

### Control Room's online Vault (recommended)

Configure your Vault using the UI. The name of the vault should be `swaglabs`.
Provide the user name and the password as key-value pairs (see the vault file
for the exact naming).
