# Python-Socket-For-Image-Transfer
A Python codelet to transfer .jpg files via socket

The image transfer protocol is as such

Server issue command - Client receive command and ACK
Server issue number of images to transfer - Client receive the int and ACK
For each image:
  Server issue the file size (in Bytes) - Client receive the imgsize and ACK
  Server transfer the file via socket.sendall - Client use socket.recv(imgsize) to receive and ACK

Code does not have all the error checkings. It only raises ValueError when there is an error occured. 
