# sqlite4tau

## Summary

This repo comprises a customized static SQLite library used within Tau4Mac.

- [SQLite source code used for this customized compilation](https://www.sqlite.org/download.html)
- [SQLite compilation options](https://www.sqlite.org/compile.html)

## Involved Compilation Options in This Repo

- DEBUG
  - `SQLITE_OMIT_AUTOINIT`
  - `SQLITE_MEMDEBUG`
  - `SQLITE_USE_URI`
  - `SQLITE_ENABLE_API_ARMOR`

- RELEASE
  - `SQLITE_OMIT_AUTOINIT`
  - `SQLITE_ENABLE_API_ARMOR`
  - `SQLITE_USE_URI`
