## `aerospike:ce-5.7.0.11`

```console
$ docker pull aerospike@sha256:b2d4c90a87261c6fe782360bec820f6b90b7f22533d1aa8430ca3f4d1ebf5d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ce-5.7.0.11` - linux; amd64

```console
$ docker pull aerospike@sha256:c47788c218b005938b412fc259337241a1cb5960fd60ec49dcba68078842f6a7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81536275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c134699fbec9ccff960b601ea2d886f8389da8a9d7b98ea925da3364c088a352`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:26 GMT
ADD file:7f5787c324936e09d339f9426eec4a0120431e2a4b6ccb0db28b94d61f074ab2 in / 
# Thu, 17 Mar 2022 04:04:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:25:25 GMT
ENV AEROSPIKE_VERSION=5.7.0.11
# Fri, 18 Mar 2022 06:25:53 GMT
ENV AEROSPIKE_SHA256=bd0d9962c8d068270746833df313d32117ef9e9c3e2367f8ac6902cf97d66142
# Fri, 18 Mar 2022 06:26:12 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Fri, 18 Mar 2022 06:26:13 GMT
COPY file:1897c4aae07efbc61bf2d8c2c7b0dfb0990174e11cc787eac71d5adf767abaed in /etc/aerospike/aerospike.template.conf 
# Fri, 18 Mar 2022 06:26:13 GMT
COPY file:e1d47057fdb4c34c118f7ba5898161c386b475cba70907a4ae483866cf07335b in /entrypoint.sh 
# Fri, 18 Mar 2022 06:26:13 GMT
EXPOSE 3000 3001 3002
# Fri, 18 Mar 2022 06:26:13 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Fri, 18 Mar 2022 06:26:13 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:a4b007099961706d45bdb3eb0a3aab719916c3e36d6da7577b0c9060260e65f8`  
		Last Modified: Thu, 17 Mar 2022 04:10:54 GMT  
		Size: 27.2 MB (27153828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f342b2351b9b57710bb425a764682ac3a1c63b960b73f21f487a75360d6fa4d`  
		Last Modified: Fri, 18 Mar 2022 06:26:50 GMT  
		Size: 54.4 MB (54380425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f6aef3a1b41a85ad7a066dac631a878d0e2771ca18aa47c57ae01f7abf3f33`  
		Last Modified: Fri, 18 Mar 2022 06:26:39 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23df580e5e040a4afc2563a8dda503b064f2551e540495ad502db626affe4bf`  
		Last Modified: Fri, 18 Mar 2022 06:26:39 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
