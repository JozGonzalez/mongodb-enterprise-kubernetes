# Security Policy

## Supported Versions

Use this section to tell people about which versions of your project are
currently being supported with security updates.

| Version | Supported          |
| ------- | ------------------ |
| 5.1.x   | :white_check_mark: |
| 5.0.x   | :x:                |
| 4.0.x   | :white_check_mark: |
| < 4.0   | :x:                |

## Reporting a Vulnerability

Use this section to tell people how to report a vulnerability.

Tell them where to go, how often they can expect to get an update on a
reported vulnerability, what to expect if the vulnerability is accepted or
declined, etc.
- name: Cache
  uses: actions/cache@v3.3.2
  with:
    # A list of files, directories, and wildcard patterns to cache and restore
    path: 
    # An explicit key for restoring and saving the cache
    key: 
    # An ordered list of keys to use for restoring stale cache if no cache hit occurred for key. Note `cache-hit` returns false in this case.
    restore-keys: # optional
    # The chunk size used to split up large files during upload, in bytes
    upload-chunk-size: # optional
    # An optional boolean when enabled, allows windows runners to save or restore caches that can be restored or saved respectively on other platforms
    enableCrossOsArchive: # optional, default is false
    # Fail the workflow if cache entry is not found
    fail-on-cache-miss: # optional, default is false
    # Check if a cache entry exists for the given input(s) (key, restore-keys) without downloading the cache
    lookup-only: # optional, default is false
  - name: Setup Go environment
  uses: actions/setup-go@v4.1.0
  with:
    # The Go version to download (if necessary) and use. Supports semver spec and ranges. Be sure to enclose this option in single quotation marks.
    go-version: # optional
    # Path to the go.mod or go.work file.
    go-version-file: # optional
    # Set this option to true if you want the action to always check for the latest available version that satisfies the version spec
    check-latest: # optional
    # Used to pull Go distributions from go-versions. Since there's a default, this is typically not supplied by the user. When running this action on github.com, the default value is sufficient. When running on GHES, you can pass a personal access token for github.com if you are experiencing rate limiting.
    token: # optional, default is ${{ github.server_url == 'https://github.com' && github.token || '' }}
    # Used to specify whether caching is needed. Set to true, if you'd like to enable caching.
    cache: # optional, default is true
    # Used to specify the path to a dependency file - go.sum
    cache-dependency-path: # optional
    # Target architecture for Go to use. Examples: x86, x64. Will use system architecture by default.
    architecture: # optional
