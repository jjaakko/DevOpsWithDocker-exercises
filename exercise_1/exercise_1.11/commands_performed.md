docker build . -t e-1.11
touch logs.txt
# Map host 8000 to container 8000. Bind volumes.
docker run -p 8000:8000 -v $(pwd)/logs.txt:/logs.txt e-1.11