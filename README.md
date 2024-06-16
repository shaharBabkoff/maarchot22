##
# explenation about mync

- `importent note:` we did exercices 1-5 (without 6)
- in order to connect to the program you can use:
- nc (-u for udp) localhost port -for running client
- nc (-u for udp) -l -p port- for running server
  ##
# we will support the following features:


- -i flag: get input from a socket
- -o flag: write output to a socket
- -b flag: input and output go to the same socket
-  -e flag: execute a shell command
- -t flag: set timeout for the execution of the program
- if we don't send the -e flag, the program will act as a chat between two terminals. 

# running examples my program support:

`with -e:`
- ./mync -e "./ttt 123456789" -i TCPS6060
- ./mync -e "./ttt 123456789" -b TCPS6060
- ./mync -e "./ttt 123456789" -i TCPS6060 -o TCPClocalhost,5050
- ./mync -e "./ttt 123456789" -i UDPS6060
- ./mync -e "./ttt 123456789" -b UDPS6060
- ./mync -e "./ttt 123456789" -i UDPS6060 -o UDPClocalhost,5050
- ./mync -e "./ttt 123456789" -i TCPS6060 -o UDPClocalhost,5050
- ./mync -e "./ttt 123456789" -i UDPS6060 -o TCPClocalhost,5050
- ./mync -e "./ttt 123456789" -i TCPMUXS6060
- ./mync -e "./ttt 123456789" -b TCPMUXS6060

`whithout -e (the chat):`
- ./mync -i TCPS6060
- ./mync -o TCPClocalhost,5050
- ./mync -i TCPS6060 -o TCPClocalhost,5050
- ./mync -b TCPS5050
- ./mync -o TCPClocalhost,6060
- ./mync -i UDPS6060 -t 20
- ./mync -o UDPClocalhost,5050
- ./mync -i UDPS6060 -o UDPClocalhost,5050 -t 20
- ./mync -b UDPS5050 -t 20
- ./mync -o UDPClocalhost,606
- ./mync -i TCPS6060 -o UDPClocalhost,5050 
- ./mync -i UDPS6060 -o TCPClocalhost,5050

  ##
  # gcov
![image](https://github.com/shaharBabkoff/maarchot22/assets/155917341/0bcde603-234b-4724-a074-7354bd9aeb04)

- `note:` we run some check not everything and also a lot of checks are about sockets so we did not check this either... 


