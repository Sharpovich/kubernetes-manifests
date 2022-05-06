FROM sharpov210/lesson1:latest
RUN apk add curl
WORKDIR /opt/app
ADD index.js .
HEALTHCHECK --interval=5s --timeout=5s \
    --start-period=5s --retries=3 \
    CMD curl http://localhost:3000 || exit 1
CMD ["node", "./index.js"]