FROM python:2-alpine3.7

RUN  apk add --update --no-cache \
       openssh \
       shadow

RUN  sed -i \
       s/#PubkeyAuthentication.*/PubkeyAuthentication\ yes/ \
       /etc/ssh/sshd_config

EXPOSE 22

COPY docker-entrypoint.sh /usr/local/bin

ENTRYPOINT ["docker-entrypoint.sh"]
CMD ["/usr/sbin/sshd", "-D"]
