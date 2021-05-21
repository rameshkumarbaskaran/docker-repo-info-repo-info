## `aerospike:ee-5.6.0.3`

```console
$ docker pull aerospike@sha256:27989acd19b7b1bc884aea332d511f1115bb88d920a28e8e1fa495a931d3f170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:ee-5.6.0.3` - linux; amd64

```console
$ docker pull aerospike@sha256:7e996e671b94b3c7bb8b0dce6edfc890b1f7d2029d50fae379c37017697fa41d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78568586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc6a0820d322b92d39a094c072d4e53636519fda9666f25eb7ea2066ffc2df22`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Wed, 12 May 2021 01:23:21 GMT
ADD file:a88164546613d1850e5c5494cccad7124d713187bfabf592a783eb9328de51eb in / 
# Wed, 12 May 2021 01:23:22 GMT
CMD ["bash"]
# Thu, 20 May 2021 18:19:20 GMT
ENV AEROSPIKE_VERSION=5.6.0.3
# Thu, 20 May 2021 18:19:20 GMT
ENV AEROSPIKE_SHA256=32f93d44c76f5cfd97fccb1256086854bfd254b65f5700d643e9ed8352910b88
# Thu, 20 May 2021 18:19:42 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libldap-dev libcurl4-openssl-dev   && wget "https://www.aerospike.com/enterprise/download/server/${AEROSPIKE_VERSION}/artifact/debian9" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Thu, 20 May 2021 18:19:42 GMT
COPY file:7d75174e09b209cf7f56b715636c2b8e08dd083d548e8cdc8517cabd512600b5 in /etc/aerospike/aerospike.template.conf 
# Thu, 20 May 2021 18:19:43 GMT
COPY file:31b6a51a1d9d91f22433472f07f6ddfe3cea3bb07f460dd69c4187bc7fd20fdf in /entrypoint.sh 
# Thu, 20 May 2021 18:19:43 GMT
EXPOSE 3000 3001 3002
# Thu, 20 May 2021 18:19:43 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Thu, 20 May 2021 18:19:43 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:fa1690ae92289fb310aa27b793a164bf8bbedc7ddd00ca079a31bb8bb315b616`  
		Last Modified: Wed, 12 May 2021 01:30:20 GMT  
		Size: 22.5 MB (22528266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cca231739e5c51faf397352718ac7049f1ac732c36a42aa2abfc46ba8124b24`  
		Last Modified: Thu, 20 May 2021 18:20:30 GMT  
		Size: 56.0 MB (56038240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f502353c8e14ac5081b25bd792f56f5658eaefea8ee164e32c3758b1ba1ab58d`  
		Last Modified: Thu, 20 May 2021 18:20:23 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88cd5fc8f6f551c8027cdded79c55765efcb5525a6bc33eeff048e997bc70ecc`  
		Last Modified: Thu, 20 May 2021 18:20:22 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
