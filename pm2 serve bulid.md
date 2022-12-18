
## Create .sh file and run pm2
Inside it write 

```
serve -s build -l [port]
```
And run .sh file as below

```
serve -s build -l [port]
```

and then run below code
```
pm2 start [bash_script_file] -- name [process_name]
```


## (Or) Create app.config.json file

Inside it write below code 

```
{
  apps : [
    {
      name : [process_name],
      script : "npx",
      interpreter : "none",
      args: "serve -s build -l [port]"
    }
  ]
}
```
Run blow code 
```
pm2 start app.config.json
```

## (Or) Run below command
```
pm2 serve build/ [port] --name [process_name]
```
