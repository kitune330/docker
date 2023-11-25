FROM ubuntu:23.04
ENV LANG=ja_JP.utf8 \
    TZ=Asia/Tokyo \
    PATH="/root/.asdf/bin:${PATH}"
RUN DEBIAN_FRONTEND=noninteractive apt-get update ; \
    apt install -y vim unzip libssl-dev make automake autoconf libncurses5-dev g++ gcc curl git ; \
    git clone https://github.com/asdf-vm/asdf.git ~/.asdf --branch v0.13.1 ; \
    echo "ASDF_DIR=$HOME/.asdf" >> ~/.bashrc ; \
    echo '. "$HOME/.asdf/asdf.sh"' >> ~/.bashrc ;\
    echo '. "$HOME/.asdf/completions/asdf.bash"' >> ~/.bashrc ; \
    asdf plugin add erlang; \
    asdf plugin add elixir; \
    asdf install erlang 26.1.2 ; \
    asdf install elixir 1.15.7-otp-26 ; \
    asdf global erlang 26.1.2 ; \
    asdf global elixir 1.15.7-otp-26 ;
