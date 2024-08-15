# lightarti directory - ARCHIVED

This project has been archived by the [C4DT](https://c4dt.epfl.ch) Factory team.
It is kept here for reference and for old URLs.
You can find more information in our [showcase](https://factory.c4dt.org/showcase/lightarti/presentation)
and find our contact information.

## Description

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

# Contributors

`lightarti-directory` is maintained by the [Center for Digital Trust](https://c4dt.org/). The following people contributed to the implementation of `lightarti-rest`:

- Linus Gasser, C4DT
- Valérian Rousset, C4DT
- Christian Grigis, C4DT
- Laurent Girod, SPRING Lab, EPFL

Analysis and design by:

- Wouter Lueks, SPRING Lab, EPFL
- Carmela Troncoso, SPRING Lab, EPFL
