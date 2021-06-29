### How to open jupyter notebook in server and use it in local

##### Step 1:
On the server side, start your jupyter session:

1. For jupyter lab: `jupyter-lab --no-browser --port <server_port>`
2. If juoyter notebook: `jupyter-notebook --no-browser --port <server_port>`

##### Step 2:
On your local machine, use the following command:

`ssh -N -f -L localhost:<local_port>:localhost:<server_port> user@server`

##### Step 3:
Visit your local browser:

`localhost:<local_port>`
