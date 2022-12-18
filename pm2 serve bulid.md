
## Create .sh file and run pm2
Inside it write 

```
serve -s build -l [port]
```
And run .sh file as below

```
pm2 start [bash_script_file] -- name [process_name]
```


## (Or) Create app.config.json file

Inside it write below code 

```
{
  apps : [
    {
      name : "react-app",
      script : "npx",
      interpreter : "none",
      args: "serve -s build -p 3000"
    }
  ]
}
```
Run blow code \
```
pm2 start app.config.json
```

## (Or) Run below command
```
pm2 serve build/ [port] --name [process_name]
```
