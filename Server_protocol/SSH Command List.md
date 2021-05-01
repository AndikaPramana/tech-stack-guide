# Command List 

## SSH 
1. SSH to a server 
	- `ssh user@ip_address` 
2. SSH to a server using authentication (key) file
	- `ssh -i key.pem user@ip_address"`
3. Listening to server port using tunneling ssh method 
	- `ssh -i key.pem -L local_port:server_ip:server_port user_tunnel_server@ip_tunnel_server`
4. Opening sftp server port through tunneling
	- 'ssh -i key.pem -L 2121:server_ip:22 user_tunnel_server@ip_tunnel_server'
	Then connect using ftp/ftp_client to localhost:2121

## SCP
1. Copy file from remote to local
	- `scp user@remote_ip:/remote_path/folder/filename /local_path`


