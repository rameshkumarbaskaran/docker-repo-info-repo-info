## `aerospike:ce-6.0.0.0`

```console
$ docker pull aerospike@sha256:f71ad8c1229b1f4111562009649c73456ab8e45f6991d0390b7ce9b7d316b219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ce-6.0.0.0` - linux; amd64

```console
$ docker pull aerospike@sha256:5b11abf417a185d4b4c1f1beaad6b2c5376c0e8ce7bde585193004c73f0da822
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100930164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8caa5000ac32c6776c13485f461123038768be6ff344f4f0a1328379ea32b678`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 27 Apr 2022 19:48:48 GMT
ENV AEROSPIKE_VERSION=6.0.0.0
# Wed, 27 Apr 2022 19:49:15 GMT
ENV AEROSPIKE_SHA256=4b72303d8d7d128bc0ba7dc30f8cc268ad776d3357b01f8ca377c281d6ad1d8c
# Wed, 27 Apr 2022 19:49:35 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Wed, 27 Apr 2022 19:49:36 GMT
COPY file:57aa54f8d05380c639ff298f99e0387bafe493553aa29e39911c8342f60a0f0e in /etc/aerospike/aerospike.template.conf 
# Wed, 27 Apr 2022 19:49:36 GMT
COPY file:e1d47057fdb4c34c118f7ba5898161c386b475cba70907a4ae483866cf07335b in /entrypoint.sh 
# Wed, 27 Apr 2022 19:49:36 GMT
EXPOSE 3000 3001 3002
# Wed, 27 Apr 2022 19:49:36 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Wed, 27 Apr 2022 19:49:36 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f30f44593830547d5476a611e2496a80e37ebed2a4212e8f9e0ec133caa268c`  
		Last Modified: Wed, 27 Apr 2022 19:50:10 GMT  
		Size: 73.8 MB (73787469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c51448bae2f51cc2d19c7cc820cf184b2f7f5e6da9350a6386cf29a128fe95`  
		Last Modified: Wed, 27 Apr 2022 19:50:02 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1c73701f75c5051098970b8720d8a05ffcfc8adfd1033e436fd9de0c0f9652`  
		Last Modified: Wed, 27 Apr 2022 19:50:02 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
