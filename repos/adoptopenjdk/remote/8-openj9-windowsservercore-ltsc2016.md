## `adoptopenjdk:8-openj9-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:a9a8bd413fd86af85f725713f4b1608725e5f598c42b7e994c5ffee6919031e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4046; amd64

### `adoptopenjdk:8-openj9-windowsservercore-ltsc2016` - windows version 10.0.14393.4046; amd64

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
