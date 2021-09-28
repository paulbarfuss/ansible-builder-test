# ansible-builder-test

### Build and Push

Ansible Builder uses similar syntax to `podman build` and will automatically build your Dockerfile/Containerfile based on the requirements specified in:

- bindep.txt (extra binaries such as pandoc, etc...)
- requirements.txt (any Python dependencies not automatically pulled in by Ansible Galaxy)
- requirements.yml (Ansible Galaxy collections, including any Python dependencies required by each collection)

Run the following to build and push the image using your own container repo and tags:

```bash
IMAGE_REPO=quay.io/pbarfuss
IMAGE_NAME=ansible-builder-test
IMAGE_TAG=v0.0.1

ansible-builder build -t ${IMAGE_REPO}/${IMAGE_NAME}:${IMAGE_TAG} -v3
podman push ${IMAGE_REPO}/${IMAGE_NAME}:${IMAGE_TAG}
```

### Inspect image


