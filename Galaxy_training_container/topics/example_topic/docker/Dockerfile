
# Galaxy - Title of the topic
#
# to build the docker image, go to root of training repo and
#    docker build -t example_topic -f topics/example_topic/docker/Dockerfile .
#
# to run image:
#    docker run -p "8080:80" -t example_topic

FROM bgruening/galaxy-stable:19.01

MAINTAINER Galaxy Training Material

ENV GALAXY_CONFIG_BRAND "GTN: Title of the topic"

# copy the tutorials directory for your topic
ADD topics/example_topic/tutorials/ /tutorials/

# install everything for tutorials
ADD bin/docker-install-tutorials.sh /setup-tutorials.sh
ADD bin/mergeyaml.py /mergeyaml.py
RUN /setup-tutorials.sh
