## `adoptopenjdk:11-openj9-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:77aaffeee357aa3f7a5a1a0f175ddc06a9e41f7575b1267ba98b066bce3ed482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64

### `adoptopenjdk:11-openj9-windowsservercore-ltsc2016` - windows version 10.0.14393.3506; amd64

```console
$ docker pull adoptopenjdk@sha256:de7dd460c21310881bfdb1b10b1166dbc51d9c0976476d1a5dd35c0b8e75e7d3
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 GB (6116679217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a142d1b71549800d2c37a6dfae705a0d467c7b456995d7a0620f32058924c9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 01:48:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2020 11:21:14 GMT
ENV JAVA_VERSION=jdk-11.0.6+10_openj9-0.18.1
# Thu, 20 Feb 2020 11:24:41 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10_openj9-0.18.1/OpenJDK11U-jdk_x64_windows_openj9_11.0.6_10_openj9-0.18.1.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10_openj9-0.18.1/OpenJDK11U-jdk_x64_windows_openj9_11.0.6_10_openj9-0.18.1.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (6297191f89d9905248c2f9b638ede5ed3dbc79eb9ac3587eb4139631479fa1ba) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '6297191f89d9905248c2f9b638ede5ed3dbc79eb9ac3587eb4139631479fa1ba') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Thu, 20 Feb 2020 11:24:43 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
# Thu, 20 Feb 2020 11:24:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:72c4471958f7f0f07260f0f430bcffb0bc07811088c24cffba1439d250ea1ae3`  
		Last Modified: Thu, 20 Feb 2020 03:04:52 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146e8c0b38e70e19fda5b583ba73373c7ed592e74680e53ea7c2451817fd73a9`  
		Last Modified: Thu, 20 Feb 2020 12:07:05 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3203dce7107d3f34192642ecdf95d86112658473abc3a83c8eb574914481fb`  
		Last Modified: Thu, 20 Feb 2020 12:07:40 GMT  
		Size: 389.6 MB (389609397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28705aecf8f9ca5e3a90d650ab7229dbc93cca219c1ede9db627848e83e7b117`  
		Last Modified: Thu, 20 Feb 2020 12:07:06 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425d7337ee92e80956e92548b6825900d3b2b9952f80ecbbc891e9b453ea2b3f`  
		Last Modified: Thu, 20 Feb 2020 12:07:05 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
