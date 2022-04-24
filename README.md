# sample
sample

## GetAccountInfoAsync
Retrieves information about a state of account corresponding to `accountAddress` and `blockHash`. 

```csharp
public async Task<AccountInfo?> GetAccountInfoAsync(string accountAddress, string blockHash);
```

**Input:**

- `accountAddress`: A null-terminated base58 encoding (same format as returned by [GetAccountList](https://www.nuget.org/packages/StyleCop.Analyzers/)) of an account address. 
- `blockHash`: A null-terminated base16 encoding of a block hash. 


**Output:**

- The [AccountInfo](https://www.nuget.org/packages/StyleCop.Analyzers/) object containing information about a state of account. Returns `null` if the account was not found.

### Code Sample
```csharp
string accountAddress = "3sAHwfehRNEnXk28W7A3XB3GzyBiuQkXLNRmDwDGPUe8JsoAcU";
string blockHash = "6b01f2043d5621192480f4223644ef659dd5cda1e54a78fc64ad642587c73def";
AccountInfo accountInfo = await client.GetAccountInfoAsync(accountAddress, blockHash);
```
