FROM opensuse/leap:42.3
#FROM opensuse/leap:15.0
#RUN apt update
RUN zypper -n install gcc || true
RUN zypper -n install make || true
RUN zypper -n install git || true
RUN zypper -n install bison || true
RUN zypper -n install flex || true
RUN zypper -n install texinfo || true
RUN zypper -n install tar || true
RUN zypper -n install gzip || true
RUN zypper -n install glibc-devel-32bit || true
RUN zypper -n install gcc-c++ || true
RUN zypper -n install lynx || true
RUN zypper -n install gcc-32bit || true
RUN zypper -n install cvs || true
RUN zypper -n install gettext-tools || true
#RUN zypper -n install xsltproc || true
#RUN zypper -n install gmp-devel mpfr-devel mpc-devel || true
#RUN apt install -y gawk
#RUN apt install -y libc6-dev-i386
RUN groupadd -g 1000 crossbuild
RUN useradd -ms /bin/bash -g 1000 crossbuild
USER crossbuild
RUN git config --global url."https://github.com/".insteadOf git@github.com:
WORKDIR /crossbuild
#USER root
