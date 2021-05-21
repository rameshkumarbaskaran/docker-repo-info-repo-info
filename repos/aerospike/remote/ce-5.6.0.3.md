## `aerospike:ce-5.6.0.3`

```console
$ docker pull aerospike@sha256:30364e82ded336900153e0cd5d86786aaf518e726b4b037b9bd5c5bda66dea9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:ce-5.6.0.3` - linux; amd64

```console
$ docker pull aerospike@sha256:78c20b859195dc9659419948e9b0f0633afd8b0ec70ca2d70e27bc25eb58ee76
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76855690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88181a7c26eb467aade456250355317921f5a0ea2c9db7f3ab1d3d4fe418de5`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Wed, 12 May 2021 01:23:21 GMT
ADD file:a88164546613d1850e5c5494cccad7124d713187bfabf592a783eb9328de51eb in / 
# Wed, 12 May 2021 01:23:22 GMT
CMD ["bash"]
# Thu, 20 May 2021 18:19:20 GMT
ENV AEROSPIKE_VERSION=5.6.0.3
# Thu, 20 May 2021 18:19:50 GMT
ENV AEROSPIKE_SHA256=75ba3e57bf3ada2aefbfe8a4e43523d87b933fea6b67e2b8c2ba542d5bfe8727
# Thu, 20 May 2021 18:20:10 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Thu, 20 May 2021 18:20:10 GMT
COPY file:1897c4aae07efbc61bf2d8c2c7b0dfb0990174e11cc787eac71d5adf767abaed in /etc/aerospike/aerospike.template.conf 
# Thu, 20 May 2021 18:20:11 GMT
COPY file:e1d47057fdb4c34c118f7ba5898161c386b475cba70907a4ae483866cf07335b in /entrypoint.sh 
# Thu, 20 May 2021 18:20:11 GMT
EXPOSE 3000 3001 3002
# Thu, 20 May 2021 18:20:11 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Thu, 20 May 2021 18:20:11 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:fa1690ae92289fb310aa27b793a164bf8bbedc7ddd00ca079a31bb8bb315b616`  
		Last Modified: Wed, 12 May 2021 01:30:20 GMT  
		Size: 22.5 MB (22528266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a624ac092d4a8b4926ba07a99dcc572587e64e878cd18a562b4f708fa8f8bbc6`  
		Last Modified: Thu, 20 May 2021 18:20:47 GMT  
		Size: 54.3 MB (54325405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d0240518db386af5b8c5617139bbde3b45ff96142eab1cbf66f3882edb0f43`  
		Last Modified: Thu, 20 May 2021 18:20:39 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499fc35a402bddf46d23a379a61c3737b92e7c3b7ed27bfdf536b962f71a5dbe`  
		Last Modified: Thu, 20 May 2021 18:20:39 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
