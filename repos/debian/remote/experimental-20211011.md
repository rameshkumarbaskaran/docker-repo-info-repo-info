## `debian:experimental-20211011`

```console
$ docker pull debian@sha256:0704313d5664e5aa845568a273b4fd73da20103b961a9d6607d2ed6468e759cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; s390x

### `debian:experimental-20211011` - linux; s390x

```console
$ docker pull debian@sha256:06c4e0c44afe02e648cdd5531d0280df7023967e12e41ee3272563fa22278ab6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53940915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8619faf1bee4a51e2100d5f39b95cbdaf1adcbe14fa14ca91b1b00a83665d4e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 00:44:52 GMT
ADD file:8e72740308f6ae0d026697be186652e326c16f3f37e6ab6cc86de966dfa8cab4 in / 
# Tue, 12 Oct 2021 00:44:55 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 00:45:11 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:7d3fc62e9c56880d86636919f36507d68aacc14f85a6c05acb3ecfcfedcafb8a`  
		Last Modified: Tue, 12 Oct 2021 00:50:54 GMT  
		Size: 53.9 MB (53940695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64db1ba033328d40f3acc0855295bc14ce0380c1aa79808f1ecbb1dcf9b4bb90`  
		Last Modified: Tue, 12 Oct 2021 00:51:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
