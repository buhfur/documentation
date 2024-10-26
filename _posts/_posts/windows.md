
# Windows 10 notes 

## Managing files  

### List 10 largest files for C:\ in megabytes

`Get-ChildItem c:\ -r -ErrorAction SilentlyContinue –Force |sort -descending -property length | select -first 10 name, DirectoryName, @{Name="MB";Expression={[Math]::round($_.length / 1MB, 2)}}`


## Environment Variables 

### List Environment Variables 

```bash
Get-Childitem env: 
```

### Modifying existing Environment Variables 

The commands below are used to modify existing Environment Variables.

#### Permanantly append Variable to path 

```bash 
setx MyVariable "MyPersistentValue" 
```

#### Add new path to system Path 

```bash
$newPath = "$env:Path;C:\NewPath"
setx Path $newPath
```

#### Remove temporary Environment Variable from path 

```bash
Remove-Item env:MyVariable
```

#### Remove persistent Environment Variable from path 

```bash
setx MyVariable ""
```

#### Check if Environment Variable exists in a powershell script 

```bash 
if($env:MyVariable) {
    Write-Output "MyVariable exists with value $env:MyVariable"
}else { 
    Write-Output "MyVariable does not exist"
}
```

#### Using an Environment Variable in a Script 

```bash 
$env:MyVariable = "something"
Write-Output "The value of MyVariable is : $env:MyVariable"
```

---

### Modifying Windows System PATH's 

### List current path 

```bash 
echo $env:path 
```

#### Temporarily append Variable to path 

```bash
$env:path += ";C:\Program Files\GnuWin32\bin" 
```


