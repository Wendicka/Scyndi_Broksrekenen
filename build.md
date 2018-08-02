In order to build you'll need the Scorpion tool. Scorpion is a CLI tool which translates Scyndi to the target languages.
In the first test Lua was used a prototype target language (due to its simplicity it was the easiest language to test stuff with), and for this document I'll assume you'll use Lua, but any console based language will do once Scyndi is fully functional.

BroksRekenen.ssf is the main file, alternatively you can use BroksRekenen_English.ssf to build the program to use the English language.

This command should translate the game into Lua
~~~shell
scorpion -target Lua BroksRekenen.ssf
~~~

Once more target languages are supported you can simply substitute "Lua" by the target language, no problem.

When translating to Lua (when using the Dutch version), please note that two files will be generated. "Dutch.ssf.scyndi.translation.Lua.lua" and "BroksRekenen.lua".
The former is only used during building and serves no more purpose after the translation is done. The reason it's not deleted is for some optimization plans I have for Scyndi later. BroksRekenen.lua will then be the file you can run with any Lua interpreter to see what it does. BroksRekenen does only use Lua core features so a simple CLI prototyper can run the translated code.

When translating to English
~~~shell
scorpion -target Lua BroksRekenen_English.ssf
~~~
The two files generated will then be "English.ssf.scyndi.translation.Lua.lua" and "BroksRekenen_English.lua"

