# INDI PROD

## DESCRIPTION
...


## SYNTAX

```ruby
indiprod [[-start] <String>] [[-revupdate] <Array>] [[-exc] <Array>] [[-dict] <Hashtable>] 
```

## EXAMPLES

```powershell
indiprod -start '22:00 01.31.2022' -revupdate @(6767,9852) -exc @(13215,15644) -dict @{15616 = 864641}
```

```powershell
indiprod -start $start -dict @{15616 = 864641} -revupdate @(6767,9852) -exc @(13215,15644) 
```

## PARAMETERS

### -start
policy activation start date

```yaml
Type: String
Mandatory: True
Syntax: '22:00 05.30.2023' --> 'HH:MM MM.DD.YYYY'
```

### -revupdate
Policy ID 

ID from QS, PILOT group NOT DL-SWD
```yaml
Type: Array
Mandatory: False
Syntax:  @(3333,4444)
```

### -exc
Policy ID 

```yaml
Type: Array
Mandatory: False
Syntax:  @(3333,4444)
```
### -dict
DSM Group object ID

pilot, qs and prod groups
```yaml
Type: Hashtable
Mandatory: True
Syntax:  @{current = target
           honnan = hova
         }
```
