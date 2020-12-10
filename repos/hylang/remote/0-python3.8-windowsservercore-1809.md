## `hylang:0-python3.8-windowsservercore-1809`

```console
$ docker pull hylang@sha256:2390f6c068f4d3563d8e0352b65ab349641625d57585f8f94390b41c8f2aebdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `hylang:0-python3.8-windowsservercore-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull hylang@sha256:c7fe180ceb967dca362f621553e5bfcaf6b2c35927a2325d0b11607e59425e8a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2464648089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57c1e0b2f93fa80afe15b323b79b74390f1c91c72c3f2b95ddda12f49b514c7`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 04 Dec 2020 02:13:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Dec 2020 13:30:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Dec 2020 17:43:53 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 09 Dec 2020 17:57:39 GMT
ENV PYTHON_VERSION=3.8.6
# Wed, 09 Dec 2020 17:57:40 GMT
ENV PYTHON_RELEASE=3.8.6
# Wed, 09 Dec 2020 17:59:22 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Wed, 09 Dec 2020 17:59:23 GMT
ENV PYTHON_PIP_VERSION=20.3.1
# Wed, 09 Dec 2020 17:59:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/91630a4867b1f93ba0a12aa81d0ec4ecc1e7eeb9/get-pip.py
# Wed, 09 Dec 2020 17:59:25 GMT
ENV PYTHON_GET_PIP_SHA256=d48ae68f297cac54db17e4107b800faae0e5210131f9f386c30c0166bf8d81b7
# Wed, 09 Dec 2020 18:00:11 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 09 Dec 2020 18:00:12 GMT
CMD ["python"]
# Thu, 10 Dec 2020 00:01:18 GMT
ENV HY_VERSION=0.19.0
# Thu, 10 Dec 2020 00:02:00 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Thu, 10 Dec 2020 00:02:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aa4f58cd6da1aaf1a0b44d443bd88e7fbe5b0a6f193995a1a61d6bd63990f314`  
		Size: 672.5 MB (672541583 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a4372d14958dc8a7eaaace9e4774e7f1db524da5eb4474b5e46738848a3a61a5`  
		Last Modified: Wed, 09 Dec 2020 13:54:38 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94dd2e25fa016037458dfad84ce68c5f51c1d9a517cbb1d6a9d9037fb27a47b`  
		Last Modified: Wed, 09 Dec 2020 18:12:33 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e6bbd02cb0aefedd3de9d671a02fd71819d4033b938f28da74a28a9e6593bb`  
		Last Modified: Wed, 09 Dec 2020 18:15:45 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8394d17edb2b9bdefcfa838c52a0ae042f8061ee068ecfaedfe1fcd8684cffed`  
		Last Modified: Wed, 09 Dec 2020 18:15:45 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb5b404e3100e0c058788bcd31567c355a123f6ebd821efc7f1a86f089a779f`  
		Last Modified: Wed, 09 Dec 2020 18:15:53 GMT  
		Size: 57.9 MB (57926886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1228aa0c005d69da15b96f38469fdaa405a126e6526bebff399a32ead8fe4312`  
		Last Modified: Wed, 09 Dec 2020 18:15:41 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab851b3d0dd2085ee865eb90aa87e538955caa72fcc950ffbd50d4b678dc4d4d`  
		Last Modified: Wed, 09 Dec 2020 18:15:41 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f5c7d48fbc828b7987c6b6abd86cbcf26ce8dcf0754fb798b678d59e3c1e2d`  
		Last Modified: Wed, 09 Dec 2020 18:15:41 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd1dccc96efb0ca657065ad1b5a8d57aa29d092fd69912e6ab5def477ff0c10`  
		Last Modified: Wed, 09 Dec 2020 18:15:45 GMT  
		Size: 10.3 MB (10304841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00acecdc3029c12656c83987839f62f87e54bc7d2b1ea9e8388693d285ba2cb`  
		Last Modified: Wed, 09 Dec 2020 18:15:41 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1669bbefc17110bf347520aeacf1145a2f4eb5c1bd2658ff8069868d1a5730`  
		Last Modified: Thu, 10 Dec 2020 00:07:21 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc66ecb0eef7c50f7778153c65019d7abed718ce6d56187b05ca57c1adbf3ff`  
		Last Modified: Thu, 10 Dec 2020 00:07:23 GMT  
		Size: 5.5 MB (5530543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdefa3f8745767942f70705ac09d0ae094bbb265b1afb6f27e903fefdd00af6b`  
		Last Modified: Thu, 10 Dec 2020 00:07:21 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
