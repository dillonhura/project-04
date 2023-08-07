# How to
1. Create python virtual environment `python3 -m venv env`
2. Install the requirements.txt `python3 -m pip install -r requirements.txt`
3. Initialize DBT project `dbt init`. Identifier account should be : `<orgname>-<account_name>`
4. Choose keypair auth for more secure way to authenticate
5. Generate key pair and setup public key for specific user in Snowflake https://docs.snowflake.com/en/user-guide/key-pair-auth
6. Run your first model `dbt run -s my_first_dbt_model`

# Hardening profiles.yml
1. Open the profiles.yml
2. For the confidentials params/keys replace the value with `"{{ env_var('VAR_NAME') }}"`
3. Run Command `EXPORT VAR_NAME=<confidential_value>`
