<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:ce-6.0.0.3`](#aerospikece-6003)
-	[`aerospike:ee-6.0.0.3`](#aerospikeee-6003)

## `aerospike:ce-6.0.0.3`

```console
$ docker pull aerospike@sha256:9102853ae92b8cb7b47eec84df292b5bd0a9655947a1065602d0f8b8112288c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ce-6.0.0.3` - linux; amd64

```console
$ docker pull aerospike@sha256:2d4a5f093f42a926f1a65c6e7af8f8706b167cf5be6585f8b8ef56fe4ee3c6c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101867682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:242333c75d5e2bb92e004793d9f42d54f67295f50fa0525ca3e5613f3446a012`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:24 GMT
ADD file:81dbfe4f9df4d280f7580380c0c5c93ba71fedba17b3072d2b7b4bce127f88a9 in / 
# Tue, 02 Aug 2022 01:20:24 GMT
CMD ["bash"]
# Tue, 16 Aug 2022 22:19:18 GMT
ENV AEROSPIKE_VERSION=6.0.0.3
# Tue, 16 Aug 2022 22:19:46 GMT
ENV AEROSPIKE_SHA256=b62a4c56d837f58b2a25d5016706fece4b87007ed84302640d7a5e161289f6e4
# Tue, 16 Aug 2022 22:20:07 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Tue, 16 Aug 2022 22:20:08 GMT
COPY file:f497c4c6974a190f79a562efd9c9c0d6b753efe43e62c3fcc2536f74ad08238d in /etc/aerospike/aerospike.template.conf 
# Tue, 16 Aug 2022 22:20:08 GMT
COPY file:fe302e12e47afe1731a34ed4ed29328c6901a3f2c9e32e307220e65cb76d53a2 in /entrypoint.sh 
# Tue, 16 Aug 2022 22:20:08 GMT
EXPOSE 3000 3001 3002
# Tue, 16 Aug 2022 22:20:08 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Tue, 16 Aug 2022 22:20:08 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:751ef25978b2971e15496369695ba51ed5b1b9aaca7e37b18a173d754d1ca820`  
		Last Modified: Tue, 02 Aug 2022 01:25:00 GMT  
		Size: 27.1 MB (27140083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a6f376cae719526da4332e9de3cf3e5069c454a7c6831424dbc5da6b6e18bc`  
		Last Modified: Tue, 16 Aug 2022 22:20:49 GMT  
		Size: 74.7 MB (74725774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b77b839a244a5e28da1fc56087daed21457deef49764d3cbc1f0d18260fa872`  
		Last Modified: Tue, 16 Aug 2022 22:20:38 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d764caf76af279ac0dcb5d1c1cc8cd57d6d05e22910181e7aea609a26ef04b27`  
		Last Modified: Tue, 16 Aug 2022 22:20:48 GMT  
		Size: 810.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:ee-6.0.0.3`

```console
$ docker pull aerospike@sha256:bd3095ca6a66a71e186554a0dcf22207ee6ba9a02709b94f2ea014c9005c3853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ee-6.0.0.3` - linux; amd64

```console
$ docker pull aerospike@sha256:5821f239b5e9fc57d0ad328ad1ae5c02465fbc686f97d85bdf445950dca65271
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104263409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7364e7040efed5fe31857d90a8e0a441b316f593a0cf5abe2a8ddf972a95c3af`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:24 GMT
ADD file:81dbfe4f9df4d280f7580380c0c5c93ba71fedba17b3072d2b7b4bce127f88a9 in / 
# Tue, 02 Aug 2022 01:20:24 GMT
CMD ["bash"]
# Tue, 16 Aug 2022 22:19:18 GMT
ENV AEROSPIKE_VERSION=6.0.0.3
# Tue, 16 Aug 2022 22:19:18 GMT
ENV AEROSPIKE_SHA256=ad2ecced7bd1a62af43788c2a31d27c3521c48b9065cdb2234d6ead8aa8c0422
# Tue, 16 Aug 2022 22:19:18 GMT
ENV AS_TINI_SHA256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940
# Tue, 16 Aug 2022 22:19:40 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps wget python python3 python3-distutils lua5.2 gettext-base libldap-dev libcurl4-openssl-dev   && wget https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static -O /usr/bin/as-tini-static   && echo "$AS_TINI_SHA256 /usr/bin/as-tini-static" | sha256sum -c -   && chmod +x /usr/bin/as-tini-static   && wget "https://download.aerospike.com/artifacts/aerospike-server-enterprise/${AEROSPIKE_VERSION}/aerospike-server-enterprise-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Tue, 16 Aug 2022 22:19:41 GMT
COPY file:f56e2e33c0b4bb66affff75053eaed44661e723b8b33d3ef3c10e305b506c350 in /etc/aerospike/aerospike.template.conf 
# Tue, 16 Aug 2022 22:19:41 GMT
COPY file:697e2123680798e87da7a3f98d1d70e76ffec66f0e1aafa90ff25047a11cca52 in /entrypoint.sh 
# Tue, 16 Aug 2022 22:19:41 GMT
EXPOSE 3000 3001 3002
# Tue, 16 Aug 2022 22:19:41 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 16 Aug 2022 22:19:41 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:751ef25978b2971e15496369695ba51ed5b1b9aaca7e37b18a173d754d1ca820`  
		Last Modified: Tue, 02 Aug 2022 01:25:00 GMT  
		Size: 27.1 MB (27140083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0937189fde642eff71608b4e421c3813176ecad280e30bdc76bf18d67d47556a`  
		Last Modified: Tue, 16 Aug 2022 22:20:31 GMT  
		Size: 77.1 MB (77121443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9933709a547cf3c030de79fb03a66769f12bccfbe0e52ded94204859830ccbeb`  
		Last Modified: Tue, 16 Aug 2022 22:20:31 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc82dd8fbbbe4398453bca16155d3b61d06786d831fa00764ffcd4daa078412`  
		Last Modified: Tue, 16 Aug 2022 22:20:30 GMT  
		Size: 840.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
