## Summary

This repo comprises a customized static SQLite library used within Tau4Mac.

- [SQLite source code used for this customized compilation](https://www.sqlite.org/download.html)
- [SQLite compilation options](https://www.sqlite.org/compile.html)

sqlite4tau uses the *amalgamation version* of SQLite source code, which is officially recommended for all applications.

## Involved Compilation Options in This Repo

- DEBUG
  - `SQLITE_OMIT_AUTOINIT`
  > For backwards compatibility with older versions of SQLite that lack the sqlite3_initialize() interface, the sqlite3_initialize() interface is called automatically upon entry to certain key interfaces such as sqlite3_open(), sqlite3_vfs_register(), and sqlite3_mprintf(). The overhead of invoking sqlite3_initialize() automatically in this way may be omitted by building SQLite with the `SQLITE_OMIT_AUTOINIT` C-preprocessor macro. When built using `SQLITE_OMIT_AUTOINIT`, SQLite will not automatically initialize itself and the application is required to invoke sqlite3_initialize() directly prior to beginning use of the SQLite library.

  - `SQLITE_MEMDEBUG`
  > The `SQLITE_MEMDEBUG` option causes an instrumented debugging memory allocator to be used as the default memory allocator within SQLite. The instrumented memory allocator checks for misuse of dynamically allocated memory. Examples of misuse include using memory after it is freed, writing off the ends of a memory allocation, freeing memory not previously obtained from the memory allocator, or failing to initialize newly allocated memory.
  
  - `SQLITE_USE_URI`
  > This option causes the URI filename process logic to be enabled by default.
  
  - `SQLITE_ENABLE_API_ARMOR`
  > When defined, this C-preprocessor macro activates extra code that attempts to detect misuse of the SQLite API, such as passing in NULL pointers to required parameters or using objects after they have been destroyed.

- RELEASE
  - `SQLITE_OMIT_AUTOINIT`
  > *As above.*

  - `SQLITE_ENABLE_API_ARMOR`
  > *As above.*

  - `SQLITE_USE_URI`
  > *As above.*
