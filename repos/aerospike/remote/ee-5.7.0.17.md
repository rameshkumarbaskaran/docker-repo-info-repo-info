## `aerospike:ee-5.7.0.17`

```console
$ docker pull aerospike@sha256:b26a34601ca57f412bf85404553d3cb75bbdd5e34c3360696360621dbf06fae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ee-5.7.0.17` - linux; amd64

```console
$ docker pull aerospike@sha256:7961e5441e32fea5238630b9666e082bfbb6468bbd5fc3fec94c2944a35f3fa0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83915214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7593e43631d102da87008daead703dd68cc32b7041cbc19cedb4cb3c034b467`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Sat, 23 Apr 2022 01:19:10 GMT
ENV AEROSPIKE_VERSION=5.7.0.17
# Sat, 23 Apr 2022 01:19:11 GMT
ENV AEROSPIKE_SHA256=1716524cf3d0d3087c6a62f28d49ab3d2c2d1dd739fe2d84d57ba71c337a6ef0
# Sat, 23 Apr 2022 01:19:11 GMT
ENV AS_TINI_SHA256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940
# Sat, 23 Apr 2022 01:19:31 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps wget python python3 python3-distutils lua5.2 gettext-base libldap-dev libcurl4-openssl-dev   && wget https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static -O /usr/bin/as-tini-static   && echo "$AS_TINI_SHA256 /usr/bin/as-tini-static" | sha256sum -c -   && chmod +x /usr/bin/as-tini-static   && wget "https://download.aerospike.com/artifacts/aerospike-server-enterprise/${AEROSPIKE_VERSION}/aerospike-server-enterprise-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Sat, 23 Apr 2022 01:19:32 GMT
COPY file:fa3bf0bd6c8130f09c26d82e9992baa4f2fe9ac69fee03e01b296f89984a97e0 in /etc/aerospike/aerospike.template.conf 
# Sat, 23 Apr 2022 01:19:32 GMT
COPY file:31b6a51a1d9d91f22433472f07f6ddfe3cea3bb07f460dd69c4187bc7fd20fdf in /entrypoint.sh 
# Sat, 23 Apr 2022 01:19:32 GMT
EXPOSE 3000 3001 3002
# Sat, 23 Apr 2022 01:19:32 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Sat, 23 Apr 2022 01:19:32 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abff78ab3a3e1da51dab6fb00350003ccc613229b083f1a988edfeb4ac5db857`  
		Last Modified: Sat, 23 Apr 2022 01:20:15 GMT  
		Size: 56.8 MB (56772462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5836f43361a66e005477de6ffacf71ebd1fc48bca2df3e06ddaf6293374b95`  
		Last Modified: Sat, 23 Apr 2022 01:20:07 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c166580457c2fd4397ec46b4ccf02d50af4c8320646a09c298e81eb8a5b1098`  
		Last Modified: Sat, 23 Apr 2022 01:20:07 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
