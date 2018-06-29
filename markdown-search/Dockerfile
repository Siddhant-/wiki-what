FROM refinery29/alpine:3.7

ADD . /markdown-search

WORKDIR /markdown-search

RUN \
    apk add --update \
        ca-certificates \
        bash \
        git \
        openssh \
        python2 \
        python2-dev \
        py-setuptools; \
    easy_install-2.7 pip; \
    pip install -r /markdown-search/requirements.txt; \
    rm -rf /tmp/* /var/tmp/* /var/cache/apk/* /var/cache/distfiles/*

VOLUME ["/workdir"]

ENTRYPOINT ["python"]
# CMD ["/markdown-search/app.py"]
CMD ["/markdown-search/search-app.py"]