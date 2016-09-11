# Version: 0.0.1
FROM yan047/jdk7v2
MAINTAINER Bo Yan

# create directory
ENV SRC_DIR /Code
RUN mkdir -p "${SRC_DIR}"

Copy App.java "${SRC_DIR}"

RUN cd "${SRC_DIR}" && javac App.java


