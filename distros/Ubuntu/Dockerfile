FROM ubuntu:18.04

# Install package dependencies
RUN apt update && apt install -y git librsvg2-bin checkinstall nodejs build-essential qt5-default qtdeclarative5-dev qtdeclarative5-dev-tools qtwebengine5-dev qml-module-qtquick-controls qml-module-qtquick-dialogs qml-module-qt-labs-platform qml-module-qtwebchannel qml-module-qtwebengine wget libssl-dev sudo zlib1g-dev libuchardet-dev librubberband-dev libfreetype6-dev libfribidi-dev libfontconfig1-dev python devscripts equivs yasm libx264-dev libmp3lame-dev libfdk-aac-dev  libpulse-dev libasound2-dev

# Setting up new user
RUN useradd builduser -m
RUN passwd -d builduser
RUN echo 'builduser ALL=(ALL) ALL' >> /etc/sudoers
WORKDIR /home/builduser

# Import the required files
ADD package.sh .

RUN mkdir -p /usr/share/desktop-directories

