<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:ce-6.1.0.2`](#aerospikece-6102)
-	[`aerospike:ee-6.1.0.2`](#aerospikeee-6102)

## `aerospike:ce-6.1.0.2`

```console
$ docker pull aerospike@sha256:7f2f8a0bb5729117b22a575f35d2e20e225c2333f711821150c42a40cb9a44cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ce-6.1.0.2` - linux; amd64

```console
$ docker pull aerospike@sha256:467f150db3964e15cf6aee99454f5dbdde3d1dbdef74b48ce396561447e194aa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.4 MB (121425819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3cadc9d478cf49a8818803a547de92b702e73675aacb46ba9f129057c7ed48`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:48 GMT
ADD file:782d864aa72c2d5fb599311ebae56db4067d2e91ff532c1aaf1a291c3dbce5bb in / 
# Tue, 13 Sep 2022 00:56:49 GMT
CMD ["bash"]
# Thu, 15 Sep 2022 17:19:27 GMT
ENV AEROSPIKE_VERSION=6.1.0.2
# Thu, 15 Sep 2022 17:19:56 GMT
ENV AEROSPIKE_SHA256=de37fb05085a0cc4183660bb5df9d9aab8c02039af2eb544102925b11c5c216e
# Thu, 15 Sep 2022 17:20:17 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && if [ -d '/opt/aerospike/bin/asadm' ];   then   mv /opt/aerospike/bin/asadm /usr/lib/;   ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f /usr/lib/asadm/asinfo ];     then     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;     fi   fi   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Thu, 15 Sep 2022 17:20:18 GMT
COPY file:f497c4c6974a190f79a562efd9c9c0d6b753efe43e62c3fcc2536f74ad08238d in /etc/aerospike/aerospike.template.conf 
# Thu, 15 Sep 2022 17:20:18 GMT
COPY file:fe302e12e47afe1731a34ed4ed29328c6901a3f2c9e32e307220e65cb76d53a2 in /entrypoint.sh 
# Thu, 15 Sep 2022 17:20:18 GMT
EXPOSE 3000 3001 3002
# Thu, 15 Sep 2022 17:20:18 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Thu, 15 Sep 2022 17:20:18 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:4b7b4a8876e2f677668e51b8473f97a237d3d4df201b9df4031bcaa8068370b1`  
		Last Modified: Tue, 13 Sep 2022 01:01:16 GMT  
		Size: 27.1 MB (27130552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13eadaf12a21043929d015fceb2e164399af40336cd4765671d4694622ed4f0c`  
		Last Modified: Thu, 15 Sep 2022 17:21:04 GMT  
		Size: 94.3 MB (94293436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8332798a39d535d760eda75dbe14a5397f62d76e4988d3c0894c724bef5222`  
		Last Modified: Thu, 15 Sep 2022 17:20:50 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fafe08288834af0c40cad34113d556f7eb8d280aa968517dd2a4573a526b2b3`  
		Last Modified: Thu, 15 Sep 2022 17:20:50 GMT  
		Size: 811.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:ee-6.1.0.2`

```console
$ docker pull aerospike@sha256:8af1b2bb3c9c763fcffcae836b65a4b8c4dbae2b6cc75105d3573ecc71bff731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ee-6.1.0.2` - linux; amd64

```console
$ docker pull aerospike@sha256:37306b7bff935092b091048fba8785f236e0cc4e4f4b017172069b9d92c53b45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123846035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f4ea818b9dbb111d689562a310ab1bd1e41b2b889749de03961ff6eab104d2`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:48 GMT
ADD file:782d864aa72c2d5fb599311ebae56db4067d2e91ff532c1aaf1a291c3dbce5bb in / 
# Tue, 13 Sep 2022 00:56:49 GMT
CMD ["bash"]
# Thu, 15 Sep 2022 17:19:27 GMT
ENV AEROSPIKE_VERSION=6.1.0.2
# Thu, 15 Sep 2022 17:19:27 GMT
ENV AEROSPIKE_SHA256=efd49204813876c5b3b3064b875efccfd49fa2a7e4840161e411988fc87f012f
# Thu, 15 Sep 2022 17:19:28 GMT
ENV AS_TINI_SHA256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940
# Thu, 15 Sep 2022 17:19:53 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps wget python python3 python3-distutils lua5.2 gettext-base libldap-dev libcurl4-openssl-dev   && wget https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static -O /usr/bin/as-tini-static   && echo "$AS_TINI_SHA256 /usr/bin/as-tini-static" | sha256sum -c -   && chmod +x /usr/bin/as-tini-static   && wget "https://download.aerospike.com/artifacts/aerospike-server-enterprise/${AEROSPIKE_VERSION}/aerospike-server-enterprise-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && if [ -d '/opt/aerospike/bin/asadm' ];   then   mv /opt/aerospike/bin/asadm /usr/lib/;   ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f /usr/lib/asadm/asinfo ];     then     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;     fi   fi   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Thu, 15 Sep 2022 17:19:53 GMT
COPY file:f56e2e33c0b4bb66affff75053eaed44661e723b8b33d3ef3c10e305b506c350 in /etc/aerospike/aerospike.template.conf 
# Thu, 15 Sep 2022 17:19:53 GMT
COPY file:697e2123680798e87da7a3f98d1d70e76ffec66f0e1aafa90ff25047a11cca52 in /entrypoint.sh 
# Thu, 15 Sep 2022 17:19:54 GMT
EXPOSE 3000 3001 3002
# Thu, 15 Sep 2022 17:19:54 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Thu, 15 Sep 2022 17:19:54 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:4b7b4a8876e2f677668e51b8473f97a237d3d4df201b9df4031bcaa8068370b1`  
		Last Modified: Tue, 13 Sep 2022 01:01:16 GMT  
		Size: 27.1 MB (27130552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c9fbe979a8225da421c5b78f0f9aedb2b90ffc751554bc5c7308efe765cbf3`  
		Last Modified: Thu, 15 Sep 2022 17:20:43 GMT  
		Size: 96.7 MB (96713597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d58d19b957cc6c97371e0bdb0fea98821b31fd637be0bde49eddbf41f30915`  
		Last Modified: Thu, 15 Sep 2022 17:20:29 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73824d619848bcf12c7d6e249182c5ca4bbe632331b0fbb4cfb2b0739972173`  
		Last Modified: Thu, 15 Sep 2022 17:20:29 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
