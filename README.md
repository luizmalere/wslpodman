# wslpodman
# assumes podman and/or podman desktop are installed and running ok

podman login registry.redhat.io

podman pull ubi9

podman run -it ubi9

yum install openssh

yum install openssh-server

yum install container-tools

yum install procps

# With container still running, open another shell and 

podman export -o ubi9.tar ${CONTAINER_ID}

podman machine init --image-path ubi9.tar podman-ubi9
