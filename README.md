# lightarti directory

Holds the latest directory files for [lightarti-rest](https://github.com/c4dt/lightarti-rest).
These files are updated once a day.
To use them, fetch the latest `directory-cache.tgz` file, untar it, and put the four files
into a directory.
The mobile app needs to pass the directory path to the lightarti-rest call.

## Creation of Certificates

With the 0.3 version of lightarti-rest, the certificate needs to be passed along.
To create the `secrets.AUTHORITY` that is needed for the script to run correctly,
run the following in `lightarti-rest/tools`:

```
DIR_AUTH_PASSWORD=very_secret_password make secrets_authority
```

This will print out a Base64-encoded string that you'll need to copy into the
`AUTHORITY` secret in the `lightarti-directory` repository.
You will also have to copy the `DIR_AUTH_PASSWORD` into the `DIR_AUTH_PASSWORD`
secret in the `lightarti-directory` repository.
