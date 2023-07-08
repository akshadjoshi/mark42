
```bash
subl $(pwd)
```
- **to permanently change the shell of anyuser**
```bash
chsh <username> -s  $(which bash)
```
- **to edit scripts**
```bash
vim $(which b-tooth)
```
> note: these will work if the script or binary is in $PATH
```bash
sudo mv $(which b-tooth) .
```
