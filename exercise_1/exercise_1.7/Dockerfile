FROM ubuntu:16.04

WORKDIR /mydir
COPY curl_script.sh .
RUN chmod u+x curl_script.sh
RUN apt-get update && apt-get install -y curl
CMD ["/bin/bash", "curl_script.sh"]
