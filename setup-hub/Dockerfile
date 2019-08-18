FROM golang:latest

LABEL "com.github.actions.name"="github-hub"
LABEL "com.github.actions.description"="hub tool for GitHub"
LABEL "com.github.actions.icon"="save"
LABEL "com.github.actions.color"="gray-dark"

LABEL version="1.0.0"
LABEL repository="http://github.com/daimor/actions/hub"
LABEL homepage="http://github.com/daimor/actions/hub"
LABEL maintainer="Dmitry Maslennikov <mrdaimor@gmail.com>"

RUN apt-get update \
    && apt-get install software-properties-common -y --no-install-recommends \
    && add-apt-repository ppa:cpick/hub \
    && apt-get update \
    && apt-get install hub -y --no-install-recommends \
    && rm -rf /var/lib/apt/lists/*

ADD entrypoint.sh /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]