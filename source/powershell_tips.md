### Tips
1. Trim the default prompt to display the current directory only
<code>
function prompt {
  $p = Split-Path -leaf -path (Get-Location)
  "PS $p> "
}
</code>
2. Map a network driver, and change to that drive
<code>
Get-PSDrive
New-PSDrive -Name e -PSProvider FileSystem -Root \\vboxsrv\vboxshare
set-location e:
</code>