# Powershell


### Environmental Variables
https://shellgeek.com/powershell-print-environment-variables/


```
Get-ChildItem $env:
```
> *Pick Specific Variable e.g(processor architecture)*

```
Get-ChildItem $env:PROCESSOR_ARCHITECTURE
```


### Piping 

```
GetChildItem | Measure-Object
```


### Loops 

```
For ($i=0; $i -le 100; $i++) {
    Write-output "hope is a good girl"
}

```

### Conditions
```
if ($box -lt 3) {
}
```


### Variables

```
$ box = "olamide"
$box
```


### _EXample_

> get the 8th word from the description of windows update service

```
((Get-WmiObject -Class Win32_Service -Filter "Name='wuauserv'" ).Description).split(' ')[7] 
```
> count the numbers of times polo as a whole word occurs in the file countpolos

```
((get-content .\countpolos).split(' ')  | select-string "^polo$").count 
```
