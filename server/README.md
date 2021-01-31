# Iot provider F# server 

This folder contain the server side of the project, built in F# and based in Saurn. This server side aplication provides a Json endpoint, to store and amnage data for IoT solutions. 



## Build and run the application

1. Make sure you have installed version of .Net SDK defined in `global.json`
2. Run `dotnet tool restore` to restore all necessary tools
3. Run `dotnet saturn migration` to create sqlite database
3. Run `dotnet fake build -t Run` to start application in watch mode (automatic recompilation and restart at file save)


#### Commands for saturn cli (alread installed)

`dotnet saturn` supports following commands:

* `gen NAME NAMES COLUMN:TYPE COLUMN:TYPE COLUMN:TYPE ...` - creates model, database layer, views and controller returning HTML views
* `gen.json NAME NAMES COLUMN:TYPE COLUMN:TYPE COLUMN:TYPE ...` - creates model, database layer and JSON API controller
* `gen.model NAME NAMES COLUMN:TYPE COLUMN:TYPE COLUMN:TYPE ...` - creates model and database layer
* `migration` - runs all migration scripts for the database

* More infos about how to use saturn CLI, go to Saturn [CLI webpage](https://github.com/SaturnFramework/Saturn.Cli). 