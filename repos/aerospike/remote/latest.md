## `aerospike:latest`

```console
$ docker pull aerospike@sha256:bec37c05778109490852addfd4ecb9f6e9f28954d2394dce1fe0761b6b66ea5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:f9f43284ed183edc0bf5dfe579f29762205dd80590fd224ee488a1875b3ca0d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53088497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c7b04c8a515e75449bcce27628e6db13fe76d731af0d8fe6f18b1710629543`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Wed, 22 Jul 2020 02:07:07 GMT
ADD file:c11db0b135382f4c5b0f55b50740639bd8c1a22153b931b409cb9e41136734f2 in / 
# Wed, 22 Jul 2020 02:07:07 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:21:44 GMT
ENV AEROSPIKE_VERSION=5.0.0.10
# Wed, 22 Jul 2020 03:21:44 GMT
ENV AEROSPIKE_SHA256=cf56e1dfabf73508491c669a9eaf32b97ddb91863e4bd78cd0cec64bc53fd0ca
# Wed, 22 Jul 2020 03:22:03 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Wed, 22 Jul 2020 03:22:04 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Wed, 22 Jul 2020 03:22:04 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Wed, 22 Jul 2020 03:22:05 GMT
VOLUME [/opt/aerospike/data]
# Wed, 22 Jul 2020 03:22:05 GMT
EXPOSE 3000 3001 3002 3003
# Wed, 22 Jul 2020 03:22:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Jul 2020 03:22:06 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:cbd31ae332794bb723708526045b062b2fe6a08ccc0f143ea7dc18e0ebe46dea`  
		Last Modified: Wed, 22 Jul 2020 02:12:25 GMT  
		Size: 22.5 MB (22515635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b7e382c7634875697c3a681249e7acae930d310f6555681bc88b170da890ae`  
		Last Modified: Wed, 22 Jul 2020 03:22:40 GMT  
		Size: 30.6 MB (30570810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728cffd6ee0bb3bb8c13cda82e7cd48ed897e936dcb105119bf33fabc189a7d0`  
		Last Modified: Wed, 22 Jul 2020 03:22:35 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92fe2f8f2a722dc44c8bb08e29443a22b5192bafff589d67e74d6844e395186b`  
		Last Modified: Wed, 22 Jul 2020 03:22:34 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
