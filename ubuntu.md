## Check location path install of an app
```bash
# check python
type -a python3
```

## Insall Node and NPM
```bash
# link: https://www.coursera.org/learn/react-basics/resources/FTd5h
sudo apt update
sudo apt install nodejs 
# veryfy
node --version && npm --version
```

## Some cml use in WSL
```bash
# cd to Downloads
cd /mnt/c/Users/thien1892/Downloads
# zip exclude subfolder
zip -r file_4.zip projects-final-portfolio/ -x projects-final-portfolio/node_modules/**\*
# install packet.json
npm install
```