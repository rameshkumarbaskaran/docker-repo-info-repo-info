## `adoptopenjdk:8u272-b10-jdk-openj9-0.23.0-windowsservercore`

```console
$ docker pull adoptopenjdk@sha256:0201fe08d8fa87643916ac2ad7f2ba473bfb220c20803499f5899ac432c204b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64
	-	windows version 10.0.14393.4046; amd64

### `adoptopenjdk:8u272-b10-jdk-openj9-0.23.0-windowsservercore` - windows version 10.0.17763.1577; amd64

```console
$ docker pull adoptopenjdk@sha256:9cb0f42dcad07bd43bc1ecf80bf3c126bcf0c35450a19ee684e6a15d6381bd7e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2613546304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547662cbb44fa0e1d79bca5da81c411144708785cb6976b34b09f520bd6f85da`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 03 Nov 2020 03:11:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Nov 2020 13:26:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Nov 2020 19:22:44 GMT
ENV JAVA_VERSION=jdk8u272-b10_openj9-0.23.0
# Wed, 11 Nov 2020 19:24:39 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u272-b10_openj9-0.23.0/OpenJDK8U-jdk_x64_windows_openj9_8u272b10_openj9-0.23.0.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u272-b10_openj9-0.23.0/OpenJDK8U-jdk_x64_windows_openj9_8u272b10_openj9-0.23.0.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (41cf00609db1291a16105e5284094638fb05522b43978e33bfd705a492768e40) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '41cf00609db1291a16105e5284094638fb05522b43978e33bfd705a492768e40') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 11 Nov 2020 19:24:40 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:680bbdbacf1bcbace70de5087d02d31e9dd7a22feae59f746f54dab46c1d5bda`  
		Size: 669.7 MB (669696346 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:da5a67a9f3a363cb69c8104913a5a58c1c47e8f648a07d057fc28a5f98790e60`  
		Last Modified: Wed, 11 Nov 2020 13:37:50 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d62c618e6da6c9f75458406ac1996ecbb3792fbaca635f5cb1d1386a08725f`  
		Last Modified: Wed, 11 Nov 2020 20:14:07 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055cbc6eb815c0a98a904804ca9b2ea6cc0f37ef1ac920cd97ddd85e8d937010`  
		Last Modified: Wed, 11 Nov 2020 20:14:28 GMT  
		Size: 225.5 MB (225513607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f894ef6c1502ee0a0e421954ae79c5714e31bb4a276d988af8777bf48f28ad`  
		Last Modified: Wed, 11 Nov 2020 20:14:08 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:8u272-b10-jdk-openj9-0.23.0-windowsservercore` - windows version 10.0.14393.4046; amd64

```console
$ docker pull adoptopenjdk@sha256:80bb518611de7b193534e35bab8426e789ee7f2c9265cd047a339e19f1918b2f
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5996868971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54044fe041a2ec2d143edff93ffe2f30ade8a0fc5567e992e9f6694fd27cd361`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 28 Oct 2020 18:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Nov 2020 13:23:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Nov 2020 19:24:55 GMT
ENV JAVA_VERSION=jdk8u272-b10_openj9-0.23.0
# Wed, 11 Nov 2020 19:27:30 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u272-b10_openj9-0.23.0/OpenJDK8U-jdk_x64_windows_openj9_8u272b10_openj9-0.23.0.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u272-b10_openj9-0.23.0/OpenJDK8U-jdk_x64_windows_openj9_8u272b10_openj9-0.23.0.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (41cf00609db1291a16105e5284094638fb05522b43978e33bfd705a492768e40) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '41cf00609db1291a16105e5284094638fb05522b43978e33bfd705a492768e40') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 11 Nov 2020 19:27:31 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4830fb08bc2df7ae80548c349b880c263ea87a7b93e13ecbc77c862b6e179558`  
		Size: 1.7 GB (1700572904 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:126d9a92c0cb7b68c56dec2dd5ba118de9dde3ec6368db734c5135fdf1528a33`  
		Last Modified: Wed, 11 Nov 2020 13:34:53 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319f1a80a3fb588afab62d6dfdae6daa9485cecee6508d06d82a311d734e5b9f`  
		Last Modified: Wed, 11 Nov 2020 20:14:42 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3d37b2da0b65359e65d49266e55398ed680b19093c0883ee7618eab98a596c`  
		Last Modified: Wed, 11 Nov 2020 20:15:02 GMT  
		Size: 226.3 MB (226306750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27628f0456e011de3e7465c1382e94579c242043fc111cf0a2e57a50658dfe1a`  
		Last Modified: Wed, 11 Nov 2020 20:14:42 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
