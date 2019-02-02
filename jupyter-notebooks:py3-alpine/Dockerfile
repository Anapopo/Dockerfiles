FROM python:3-alpine

WORKDIR /Notebooks

RUN sed -ie 's/dl-cdn.alpinelinux.org/mirrors.tuna.tsinghua.edu.cn/g' /etc/apk/repositories && \
    apk --no-cache add build-base zeromq && \
    pip install -i https://pypi.tuna.tsinghua.edu.cn/simple --no-cache-dir jupyter && \
    apk del build-base

CMD ["jupyter", "notebook", "--allow-root", "--no-browser", "--ip=0.0.0.0"]

EXPOSE 8888
