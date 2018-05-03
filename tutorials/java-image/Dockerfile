# By: Miztli Melgoza
# Image description: Linux Fedora 27 with sdkman and Oracle JDK 1.8
FROM fedora:27

# Maintained by
MAINTAINER \
[Miztli Melgoza <dark_coneja@hotmail.com>]

#ENV SDKMAN_DIR /usr/local/sdkman

# Install curl, zip, unzip, findutils
RUN dnf update -y \
    && dnf install -y curl zip unzip which findutils

RUN curl -s get.sdkman.io | bash \
    && source "$HOME/.sdkman/bin/sdkman-init.sh" \
    && sdk list java \
    && sdk install java 8u161-oracle\
    && java -version
# Define default command
CMD ["bash"]
