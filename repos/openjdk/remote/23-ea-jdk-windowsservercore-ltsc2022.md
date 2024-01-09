## `openjdk:23-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:ae2c014a4827664641d666f97ea85cc3d1ab83310060436b0fa2329ec6af896f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2159; amd64

### `openjdk:23-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2159; amd64

```console
$ docker pull openjdk@sha256:e103e34e46d59d3510ac8b2293bcb3f87dd72cc6dd57f1e63fcc799beb2d125c
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2087896841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d425e916e500fb89f5990b9f4cd59982d65c5a210d143c7b238a42c21966e023`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Tue, 09 Jan 2024 00:54:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jan 2024 00:54:26 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 09 Jan 2024 00:54:27 GMT
ENV JAVA_HOME=C:\openjdk-23
# Tue, 09 Jan 2024 00:54:33 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 09 Jan 2024 00:54:33 GMT
ENV JAVA_VERSION=23-ea+4
# Tue, 09 Jan 2024 00:54:34 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/4/GPL/openjdk-23-ea+4_windows-x64_bin.zip
# Tue, 09 Jan 2024 00:54:35 GMT
ENV JAVA_SHA256=14230e6d57a3b39a3b5e232e7095fe1821a48197f75b68ae0f09db29e5391216
# Tue, 09 Jan 2024 00:54:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 09 Jan 2024 00:55:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cbf85ce8f072acb13ef93faa1a9e50f2745e7ce9ca24c01c9599bd36c05a811`  
		Last Modified: Tue, 09 Jan 2024 00:55:09 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2361e729bd839b1dd687dbdc028e76c6957cb0e6bb76515acc937a3b6d7e3837`  
		Last Modified: Tue, 09 Jan 2024 00:55:09 GMT  
		Size: 485.1 KB (485123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f583ef78eb2eabf98a73acdd25d75fd42555678d168354b3f830e7f354b3e5f`  
		Last Modified: Tue, 09 Jan 2024 00:55:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eaf576f9d345c2dc4ce9df2fa682b07ccae2d4118a6a9c023bc1ece20aeb3b1`  
		Last Modified: Tue, 09 Jan 2024 00:55:08 GMT  
		Size: 336.3 KB (336325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5834453b754061fbef5f8c5a94aa88a100851cedcc097dd8edfd676257832889`  
		Last Modified: Tue, 09 Jan 2024 00:55:06 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa8c868a4f6d9291026084d62e1544f09fb01e1efacbac3cc82cc8bef3dbd06`  
		Last Modified: Tue, 09 Jan 2024 00:55:06 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f52c1c24d9744005c56c5d861665f104a66c9cb4567855a611cf86b79ed1c410`  
		Last Modified: Tue, 09 Jan 2024 00:55:05 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5fcf86e3a432edefe3ba3d106de6b88a243381462c8c5c1ee5a0db0c8ac73a5`  
		Last Modified: Tue, 09 Jan 2024 00:55:16 GMT  
		Size: 197.8 MB (197793828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d18c35cf4e077e5faf97eeac0b646511da7c4fc67ea767c23b1bae1592f24a4`  
		Last Modified: Tue, 09 Jan 2024 00:55:05 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
