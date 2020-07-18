## `adoptopenjdk:11-jre-openj9-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:53eb9ab05f4b123873f4495b3b51603a3326a0aff4cecf19bf6368df1fc35f83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `adoptopenjdk:11-jre-openj9-windowsservercore-1809` - windows version 10.0.17763.1339; amd64

```console
$ docker pull adoptopenjdk@sha256:4662acf9e1baece0e42f6e17cfa9f25f3e50a438f90581730061339feb88f33b
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2390291302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a5bd49b15e5506b7cc8d9f6c3cd6f4943fffa2a3288b9fb88cbb4f7ba941a3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Tue, 14 Jul 2020 18:41:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 18 Jul 2020 00:24:17 GMT
ENV JAVA_VERSION=jdk-11.0.8+10_openj9-0.21.0
# Sat, 18 Jul 2020 00:41:14 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10_openj9-0.21.0/OpenJDK11U-jre_x64_windows_openj9_11.0.8_10_openj9-0.21.0.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10_openj9-0.21.0/OpenJDK11U-jre_x64_windows_openj9_11.0.8_10_openj9-0.21.0.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (de1caf30e81fbdc0e128e3e3360cd6245b6dd7b0857224604a810dde47061152) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'de1caf30e81fbdc0e128e3e3360cd6245b6dd7b0857224604a810dde47061152') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 18 Jul 2020 00:41:16 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
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
	-	`sha256:4daee471b24230a5cd78984baebc91527ce3072d7bf9eee3b7513cf18b801912`  
		Last Modified: Sat, 18 Jul 2020 01:18:25 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1d8bc6c7d6aed19a5a506f07e1e3e0dcf724c1e5f4650b655dabe1816e40f0`  
		Last Modified: Sat, 18 Jul 2020 01:19:20 GMT  
		Size: 80.1 MB (80095624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b39795d733c0fc20cadb885aad05fe658290ca9a055f2d9d0718dd3a8b2b219`  
		Last Modified: Sat, 18 Jul 2020 01:19:08 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
