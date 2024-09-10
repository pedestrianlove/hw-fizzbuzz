# From official php image.
FROM ruby:alpine

LABEL org.opencontainers.image.source="https://github.com/pedestrianlove/hw-fizzbuzz"

RUN mkdir -p /workspace/cli

# Install quality-of-life packages.
RUN apk --update add --no-cache curl git vim fish tmux neovim wget make
RUN git clone https://github.com/rbenv/rbenv.git ~/.rbenv
RUN gem install robocop

# Make fish the default shell
RUN sed -i 's|/bin/sh$|/usr/bin/fish|' /etc/passwd

# Prevent container from exiting early.
CMD ["sleep", "infinity"]
