#Operator System Project
##A project emulate rsync

client syntax: ./client source_path destination_address@destination_path options

source_address & destination_address (pending)
- for local: folder_path
- for outer_computer: ip_address@folder_path

option
- get: one way from server to client
- put: one way from client to server
- post: two ways sync

Version_1 with GET option, get file from server to client (oneway)
user guide
```
git clone https://github.com/DucHuySET/os_project.git
cd os_project
cd server
gcc server.c ../utils/*.c ../include/*.c  -o server -lssl -lcrypto
./server
```
result: Server listening on port 12345...

for client, can modify GET, PUT, POST
```
cd ..
cd client
gcc client.c ../utils/*.c ../include/*.c  -o client -lssl -lcrypto
./client ../test/test_folder_1 ../test/test_folder_2 GET
```
result: 

Connected to server

Then observe result

For sync between two computer, firstly get server ip address with run in terminal

```
ip a
```
or 
```
hostname -I
```
