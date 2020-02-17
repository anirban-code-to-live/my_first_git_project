### How to open jupyter notebook in server and use it in local

1. `ssh -L <local_port>:localhost:<server_port> user@server`
2. `jupyter-notebook --no-browser --port <server_port>`
3. Go to localhost:<local_port>
