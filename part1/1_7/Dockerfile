FROM ubuntu:16.04

RUN apt-get update && apt-get install -y curl
COPY curlscript.sh ./curlscript.sh
RUN chmod 755 ./curlscript.sh
CMD ["./curlscript.sh"]
