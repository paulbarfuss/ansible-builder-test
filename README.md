# ansible-builder-test

### Build and Push

```bash
IMAGE_REPO=quay.io/pbarfuss
IMAGE_NAME=ansible-builder-test
IMAGE_TAG=v0.0.1

ansible-builder build -t ${IMAGE_REPO}/${IMAGE_NAME}:${IMAGE_TAG} -v3
podman push ${IMAGE_REPO}/${IMAGE_NAME}:${IMAGE_TAG}
```

### Push

```bash
```
