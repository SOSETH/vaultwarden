# Vaultwarden

Tested on: Debian 11

Setup vaultwarden behind an nginx reverse proxy.

## Configuration
|Var|Default value|Description|
|---|-------------|-----------|
|vaultwarden_postgres_user|`user`|Username used to connect to Postgres|
|vaultwarden_postgres_password|`password`|Password used to connect to Postgres|
|vaultwarden_postgres_database|`database`|Database to use in Postgres|
|vaultwarden_postgres_host|`127.0.0.1`|Host to connect to for Postgres|
|vaultwarden_postgres_max_conn|`25`|Maximum number of DB connections to establish (pool size)|
|vaultwarden_smtp_user|`user`|Username for SMTP|
|vaultwarden_smtp_password|`password`|Password for SMTP|
|vaultwarden_smtp_from|`vaultwarden@example.org`|SMTP From address|
|vaultwarden_smtp_host|`127.0.0.1`|Mailserver to connect to (port 587, STARTTLS is attempted)|
|vaultwarden_smtp_from_name|`Vaultwarden`|Human-readable name for email sender|
|vaultwarden_signups_allowed|`false`|Whether signups are allowed|
|vaultwarden_signups_allowed_domains|`foo.example.org`|Which domains can signup even if signups are not allowed|
|vaultwarden_admin_token|unset|Admin token to use - the interface is only available on localhost|
|vaultwarden_support_yubico|`False`|Whether to support YubiKey's OTP service|
|vaultwarden_yubico_client_id|`Foobar`|YubiCo OTP Client ID|
|vaultwarden_yubico_secret_key|`BarBaz`|YubiCo OTP Client Secret|
|vaultwarden_rocket_workers|`10`|Number of web workers to use|
|vaultwarden_public_url|`https://foo.example.org`|Where is this instance exposed publicly|

## Dependencies
nginx (SOSETH/nginx) needs to be rolled out and provided with a valid SSL cert. Data is stored in a postgres database
that also has to be provisioned somewhere.