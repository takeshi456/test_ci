FROM alpine

ADD requirement.txt /root/requirement.txt

WORKDIR /root

RUN apk update && \
    apk upgrade && \
    apk add --no-cache python3 python3-dev py3-pip git && \
    pip3 install -r requirement.txt && \
    git clone https://github.com/takeshi456/test_ci

ENTRYPOINT ["/usr/bin/python3","/root/test_ci/test/manage.py","runserver","0:8000"]
