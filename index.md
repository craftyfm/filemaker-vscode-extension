

in the folder where the YAML file is   /color sytnax  and with the TextMate extention installed  open command pallet:  ctr + Shft + P  Convert to tmLanguage JSOn File

you will get a JSON file which you copy paste tot he / filemaker-synatax folder

now build the .vscode/launch.json by hitting F5

test the syntax change

update the package.json file
version: add minor number

now biuld the  vsix file
``` vsce package ```

``` vsce publish patch ```

install via 
``` code --install-extension filemaker-syntax-1.0.0.vsix ```

or

git clone https://github.com/yourusername/vscode-filemaker-syntax.git 
cd vscode-filemaker-syntax
npm install -g @vscode/vsce
vsce package
code --install-extension ./filemaker-syntax-1.0.0.vsix 



