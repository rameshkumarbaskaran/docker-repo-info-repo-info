## `influxdb:latest`

```console
$ docker pull influxdb@sha256:1db410a831ae62beaf59f2d8f6176a37cdd54cd3ffa12d6afc4e86fac8c4aa12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:f04aeb3652581c9c0a085ecc139cb41c55fb96881445bfe550732ebaa439162e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98837102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3457f36e4c3c3c27f81606a051099da0e417ea6ca53d251c5f4a89f1047352e8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 09:11:24 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:11:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fLo /usr/local/bin/yq "https://github.com/mikefarah/yq/releases/download/v4.30.8/yq_linux_${arch}" &&     case ${arch} in       amd64) echo '6c911103e0dcc54e2ba07e767d2d62bcfc77452b39ebaee45b1c46f062f4fd26 /usr/local/bin/yq' ;;       arm64) echo '95092e8b5332890c46689679b5e4360d96873c025ad8bafd961688f28ea434c7 /usr/local/bin/yq' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/yq &&     yq --version
# Thu, 23 Mar 2023 09:11:26 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb
# Thu, 23 Mar 2023 09:11:26 GMT
ENV GOSU_VER=1.12
# Thu, 23 Mar 2023 09:11:29 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Thu, 23 Mar 2023 09:11:55 GMT
ENV INFLUXDB_VERSION=2.6.1
# Thu, 23 Mar 2023 09:11:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz" &&     cp "influxdb2_linux_${arch}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version
# Thu, 23 Mar 2023 09:11:58 GMT
ENV INFLUX_CLI_VERSION=2.6.1
# Thu, 23 Mar 2023 09:12:00 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}/influx" /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Thu, 23 Mar 2023 09:12:01 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Thu, 23 Mar 2023 09:12:01 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 23 Mar 2023 09:12:01 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Thu, 23 Mar 2023 09:12:01 GMT
COPY file:595a669a2c2c2f47df93700fcd3e412750aae40abb979bb4af48a89af97a8b72 in /entrypoint.sh 
# Thu, 23 Mar 2023 09:12:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2023 09:12:01 GMT
CMD ["influxd"]
# Thu, 23 Mar 2023 09:12:01 GMT
EXPOSE 8086
# Thu, 23 Mar 2023 09:12:01 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 23 Mar 2023 09:12:02 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 23 Mar 2023 09:12:02 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 23 Mar 2023 09:12:02 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d55eeb8b14defb8ac4850a09e8ad01f5c4cf5c1e3bc96a4d6ddcb5dd99b2967`  
		Last Modified: Thu, 23 Mar 2023 09:14:07 GMT  
		Size: 6.3 MB (6327646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25ee49adb76883236157ca880b95c0b39a86ffc4928c6cb5d600138d2327b8b`  
		Last Modified: Thu, 23 Mar 2023 09:14:06 GMT  
		Size: 7.0 MB (7049180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444ced87a2669810a478f0be91960e726ec68f41768a5278616dee7e45cdce25`  
		Last Modified: Thu, 23 Mar 2023 09:14:05 GMT  
		Size: 4.1 KB (4108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42dd140e260ecbccf7980d8969186acc4a361852da08029550e9b500459cdb27`  
		Last Modified: Thu, 23 Mar 2023 09:14:05 GMT  
		Size: 982.0 KB (982038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a37d71b80c7bcd176ead26dbff3e1a6e8d88304d00c89c37b977c3d0d83b0d`  
		Last Modified: Thu, 23 Mar 2023 09:14:37 GMT  
		Size: 46.8 MB (46844106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:307bf22ace15dc32ccf8fa3b2419e02cb3616c0b4cc378d5eeecdaa2a0bcd313`  
		Last Modified: Thu, 23 Mar 2023 09:14:33 GMT  
		Size: 6.2 MB (6211621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3c5cb0e3724df630235b56e96b61820cf0a82d823b264c2f5a1ad674d6fa15`  
		Last Modified: Thu, 23 Mar 2023 09:14:32 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d59d88bb98b8eb3b84b40832d3901db1d4ea4ad8023da57808ae273216f3a078`  
		Last Modified: Thu, 23 Mar 2023 09:14:32 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72f2222f33d1bd5aa1249533a3f6e37e5a70fdfad2f6712ee623ce2acce3b8d`  
		Last Modified: Thu, 23 Mar 2023 09:14:32 GMT  
		Size: 6.5 KB (6463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:abddd6d01c57536b34be4bec6e7af0e563a74edf38b945bed3e43a6b54348535
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94794221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f63af630833a4e76010eb8782a25beb019d075506c21066d1ae8a25f26ad2f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:10 GMT
ADD file:83beb883b699cd442f1dbd4baf29c23f4cd15f7a5f9f120979df16a77455c69f in / 
# Thu, 23 Mar 2023 00:45:10 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 09:10:14 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 09:10:15 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fLo /usr/local/bin/yq "https://github.com/mikefarah/yq/releases/download/v4.30.8/yq_linux_${arch}" &&     case ${arch} in       amd64) echo '6c911103e0dcc54e2ba07e767d2d62bcfc77452b39ebaee45b1c46f062f4fd26 /usr/local/bin/yq' ;;       arm64) echo '95092e8b5332890c46689679b5e4360d96873c025ad8bafd961688f28ea434c7 /usr/local/bin/yq' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/yq &&     yq --version
# Thu, 23 Mar 2023 09:10:16 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb
# Thu, 23 Mar 2023 09:10:16 GMT
ENV GOSU_VER=1.12
# Thu, 23 Mar 2023 09:10:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true
# Thu, 23 Mar 2023 09:10:49 GMT
ENV INFLUXDB_VERSION=2.6.1
# Thu, 23 Mar 2023 09:10:52 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz" &&     cp "influxdb2_linux_${arch}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}-linux-${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version
# Thu, 23 Mar 2023 09:10:52 GMT
ENV INFLUX_CLI_VERSION=2.6.1
# Thu, 23 Mar 2023 09:10:54 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     cp "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}/influx" /usr/local/bin/influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version
# Thu, 23 Mar 2023 09:10:54 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Thu, 23 Mar 2023 09:10:54 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 23 Mar 2023 09:10:55 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Thu, 23 Mar 2023 09:10:55 GMT
COPY file:595a669a2c2c2f47df93700fcd3e412750aae40abb979bb4af48a89af97a8b72 in /entrypoint.sh 
# Thu, 23 Mar 2023 09:10:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2023 09:10:55 GMT
CMD ["influxd"]
# Thu, 23 Mar 2023 09:10:55 GMT
EXPOSE 8086
# Thu, 23 Mar 2023 09:10:55 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 23 Mar 2023 09:10:55 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 23 Mar 2023 09:10:55 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 23 Mar 2023 09:10:55 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:fcdb9667c46b09d1c1d058681ea4a1db41e66bbc1a71d873a0c9da4f7a92947d`  
		Last Modified: Thu, 23 Mar 2023 00:48:09 GMT  
		Size: 30.1 MB (30062700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40871433b7864a6c0d657efda2cc53b8cf76c232272114d18e5c2396c63ac2b6`  
		Last Modified: Thu, 23 Mar 2023 09:11:26 GMT  
		Size: 6.3 MB (6308577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13d3802a08020fc6ebf59c0ccf78c1e9f6f60beb4140a800717ca5f23067a10a`  
		Last Modified: Thu, 23 Mar 2023 09:11:25 GMT  
		Size: 6.6 MB (6643026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd72245adc39892c036094c00d370bbeb5f97382ca50ea59f0f9fb34d40b576`  
		Last Modified: Thu, 23 Mar 2023 09:11:24 GMT  
		Size: 4.1 KB (4120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745a7db30e3c11be3091abb0811f7b9428c1af6f2506a38017c133262db389f4`  
		Last Modified: Thu, 23 Mar 2023 09:11:24 GMT  
		Size: 916.9 KB (916930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2edfb878f3e6acfc42bc0a0f9bd87f7704c1f90dab51171cf10daa056ef46b7d`  
		Last Modified: Thu, 23 Mar 2023 09:11:52 GMT  
		Size: 45.1 MB (45145873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5815ee68920d0c61fbb3827691139c57c8e3b04c853aaa473891483e50ca9fe1`  
		Last Modified: Thu, 23 Mar 2023 09:11:50 GMT  
		Size: 5.7 MB (5705996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be0918d2cae7a6bd23c0a9924d61106faba6dead4d70fcb47a902d7645da428`  
		Last Modified: Thu, 23 Mar 2023 09:11:49 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6845d8ca913c8ff0bc6b75058a57db3227629d09b3ffcd7215dc9e30c92141b4`  
		Last Modified: Thu, 23 Mar 2023 09:11:49 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3960a719e7e47aa5b11064519fb3675b1d4f63ea39e4b43d51bf4071bce03bb9`  
		Last Modified: Thu, 23 Mar 2023 09:11:49 GMT  
		Size: 6.5 KB (6463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
