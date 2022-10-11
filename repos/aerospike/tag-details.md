<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:ce-6.1.0.3`](#aerospikece-6103)
-	[`aerospike:ee-6.1.0.3`](#aerospikeee-6103)

## `aerospike:ce-6.1.0.3`

```console
$ docker pull aerospike@sha256:1a4d83a7d1ef1852bf4660a5cfdd4d012d79d754e18c3da5b10973c231119b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ce-6.1.0.3` - linux; amd64

```console
$ docker pull aerospike@sha256:4e1fa1dcc306ed5682107778d5b10adba9ebf17b31f73252d4bcf5fe4a2a0eec
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65139582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0c1705439a3bc52d1ef36792bc6d79848781d6733daff3c4ae5e6b294445f3`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-o","pipefail","-c"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Tue, 11 Oct 2022 17:19:28 GMT
ENV AEROSPIKE_VERSION=6.1.0.3
# Tue, 11 Oct 2022 17:19:52 GMT
ENV AEROSPIKE_SHA256=e4f9c152209547517951b78e42ca0251bd237fe1eba65b7bef81fea94ab653c9
# Tue, 11 Oct 2022 17:19:52 GMT
ENV AS_TINI_SHA256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940
# Tue, 11 Oct 2022 17:19:52 GMT
SHELL [/bin/bash -o pipefail -c]
# Tue, 11 Oct 2022 17:20:06 GMT
RUN export DEBIAN_FRONTEND=noninteractive   && apt-get update -y   && apt-get install -y --no-install-recommends     apt-utils     2>&1 | grep -v "delaying package configuration"   && apt-get install -y --no-install-recommends     binutils     ca-certificates     gettext-base     wget     xz-utils   && wget https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static --progress=bar:force:noscroll -O /usr/bin/as-tini-static 2>&1   && echo "$AS_TINI_SHA256 /usr/bin/as-tini-static" | sha256sum -c -   && chmod +x /usr/bin/as-tini-static   && wget "https://artifacts.aerospike.com/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian11.tgz" --progress=bar:force:noscroll -O aerospike-server.tgz 2>&1   && echo "$AEROSPIKE_SHA256 aerospike-server.tgz" | sha256sum -c -   && mkdir -p aerospike/pkg   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && ar --output aerospike/pkg -x aerospike/aerospike-tools-*.deb   && tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/   && rm -rf aerospike-server.tgz /var/lib/apt/lists/*   && dpkg -r apt-utils binutils ca-certificates wget xz-utils   && dpkg --purge apt-utils binutils ca-certificates wget xz-utils 2>&1   && apt-get purge -y   && apt-get autoremove -y   && find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike   && if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then     mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f /usr/lib/asadm/asinfo ]; then       ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;     fi   fi   && rm -rf /opt/aerospike/bin   && rm -rf aerospike
# Tue, 11 Oct 2022 17:20:07 GMT
COPY file:f497c4c6974a190f79a562efd9c9c0d6b753efe43e62c3fcc2536f74ad08238d in /etc/aerospike/aerospike.template.conf 
# Tue, 11 Oct 2022 17:20:07 GMT
COPY file:e3973656bf47d8e3796d7b5dc7200e68dcaedc877c80f4ebeed9484f3aa315d9 in /entrypoint.sh 
# Tue, 11 Oct 2022 17:20:07 GMT
EXPOSE 3000 3001 3002
# Tue, 11 Oct 2022 17:20:07 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 11 Oct 2022 17:20:07 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e18201e433aaf2ae49a93fc789b51362bdace5b623c3586b3f8059f1138a548`  
		Last Modified: Tue, 11 Oct 2022 17:20:34 GMT  
		Size: 33.7 MB (33717672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38f156994acfed366390e9807014040eadc9c9ad96191e32f5957c38793e103`  
		Last Modified: Tue, 11 Oct 2022 17:20:30 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9bb39d998a7608e5b20005e90d405312aaf22e1df291cc63dc901cfd5e0e37`  
		Last Modified: Tue, 11 Oct 2022 17:20:30 GMT  
		Size: 790.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:ee-6.1.0.3`

```console
$ docker pull aerospike@sha256:912a5d1e17d22977c3b78771a9d07d37e168db61f4308360c1160e9efff9faa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ee-6.1.0.3` - linux; amd64

```console
$ docker pull aerospike@sha256:983e4d1ded6bbe2f25890e8b173ec0b67955f1929a1584a464b29703408453a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68176027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edf97063cc1c0edaab7b6181206b851e4dbf797b1b962df438257229f91df230`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-o","pipefail","-c"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Tue, 11 Oct 2022 17:19:28 GMT
ENV AEROSPIKE_VERSION=6.1.0.3
# Tue, 11 Oct 2022 17:19:28 GMT
ENV AEROSPIKE_SHA256=de62082abe7c5fb040fc5eaaed22274142d96cbcd7dfce7530a52d65bce8b277
# Tue, 11 Oct 2022 17:19:28 GMT
ENV AS_TINI_SHA256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940
# Tue, 11 Oct 2022 17:19:28 GMT
SHELL [/bin/bash -o pipefail -c]
# Tue, 11 Oct 2022 17:19:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive   && apt-get update -y   && apt-get install -y --no-install-recommends     apt-utils     2>&1 | grep -v "delaying package configuration"   && apt-get install -y --no-install-recommends     binutils     ca-certificates     gettext-base     wget     xz-utils   && apt-get install -y --no-install-recommends     libcurl4     libldap-2.4.2   && wget https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static --progress=bar:force:noscroll -O /usr/bin/as-tini-static 2>&1   && echo "$AS_TINI_SHA256 /usr/bin/as-tini-static" | sha256sum -c -   && chmod +x /usr/bin/as-tini-static   && wget "https://artifacts.aerospike.com/aerospike-server-enterprise/${AEROSPIKE_VERSION}/aerospike-server-enterprise-${AEROSPIKE_VERSION}-debian11.tgz" --progress=bar:force:noscroll -O aerospike-server.tgz 2>&1   && echo "$AEROSPIKE_SHA256 aerospike-server.tgz" | sha256sum -c -   && mkdir -p aerospike/pkg   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && ar --output aerospike/pkg -x aerospike/aerospike-tools-*.deb   && tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/   && rm -rf aerospike-server.tgz /var/lib/apt/lists/*   && dpkg -r apt-utils binutils ca-certificates wget xz-utils   && dpkg --purge apt-utils binutils ca-certificates wget xz-utils 2>&1   && apt-get purge -y   && apt-get autoremove -y   && find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike   && if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then     mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f /usr/lib/asadm/asinfo ]; then       ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;     fi   fi   && rm -rf /opt/aerospike/bin   && rm -rf aerospike
# Tue, 11 Oct 2022 17:19:47 GMT
COPY file:f56e2e33c0b4bb66affff75053eaed44661e723b8b33d3ef3c10e305b506c350 in /etc/aerospike/aerospike.template.conf 
# Tue, 11 Oct 2022 17:19:47 GMT
COPY file:954d06187376ade36d0a4daf43c9abe4806362f2f33f0bd9dbaef5a67c967bd3 in /entrypoint.sh 
# Tue, 11 Oct 2022 17:19:47 GMT
EXPOSE 3000 3001 3002
# Tue, 11 Oct 2022 17:19:47 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 11 Oct 2022 17:19:48 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f469d17a76e5018b1dde076dfb15c79f600d82691a914755823a05945f6027`  
		Last Modified: Tue, 11 Oct 2022 17:20:22 GMT  
		Size: 36.8 MB (36754062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3430b11da570f5f78c257986c105956e620c2db1f90cb1b60c0323d3ba075c02`  
		Last Modified: Tue, 11 Oct 2022 17:20:17 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c70dff27ef082bcacb7dc4667d86370938ddd6776611991a5a2ce8adc5f039`  
		Last Modified: Tue, 11 Oct 2022 17:20:17 GMT  
		Size: 819.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
