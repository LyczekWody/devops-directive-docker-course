.PHONY: build
build:
	docker build --tag my-scratch-image .

# Have to authenticate to dockerhub and create repo first:
# https://docs.docker.com/engine/reference/commandline/login/
.PHONY: push-dockerhub
push-dockerhub:
	docker tag my-scratch-image szuter/moje_repo # defaults to latest
	docker push szuter/moje_repo

	docker tag my-scratch-image szuter/moje_repo:abc-123
	docker push szuter/moje_repo:abc-123

# Have to authenticate to ghcr.io first
# https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry#authenticating-to-the-container-registry
.PHONY: push-github-packages
push-github-packages:
	docker tag my-scratch-image ghcr.io/lyczekwody/docker-course
	docker push ghcr.io/lyczekwody/docker-course

	docker tag my-scratch-image ghcr.io/lyczekwody/docker-course:abc-123
	docker push ghcr.io/lyczekwody/docker-course:abc-123
