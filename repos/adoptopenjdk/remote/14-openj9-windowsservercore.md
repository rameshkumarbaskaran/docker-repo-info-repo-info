## `adoptopenjdk:14-openj9-windowsservercore`

```console
$ docker pull adoptopenjdk@sha256:49bd517850f256cd8018fbf482f32e07af2de8471f07e53974bdfe2a9942e4fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `adoptopenjdk:14-openj9-windowsservercore` - windows version 10.0.17763.1339; amd64

```console
$ docker pull adoptopenjdk@sha256:aaee374ba4a169df85187b61bce22cc423d7db2f7978fb55eb8b4795d15e26bf
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2703819668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f5c9eb3f8d88fe9575a823e0649fce7d1427d7e34d8b5fdefe952bdb42b810`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Tue, 14 Jul 2020 18:41:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 18 Jul 2020 00:54:24 GMT
ENV JAVA_VERSION=jdk-14.0.2+12_openj9-0.21.0
# Sat, 18 Jul 2020 00:57:10 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12_openj9-0.21.0/OpenJDK14U-jdk_x64_windows_openj9_14.0.2_12_openj9-0.21.0.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12_openj9-0.21.0/OpenJDK14U-jdk_x64_windows_openj9_14.0.2_12_openj9-0.21.0.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (2e496ce7ca02f7a380fd1902e06d55d52121bb2eee29b21b8e54ad3e2fd3466e) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '2e496ce7ca02f7a380fd1902e06d55d52121bb2eee29b21b8e54ad3e2fd3466e') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 18 Jul 2020 00:57:12 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
# Sat, 18 Jul 2020 00:57:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:25edfecb5915de420000d722dc47ef9b13bc344a8330c4300e36a4ec8ca73033`  
		Last Modified: Tue, 14 Jul 2020 19:42:57 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e2ba294f47a8f233fc9dc43dc4b32f4e788b6ca9a10574efdf8d5a279dc2ae`  
		Last Modified: Sat, 18 Jul 2020 01:19:32 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5d0a3d70a1b4d53325870d9b7e47d41451edfc259916dbd1ace567bf04624e`  
		Last Modified: Sat, 18 Jul 2020 01:20:05 GMT  
		Size: 393.6 MB (393622812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dafb69917a39daf92b91f64887f5e64be7ec472d8821ba8c4fcc17b716270da`  
		Last Modified: Sat, 18 Jul 2020 01:19:32 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530d56180976241b7f02354afd682570b6b02e1baa0ef67dc4abde0942b1de76`  
		Last Modified: Sat, 18 Jul 2020 01:19:33 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
