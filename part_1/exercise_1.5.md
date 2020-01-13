 Use -it to open interactive session:
 docker run -it ubuntu sh -c 'echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website;'

On another terminal tab install curl
 docker exec -it 5ddac6c6888e sh
 apt-get update
 apt-get install curl

 Then input helsinki.fi on the first tab:
 
