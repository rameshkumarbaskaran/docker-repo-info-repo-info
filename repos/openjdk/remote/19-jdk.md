## `openjdk:19-jdk`

```console
$ docker pull openjdk@sha256:1569b627c19d534976fb20a38b4f3d94be94dc3bade1dac9590e8e657d6cb2d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.473; amd64
	-	windows version 10.0.17763.2458; amd64

### `openjdk:19-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:7e56319a4126163b3e40a6d4fcf83ab44cc255d904f23c2d43fb8b10ff9835ab
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.2 MB (245232685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb45a44e9e6b5fa554a374ba88d654101386a84c84fe70ea6cff03c8453061c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 Dec 2021 02:20:57 GMT
ADD file:15b307e0b1aafead42c103e34d3e51a271acea1ab0b68961e239f11af3b0d179 in / 
# Thu, 23 Dec 2021 02:20:57 GMT
CMD ["/bin/bash"]
# Thu, 23 Dec 2021 02:37:54 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 23 Dec 2021 02:37:55 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Thu, 23 Dec 2021 02:37:55 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Dec 2021 02:37:55 GMT
ENV LANG=C.UTF-8
# Wed, 19 Jan 2022 20:37:50 GMT
ENV JAVA_VERSION=19-ea+5
# Wed, 19 Jan 2022 20:38:08 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/5/GPL/openjdk-19-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='bb5a59a9573422be1df23754d298fce48e8d530e78af478756f219b2a8df34e1'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/5/GPL/openjdk-19-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='27ef9cda6adaf16f8b57abfbdff8dbfef8a0ece62a0e47c0744f5e8dba8fb354'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 19 Jan 2022 20:38:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:155aced2666332ddff5a741b0236f360820e7aa3fc3dde2224fc17a91fc48db6`  
		Last Modified: Thu, 23 Dec 2021 02:21:56 GMT  
		Size: 42.1 MB (42105152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5901c58ecb29b61159b5e3a63dfbb0fb520b2de1d33c9fb038d9b697e3fcd4`  
		Last Modified: Thu, 23 Dec 2021 02:45:32 GMT  
		Size: 13.5 MB (13520734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9458456eba0e7d1f816edbc249383e0e2862931277ba87a6a81f337e367e3a`  
		Last Modified: Wed, 19 Jan 2022 20:50:23 GMT  
		Size: 189.6 MB (189606799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:30fabe45193ce63e758dcf90ec208a19d32fc8ff0c51acfb514b1becf17c0e9f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.9 MB (244852313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3157e0c58862609721c095e65dd5e54d89f457a7516fe971c32081e9d2d59352`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 Dec 2021 02:40:45 GMT
ADD file:140d632303428d802f77f473aef33fa52daacdfc76b23edde4344be661c1d4b0 in / 
# Thu, 23 Dec 2021 02:40:46 GMT
CMD ["/bin/bash"]
# Thu, 23 Dec 2021 02:58:38 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 27 Dec 2021 17:43:38 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Mon, 27 Dec 2021 17:43:39 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Dec 2021 17:43:40 GMT
ENV LANG=C.UTF-8
# Wed, 19 Jan 2022 20:52:14 GMT
ENV JAVA_VERSION=19-ea+5
# Wed, 19 Jan 2022 20:52:26 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/5/GPL/openjdk-19-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='bb5a59a9573422be1df23754d298fce48e8d530e78af478756f219b2a8df34e1'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/5/GPL/openjdk-19-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='27ef9cda6adaf16f8b57abfbdff8dbfef8a0ece62a0e47c0744f5e8dba8fb354'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 19 Jan 2022 20:52:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53f096d4aa0757c30613f325df1e03a90db9d9879ea251b394e3ab0a068b5610`  
		Last Modified: Thu, 23 Dec 2021 02:41:44 GMT  
		Size: 42.0 MB (42018351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921862a08fd8bc652539d62804daf06ab6464bd5b42061f5bedbdfa73bd62136`  
		Last Modified: Thu, 23 Dec 2021 03:11:46 GMT  
		Size: 14.3 MB (14303905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1896aa679bf26dd622f45bd872c0f205ca95209f0a88cf0722670f12f6df5b`  
		Last Modified: Wed, 19 Jan 2022 21:09:38 GMT  
		Size: 188.5 MB (188530057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-jdk` - windows version 10.0.20348.473; amd64

```console
$ docker pull openjdk@sha256:fbf5ff63e65002c3994fd6c1c7ee078d817b39d873e8f784a95d6fd58a3cdbc6
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2394012649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b46d851e5ff1352747083fec25a4fd89a5ebeac200fec1cd4a0af800b24056e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 16 Jan 2022 05:17:24 GMT
RUN Install update ltsc2022-amd64
# Wed, 19 Jan 2022 22:21:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 19 Jan 2022 22:23:11 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 19 Jan 2022 22:23:13 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 19 Jan 2022 22:23:50 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 19 Jan 2022 22:23:51 GMT
ENV JAVA_VERSION=19-ea+5
# Wed, 19 Jan 2022 22:23:52 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/5/GPL/openjdk-19-ea+5_windows-x64_bin.zip
# Wed, 19 Jan 2022 22:23:54 GMT
ENV JAVA_SHA256=f26cae210cb484a48c086f2207018482162d2dd793fb69cc5575dc575159ee1c
# Wed, 19 Jan 2022 22:25:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 19 Jan 2022 22:25:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0e02c12b1310e6c76c29fcd6f81905400fdb6a01caac9dc825939ad004baffef`  
		Size: 955.8 MB (955800778 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2e1f45a873642f0aab3474828d75469362741244e7c714068ac1afe056102cd6`  
		Last Modified: Thu, 20 Jan 2022 00:40:19 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa436893917b4b24f7020ae30c97fa33ab983d9c24e6fd7534d56f8b19bf786f`  
		Last Modified: Thu, 20 Jan 2022 02:19:54 GMT  
		Size: 601.2 KB (601200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039cc436f8de7b22962fef11f63ff7fb05b1dad02d0b04d62c514a24ef045cf9`  
		Last Modified: Thu, 20 Jan 2022 02:19:54 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880009a6e2005dbfbbe934f1896114d21a0e91c8bdaffaee2d5349c8e9de467f`  
		Last Modified: Thu, 20 Jan 2022 02:19:54 GMT  
		Size: 506.3 KB (506304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6476e989f4ef1c0105bcbfdb2e49a2f9a8e2c38c7965632f12874d53f966a3ac`  
		Last Modified: Thu, 20 Jan 2022 02:19:51 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e9e6382144fac92b0302de50ef80abed74492f950559f445c07fb619328fa5`  
		Last Modified: Thu, 20 Jan 2022 02:19:51 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d1ae9e8e1f91816db321b537dae2215fafc5c28edad901672074520af94d9bb`  
		Last Modified: Thu, 20 Jan 2022 02:19:51 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d459a2a2f0391e238a8490c233e0cecf0215497acbf0e2b113235bc36a47934`  
		Last Modified: Thu, 20 Jan 2022 02:20:13 GMT  
		Size: 185.4 MB (185396804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f67526579a95197c298e3d91e454074a2bf71e07bc9b281dcbb6c6f9345b112`  
		Last Modified: Thu, 20 Jan 2022 02:19:51 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-jdk` - windows version 10.0.17763.2458; amd64

```console
$ docker pull openjdk@sha256:086ac9333baa6a4f98696effa9ef688bc2621ac379aa8f293cce9da656420cea
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2899183812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927efc65e419ae881333934b6a2d79cbe28c03b241fcf45afd02ad62b7b025fb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Wed, 19 Jan 2022 23:21:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 19 Jan 2022 23:23:41 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 19 Jan 2022 23:23:42 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 19 Jan 2022 23:24:43 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 19 Jan 2022 23:24:44 GMT
ENV JAVA_VERSION=19-ea+5
# Wed, 19 Jan 2022 23:24:46 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/5/GPL/openjdk-19-ea+5_windows-x64_bin.zip
# Wed, 19 Jan 2022 23:24:47 GMT
ENV JAVA_SHA256=f26cae210cb484a48c086f2207018482162d2dd793fb69cc5575dc575159ee1c
# Wed, 19 Jan 2022 23:26:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 19 Jan 2022 23:26:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba7b1090ce9545f6aac90d390785f6c5e3846304cb7596289dfc36c169d7b1da`  
		Last Modified: Thu, 20 Jan 2022 00:40:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98c73c8d54eeae51e9c93499966b4413ea63f218bdf175bed7b7d83c76e6d58`  
		Last Modified: Thu, 20 Jan 2022 02:20:37 GMT  
		Size: 357.3 KB (357347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64554bb59fd3345200ae4e79426f465295d19e9d1be31e0f5a60f5ddc13af5b2`  
		Last Modified: Thu, 20 Jan 2022 02:20:37 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec53942b6c9dd8e8c55c8a2268d1a09a715d75e3edcf063826fa7462dcdb7c2`  
		Last Modified: Thu, 20 Jan 2022 02:20:37 GMT  
		Size: 310.5 KB (310471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d141803c8aab02129e988faf86c371d9b668e48eca86018fc286832474e30c41`  
		Last Modified: Thu, 20 Jan 2022 02:20:34 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb1987e1022766c5d2f165a31c73811ef92d4355641df7c1ddbdcec622af64f`  
		Last Modified: Thu, 20 Jan 2022 02:20:34 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b640b981a509de2f8f450f072f57ab99586f4006ae9bb091972dddffffab28`  
		Last Modified: Thu, 20 Jan 2022 02:20:34 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da608d0b4f17679a64e5378495b3e4f43cc83e88714bb05f4eab7c0a39deee0e`  
		Last Modified: Thu, 20 Jan 2022 02:21:01 GMT  
		Size: 185.2 MB (185185994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b539e8137a7eb304fd00a373dda61eeba820ce6e1497f9236a698d64e1691a`  
		Last Modified: Thu, 20 Jan 2022 02:20:34 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
