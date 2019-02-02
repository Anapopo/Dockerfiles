FROM swden/jupyter-notebook:py3-alpine

RUN apk --no-cache add build-base npm nodejs python2 && \ 
    npm install -g --registry https://registry.npm.taobao.org/ --unsafe-perm ijavascript && \ 
    ijsinstall && \
    apk del build-base npm python2
