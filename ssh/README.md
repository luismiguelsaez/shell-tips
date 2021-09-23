# SSH tips

## Authentication

### From Hashicorp Vault
```
vault login -method=oidc -path=google
ssh -i <(vault kv get -field=priv kv/internal/aws/ssh_keys/dev/Platform) < user_name >@< server_ip >
```
