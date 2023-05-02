## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:4baaada62295c0836a3afd7720bdb890a528833056da420b9b3c6ba43248032a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:2d21ba1f0e9f55e60aec0e4c391bc1ca90d5ee1801b16b30847e8e9d42b8fe19
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49293163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b42a3b8f2261d6be25867ff1df1964c392f850cd4a70159ba2b885ec4bc3598`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:35 GMT
ADD file:1cb6c660a2e3ea14b2a11bb8b80f53920c3da423a0ad7004391bfab4db4d0177 in / 
# Wed, 12 Apr 2023 00:19:36 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:19:39 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cc556c281183180fae02d57fa6fb60ed0a99d9040936278743dc4022bfb0c686`  
		Last Modified: Wed, 12 Apr 2023 00:22:48 GMT  
		Size: 49.3 MB (49292938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b912467d263f30e17a171b9b45ce9f875a6d1a5b431c9f031644052c2145f27a`  
		Last Modified: Wed, 12 Apr 2023 00:22:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:63c0590c4fca207832f2289398b9a7b16607a789126ed57f63d51392efe74d70
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47167424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c33cad8fdf47145896d1114f29b974d9676db8fa76d046cb74ccc8fca6bd04a5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 22:48:29 GMT
ADD file:1ecd266ebf23430d2ea2417b92ebee6029d940fbe99297183c4f811e24fdffb7 in / 
# Tue, 02 May 2023 22:48:32 GMT
CMD ["bash"]
# Tue, 02 May 2023 22:48:34 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cbca433c216350213a8b219e118cb55f422acfc53f49c76c44e044b42a5c0aa6`  
		Last Modified: Tue, 02 May 2023 22:50:27 GMT  
		Size: 47.2 MB (47167199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f12bd05394d7cdb0240b97ff1f8b37890ba3605c9be05a5f0137391f033b4a`  
		Last Modified: Tue, 02 May 2023 22:50:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:4f3ae1bbc920a0e25aa1be4afdcec99f8267725fe48d34868307592bb1800e5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45883342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce3550faf1d683b8578f68270eb38d7c0c07f7048548f01d3a047686030a903a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:10 GMT
ADD file:aa1c08333544c05fc5317d775ee99af7479c6fa5f35b74652f6126a7a5099958 in / 
# Tue, 11 Apr 2023 23:59:11 GMT
CMD ["bash"]
# Tue, 11 Apr 2023 23:59:16 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:81b1dd69f2a38ad14b0919ab9c395aafeb137158539ab6531ac5743690a0ebb7`  
		Last Modified: Wed, 12 Apr 2023 00:02:26 GMT  
		Size: 45.9 MB (45883114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91279df2be4fc54fa107a1489c352c4e6820235721f6d2fce9770dcd788dd23b`  
		Last Modified: Wed, 12 Apr 2023 00:02:34 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:2c2e5b6d8c2df06479ad95ba623cb29ec23bd3b9adadc01ee66f01bd28305610
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49345592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6814ea763798190eca3987817a70a7bc13eb57913ca423f012a79a5fc8b4e4fb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:27 GMT
ADD file:efed18ef2a003bff7e64e7049455216e51876402083581032c35085328e416f6 in / 
# Wed, 12 Apr 2023 00:39:28 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:39:32 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b0f987ce91d920ae0a705ed6c9824f1bbbfa282defb8986614030eb8e2bc0b4e`  
		Last Modified: Wed, 12 Apr 2023 00:41:45 GMT  
		Size: 49.3 MB (49345365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b263e24395ff79fba3574dbdcda1c6a7449a8f599b233b13d651751ee6c469`  
		Last Modified: Wed, 12 Apr 2023 00:41:53 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:1b69101031c40b23221892a619f241319692e3bba4d3557778719ebbd302d439
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50318201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f543f79f68c9d270fa7d7810125f7c293424c6c72a1cc2f78c4f201a5d39408c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:38:30 GMT
ADD file:7718865253a3489583d40f8c7a7beede0c20cebbab68bb3e97ad2e84082afcb7 in / 
# Wed, 12 Apr 2023 00:38:30 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:38:34 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a4ce9e81f634822e5166ef3eef875a4140795ac18afe0391433d72c7865bf67b`  
		Last Modified: Wed, 12 Apr 2023 00:41:43 GMT  
		Size: 50.3 MB (50317977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2ebfdfe5f5fe09aaad696aacc27e759afc03f711b3867a755a7e8d60976b31`  
		Last Modified: Wed, 12 Apr 2023 00:41:51 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:51d60254ade2a3f26c148960aa9cc4e84d93e7057c95f7c7d662215de074a040
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49299550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85c5fc7fe8efbc02051c3a45ded9ac0c75ed645710021436025b7731d2a5f78`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:08:16 GMT
ADD file:6a525220124da7146a3c356cc57678f3b8d7c6e9299febaaebd5b5a005f1325c in / 
# Wed, 12 Apr 2023 00:08:21 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:08:34 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b6bdb9410f81554043d19e5ae83249eaa10ffe038db54932946c7d9eaccc8b96`  
		Last Modified: Wed, 12 Apr 2023 00:15:35 GMT  
		Size: 49.3 MB (49299322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a1043ecd820d689db7a68e952536be338fede5f152559185ae52b314992d71`  
		Last Modified: Wed, 12 Apr 2023 00:15:45 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:5e56ccae3b1e7e733e6cecea378c4d0e188de09325248ac762fc060a80ab6c7b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53300212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746daca5182cd8102027b20e4f425f2b751ab80c5c23090d7f9da458a5e8c659`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:07:22 GMT
ADD file:b747fc06f7ee1d3e19fc9cf3aa83e6ab4caa056a72d230caf616e67849bfe112 in / 
# Wed, 12 Apr 2023 00:07:25 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 00:07:28 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8314f03b76ec928732612641a4f8420e3c4c25719b48503230bf6c03979aeb2e`  
		Last Modified: Wed, 12 Apr 2023 00:11:50 GMT  
		Size: 53.3 MB (53299984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9785fbbebdcc5c8fd5e34ff7ad1f4a56c3e4defce0fd15af015a6930e52109d8`  
		Last Modified: Wed, 12 Apr 2023 00:12:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:e86cee0f7cd4dced279fe1b9e2e5af3a9da36b381c0d88e68a4ae2aad33db27f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47670634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b1d9f76008c7acea5b310397ea20bff9b9157160f0f1796bab476ab62ebcfe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:19 GMT
ADD file:5d2b35b45a0f23e2f2e93f9c311eb34a92e4591ea27979236d801e512d44cb85 in / 
# Tue, 11 Apr 2023 23:59:31 GMT
CMD ["bash"]
# Tue, 11 Apr 2023 23:59:39 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8a09cd2374da8355612e7d4c91d55107a3f089816ae52b2c91b9e08e6a895ab1`  
		Last Modified: Wed, 12 Apr 2023 00:04:39 GMT  
		Size: 47.7 MB (47670407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fccd5749b40f4eca9cb96b5e4e343d8ee1bb6f2f86458a77183862f5bb0b59`  
		Last Modified: Wed, 12 Apr 2023 00:04:44 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
