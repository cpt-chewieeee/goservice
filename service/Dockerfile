FROM golang

# if left blank service will run with dev settings
# to build production image run:
# $ docker build ./service --build-args app_env=production
ARG app_env
ENV APP_ENV $app_env

# WORKDIR /go/src/github.com/cpt-chewieeee/GoDoRP/service
COPY ./start /usr/local/bin
RUN chmod +x /usr/local/bin/start
# RUN go get github.com/julienschmidt/httprouter
# RUN go build server.go

# # if dev setting will use pilu/fresh for code reloading via docker-compose volume sharing with local machine
# # if production setting will build binary
# CMD if [ ${APP_ENV} = production ]; \
# 	then \
# 	service; \
# 	else \
# 	go get github.com/pilu/fresh && \
# 	fresh; \
# 	fi
# EXPOSE 8080