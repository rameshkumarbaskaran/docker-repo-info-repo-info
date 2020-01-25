## `hylang:python2.7-windowsservercore-ltsc2016`

```console
$ docker pull hylang@sha256:dea4092d5e39a12a223e27abd47ccb06ebcbbfd93eb3784fa1998152c466ec21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3443; amd64

### `hylang:python2.7-windowsservercore-ltsc2016` - windows version 10.0.14393.3443; amd64

```console
$ docker pull hylang@sha256:3c0ce5302ec4f8658920cce9e5e082164447c417735c5a3596e0423c84fdec03
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5789198618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fb7d5c20931aaf6191e78ef7c7f41a18b4a3766e2cd4a707818e4663df42c96`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 02 Jan 2020 15:48:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jan 2020 23:50:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jan 2020 18:25:25 GMT
ENV PYTHON_VERSION=2.7.17
# Wed, 15 Jan 2020 18:25:26 GMT
ENV PYTHON_RELEASE=2.7.17
# Wed, 15 Jan 2020 18:28:02 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}.amd64.msi' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.msi'; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'python.msi', 			'/quiet', 			'/qn', 			'TARGETDIR=C:\Python', 			'ALLUSERS=1', 			'ADDLOCAL=DefaultFeature,Extensions,TclTk,Tools,PrependPath' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.msi -Force; 		Write-Host 'Complete.'
# Sat, 25 Jan 2020 02:34:13 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Sat, 25 Jan 2020 02:34:15 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/42ad3426cb1ef05863521d7988d5f7fec0c99560/get-pip.py
# Sat, 25 Jan 2020 02:34:16 GMT
ENV PYTHON_GET_PIP_SHA256=da288fc002d0bb2b90f6fbabc91048c1fa18d567ad067ee713c6e331d3a32b45
# Sat, 25 Jan 2020 02:36:05 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Sat, 25 Jan 2020 02:37:12 GMT
RUN pip install --no-cache-dir virtualenv
# Sat, 25 Jan 2020 02:37:14 GMT
CMD ["python"]
# Sat, 25 Jan 2020 05:09:32 GMT
ENV HY_VERSION=0.17.0
# Sat, 25 Jan 2020 05:10:44 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Sat, 25 Jan 2020 05:10:46 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31f9df80631e7b5d379647ee7701ff50e009bd2c03b30a67a0a8e7bba4a26f94`  
		Size: 1.7 GB (1654613376 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f1c8c4c99f36cfcf87884a9382011e93fb05fa4002d8f4eca62a43e744db8e95`  
		Last Modified: Wed, 15 Jan 2020 01:46:47 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4287864358145220d2cb16b67268467546ff8efdf51507ec81129f122708a47b`  
		Last Modified: Wed, 15 Jan 2020 18:43:19 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c883f7ca435fbdfe46efa0a8699443e235080d73c839cadb563b2f6da76d4002`  
		Last Modified: Wed, 15 Jan 2020 18:43:16 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53b74241deb5632f2a489ac1f65935c6f2981dcb2346a46c2010417f601b2ce`  
		Last Modified: Wed, 15 Jan 2020 18:44:09 GMT  
		Size: 39.7 MB (39688129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9e6107174ac8b469aad6c34475ddb22052c322490c315d507f742f34d43fe1`  
		Last Modified: Sat, 25 Jan 2020 03:14:30 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00c4e5f1c807b42e17046360ff37fe2f0d6dba3374c7183f7193d0fde1635511`  
		Last Modified: Sat, 25 Jan 2020 03:14:27 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5665ece0df64cc6be249e6c81a4e589256201545c17ba09b01d8bdeeb50f58c7`  
		Last Modified: Sat, 25 Jan 2020 03:14:27 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705ecfb9c7ecc65c5a373e0304d3caee9fe9562d2bdc6d3cbf0e6eb92e7243ce`  
		Last Modified: Sat, 25 Jan 2020 03:14:38 GMT  
		Size: 10.0 MB (10047346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1065c826c080c21f898dff89e6d7b390ac98cc06f5cb5903c8e9f75db31c7aa3`  
		Last Modified: Sat, 25 Jan 2020 03:14:30 GMT  
		Size: 8.8 MB (8775265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f52b87793ae0b9a58e9117f5f30cd0d3fb65cdca81cbf96025a0f8c4942ce63e`  
		Last Modified: Sat, 25 Jan 2020 03:14:27 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed07316887684b8111950929d9e579439f6a197ebb1380c4f57cd8276ed08d3`  
		Last Modified: Sat, 25 Jan 2020 05:15:06 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9964cf2ed03a627185ba012b67865f99b4222c5c16cde6281be2d642e36b9c`  
		Last Modified: Sat, 25 Jan 2020 05:15:09 GMT  
		Size: 6.1 MB (6077840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ff49ae8228b46b94869387744eb09172dfc9aa1ed75a2c00baf919b02d3211`  
		Last Modified: Sat, 25 Jan 2020 05:15:06 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
