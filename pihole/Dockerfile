FROM pihole/pihole:latest

RUN cd /tmp && wget https://bin.equinox.io/c/VdrWdbjqyF/cloudflared-stable-linux-arm.deb \
 && apt-get install /tmp/cloudflared-stable-linux-arm.deb

RUN useradd -s /usr/sbin/nologin -r -M cloudflared

RUN chown cloudflared:cloudflared /usr/local/bin/cloudflared

ADD config/s6 /etc/services.d/

