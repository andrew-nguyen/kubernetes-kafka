NAME=kafka-persistent
VERSION=0.10.1.1
PROJECT_ID=qlaro-dev
PROJECT=us.gcr.io/${PROJECT_ID}

build: Dockerfile
	  docker build -t ${PROJECT}/${NAME}:${VERSION} .

push: build
	  gcloud docker -- push ${PROJECT}/${NAME}:${VERSION}

devbuild: Dockerfile
	  docker build -t ${DEVREGISTRY}/${NAME}:${VERSION} .

devpush: devbuild
	  docker push ${DEVREGISTRY}/${NAME}:${VERSION}

.PHONY: all build push
