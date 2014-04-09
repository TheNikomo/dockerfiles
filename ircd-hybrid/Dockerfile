# ircd-hybrid
#
# VERSION               0.0.1

FROM debian
MAINTAINER Niko Montonen "nikomo@nikomo.fi"

CMD apt-get update && apt-get dist-upgrade -y
CMD apt-get update && apt-get install -y nano dialog irssi ircd-hybrid supervisor

CMD rm /etc/ircd-hybrid/ircd.conf
ADD ircd.conf /etc/ircd-hybrid/ircd.conf
CMD chmod 660 /etc/ircd-hybrid/ircd.conf
CMD chown irc:irc /etc/ircd-hybrid/ircd.conf

ADD supervisord.conf /etc/supervisor/conf.d/supervisord.conf
CMD /usr/bin/supervisord