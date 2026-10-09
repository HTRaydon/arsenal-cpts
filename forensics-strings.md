# Strings

% strings, forensics, cpts

## Strings - Strings - Strings - Strings - retrieving-hardcoded-credentials-from-thick-client-applications
#cat/POSTEXPLOIT #cpts
Inspecting the execution of the executable through `ProcMon64` shows that it is querying multiple things in the registry and does not show anything solid to go by. Let's start `x64dbg`, navigate to `Options` -> `Preferen

```
).NETFramework,Version=v4.0,Profile=Client
```

## Strings - Strings - Strings - Strings - strings-to-view-db-file-contents
#cat/POSTEXPLOIT #cpts
We can also copy them over to our attack box and search through the data using the `strings` command, which may be less efficient depending on the size of the database.

```
strings plum.sqlite-wal
```

