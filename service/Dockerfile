FROM golang

# if left blank service will run with dev settings
# to build production image run:
# $ docker build ./service --build-args app_env=production
ARG app_env
ENV APP_ENV $app_env

# it is okay to leave user/GoDoRP as long as you do not want to share code with other libraries
COPY . /go/src/github.com/cpt-chewieeee/GoDoRP/service
WORKDIR /go/src/github.com/cpt-chewieeee/GoDoRP/service


RUN go run server.go

# if dev setting will use pilu/fresh for code reloading via docker-compose volume sharing with local machine
# if production setting will build binary
CMD if [ ${APP_ENV} = production ]; \
	then \
	api; \
	else \
	go get github.com/pilu/fresh && \
	fresh; \
	fi
EXPOSE 8080