FROM alpine:3.9.2

LABEL maintainer=""

RUN apk add git npm 

RUN git clone https://github.com/hakimel/reveal.js.git

RUN cd reveal.js/ && npm install

ADD ./2git.html /reveal.js/index.html 
ADD ./logo.png /reveal.js/logo.png

EXPOSE 8000

ENTRYPOINT ["npm", "start", "--prefix", "/reveal.js/"]