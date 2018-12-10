FROM node:lts-alpine

WORKDIR /Blog

# hexo
RUN sed -i 's/dl-cdn.alpinelinux.org/mirror.tuna.tsinghua.edu.cn/g' /etc/apk/repositories \
    && apk --no-cache add curl git \
    && yarn config set registry 'https://registry.npm.taobao.org' \
    && yarn global add hexo \
    && git clone https://github.com/Anapopo/Blog.git . \
    && git clone https://github.com/Anapopo/hexo-theme-spectre.git themes/spectre \
    && curl https://gist.githubusercontent.com/Anapopo/ab359e360107c6c9dee9093fde8a3760/raw/6f061a4a27a179574602465320476fd487663579/_config.yml > themes/spectre/_config.yml \
    && yarn \
    && apk del curl git

EXPOSE 4000

CMD ["hexo", "server"]
