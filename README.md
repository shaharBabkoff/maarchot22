##
# explenation about mync

- `importent note:` we did exercices 1-5 (without 6)
we will support the following features:

- -e flag: execute a shell command
- -i flag: get input from a socket
- -o flag: write output to a socket
- -b flag: input and output go to the same socket
- -t flag: set timeout for the execution of the program
- if we don't send the -e flag, the program will act as a chat between two terminals. 

# running examples my program support:

`with -e:`
- ./mync -e "./ttt 123456789" -i TCPS6060
- ./mync -e "./ttt 123456789" -b TCPS6060
- ./mync -e "./ttt 123456789" -o TCPClocalhost,5050
- ./mync -e "./ttt 123456789" -i TCPS6060 -o TCPClocalhost,5050
- ./mync -e "./ttt 123456789" -i UDPS6060
- ./mync -e "./ttt 123456789" -b UDPS6060
- ./mync -e "./ttt 123456789" -o UDPClocalhost,5050
- ./mync -e "./ttt 123456789" -i UDPS6060 -o UDPClocalhost,5050
- ./mync -e "./ttt 123456789" -i TCPS6060 -o UDPClocalhost,5050
- ./mync -e "./ttt 123456789" -i UDPS6060 -o TCPClocalhost,5050
- ./mync -e "./ttt 123456789" -i TCPMUXS6060
- ./mync -e "./ttt 123456789" -b TCPMUXS6060

`whithout -e (the chat):`
- ./mync -i TCPS6060
- ./mync -o TCPClocalhost,5050
- ./mync -i TCPS6060 -o TCPClocalhost,5050
- ./mync -i TCPS5050
- ./mync -o TCPClocalhost,6060
- ./mync -i UDPS6060
- ./mync -o UDPClocalhost,5050
- ./mync -i UDPS6060 -o UDPClocalhost,5050
- ./mync -i UDPS5050
- ./mync -o UDPClocalhost,6060
- ./mync -i TCPS6060 -o UDPClocalhost,5050 
- ./mync -i UDPS6060 -o TCPClocalhost,5050

