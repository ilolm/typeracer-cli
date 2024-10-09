FROM node:20.16.0-alpine3.19

RUN npm i --global typeracer-cli && \
    npm cache clean --force && \
    adduser -s /usr/bin/nologin -H -D typer

USER typer

ENTRYPOINT ["/usr/local/bin/typerace"]
CMD ["practice"]
