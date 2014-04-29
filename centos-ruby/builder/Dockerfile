# Self-contained Ruby builder image.
#
# You can use this image to produce an application image providing the source
# code:
#
# $ docker run -v $(pwd):/tmp/src openshift/centos-ruby-builder
# <your application is being build>
#
# $ docker commit <id> your_application
#
# Then you can start your application using:
#
# $ docker run -p :9292 your_application
#
#
FROM openshift/centos-ruby-extended
MAINTAINER Michal Fojtik <mfojtik@redhat.com>

USER ruby

# TODO: Replace this by ADD url? Like:
# ADD https://openshift.url/v3/builders/ruby /usr/bin/deploy
#
ADD ./bin/deploy /usr/bin/deploy

ENTRYPOINT ["/usr/bin/deploy"]
