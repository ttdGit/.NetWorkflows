# LocalDb
Once installed, you can interact with SqlLocalDb using the command line. The following will tell you the version of SqlLocalDb:

```json
C:\> SqlLocalDb info
Result:
v11.0
```
If you want to create an instance:
```
C:\> SqlLocalDb create "MyInstance"
Result:
LocalDB instance "MyInstance" created with version 11.0.
```
To start the instance:
```
C:\> SqlLocalDb start "MyInstance"
Result:
LocalDB instance "MyInstance" started.
```
You can also create an instance and start it in one command using the -s argument:
```
C:\> SqlLocalDb create "MyInstance" -s
```
To stop and delete an instance, you can issue two commands:
```
C:\> SqlLocalDb stop   "MyInstance"
C:\> SqlLocalDb delete "MyInstance"

If you try to just delete the instance without first stopping it, you will get this error:
Delete of LocalDB instance "MyInstance" failed because of the following error:
Requested operation on LocalDB instance cannot be performed because specified instance is currently in use.
Stop the instance and try again.
To check on the status and other details about an instance, you can run:
C:\> SqlLocalDb info "MyInstance"
```
