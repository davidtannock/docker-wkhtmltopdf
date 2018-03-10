FROM alpine:3.7

ENV WKHTMLTOPDF_VERSION 0.12.4

COPY wrapper /tmp/

RUN apk add --update-cache \
        xvfb \
        dbus \
        ttf-freefont \
        fontconfig && \
    apk add --update-cache \
            --repository https://dl-3.alpinelinux.org/alpine/edge/testing/ \
            --allow-untrusted \
        wkhtmltopdf && \
    apk add --update-cache \
        python \
        make \
        g++ && \
    rm -rf /var/cache/apk/* && \
    mv /usr/bin/wkhtmltopdf /usr/bin/wkhtmltopdf.ini && \
    mv /tmp/wrapper /usr/bin/wkhtmltopdf && \
    chmod +x /usr/bin/wkhtmltopdf

ENTRYPOINT ["/usr/bin/wkhtmltopdf"]
CMD ["-h"]
