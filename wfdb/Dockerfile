# Usage
# 1st, Build this Dockerfile
#
#   docker build -t wfdb .
#
# 2nd, Run container
# 
# docker run -v $PWD:/Downloads rdsamp -r adfecgdb/r01.edf -c -H -f 0 -t 10 -v -pd > samples.csv
# 
# This means download file on current directory as samples.csv
# 
# off course, you can run other command like rdrecord or wrsamp etc.

FROM gcc:9.2

WORKDIR /wfdb
RUN apt-get update && apt-get install -y libcurl4-openssl-dev libexpat1-dev curl &&\
    curl -O https://archive.physionet.org/physiotools/wfdb.tar.gz && tar xzf wfdb.tar.gz

RUN TMP=$(ls | grep "^wfdb-") && cd $PWD/$TMP && ./configure && make install && make check

WORKDIR /Downloads

