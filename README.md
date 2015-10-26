# s3get

[![wercker status](https://app.wercker.com/status/fc5024866777cab943474d3c6ad246d8/m "wercker status")](https://app.wercker.com/project/bykey/fc5024866777cab943474d3c6ad246d8)

Forked from wercker/s3cmd and adjusted for s3cmd get

It is recommended that you use application and deployment variables in wercker, so you don't include any private keys in your code.

# Options

* `key-id` (required) The Amazon Access key that will be used for authorization.
* `key-secret` (required) The Amazon Access secret that will be used for authorization.
* `bucket-url` (required) The url of the bucket to sync to, like: `s3://wercker.com`, where `wercker.com` is the bucket name.
* `source-dir` (optional, default: `./`) The directory to sync to the remote bucket.
* `delete-removed` (optional, default: `true`) Add `--delete-remove` flag if this is `true`.
* `opts` (optional, default: `--acl-public`) Arbitrary options provided to s3cmd. See `s3cmd --help` for more.

# Example

```
deploy:
    steps:
        - s3get:
            key-id: $KEY
            key-secret: $SECRET
            bucket-url: $BUCKET
            source-dir: $SOURCE
```

# License

The MIT License (MIT)

# Changelog

## 1.0

- Initial Release

