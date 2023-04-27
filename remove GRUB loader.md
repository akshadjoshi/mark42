`run cmd as administrator`

```powershell
diskpart
```

```powershell
list disk
```

- select the disk which has the max size `can be disk 0`

```powershell
select disk 
```

```powershell
list partition
```

- select the partition whose `TYPE` is `System`

```powershell
select partition
```

now assign a drive letter so that the partition can be mounted on your PC

```powershell
assign letter=z
```

**Now exit diskpart & check for the mounted partition in file manager**

- access the partition via cmd

```powershell
z:
```

```powershell
dir
```

- go in the dir/folder named as EFI or efi 
`you can PRESS {TAB} to auto complete `

```powershell
cd EFI 
```

- now check for other dir/folder in the EFI folder

```bash
dir
```

**check for the name of linux you installed** can be `debain` or `kali` depeding on the distro you installed 

```bash
rmdir /s kali
```

OR 

```bash
rmdir /s debain
```
