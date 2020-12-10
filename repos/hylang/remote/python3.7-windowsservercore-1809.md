## `hylang:python3.7-windowsservercore-1809`

```console
$ docker pull hylang@sha256:0ea4cba6b295e4fb5cf0db9564419153b3616b6964e6c89d10a4a512ce83ab17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `hylang:python3.7-windowsservercore-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull hylang@sha256:d2351279d4c421b7358a2826ff17cf232c131aef33b77f599fb6437c30fa90ee
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2462507757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10d205a16390ae7e27dc1d97f43a7bdbca635cea94459b4e96017c4aee9251f2`
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
# Wed, 09 Dec 2020 18:04:33 GMT
ENV PYTHON_VERSION=3.7.9
# Wed, 09 Dec 2020 18:04:33 GMT
ENV PYTHON_RELEASE=3.7.9
# Wed, 09 Dec 2020 18:06:14 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Wed, 09 Dec 2020 18:06:15 GMT
ENV PYTHON_PIP_VERSION=20.3.1
# Wed, 09 Dec 2020 18:06:16 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/91630a4867b1f93ba0a12aa81d0ec4ecc1e7eeb9/get-pip.py
# Wed, 09 Dec 2020 18:06:17 GMT
ENV PYTHON_GET_PIP_SHA256=d48ae68f297cac54db17e4107b800faae0e5210131f9f386c30c0166bf8d81b7
# Wed, 09 Dec 2020 18:07:02 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 09 Dec 2020 18:07:03 GMT
CMD ["python"]
# Thu, 10 Dec 2020 00:04:06 GMT
ENV HY_VERSION=0.19.0
# Thu, 10 Dec 2020 00:04:43 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Thu, 10 Dec 2020 00:04:44 GMT
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
	-	`sha256:42503025b6e82ddd400c97bfd9a6da7435747297eb8b863eb00220f7f478b452`  
		Last Modified: Wed, 09 Dec 2020 18:17:39 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c475e07ff02e5a10166c8bcdc59cb193113b3911a4e9f93437cd66a1178231a`  
		Last Modified: Wed, 09 Dec 2020 18:17:39 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca1b1d090f4e314e67e439e6419f56577df79cc19b939ee9e8d9e65acd163d0`  
		Last Modified: Wed, 09 Dec 2020 18:17:48 GMT  
		Size: 55.8 MB (55842148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2679005f3bf37c972925edc896496fe44db1d0a2c889a8c2201d29ee189a5be0`  
		Last Modified: Wed, 09 Dec 2020 18:17:36 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffe3a3d697e191a0d02b1210610e412ea393767b2e40a6e59066ab0c1f995ce`  
		Last Modified: Wed, 09 Dec 2020 18:17:36 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69c7d2175e88053a2437fa10e4dbeb1128cb7bf379f01ea308cec9d313adefc`  
		Last Modified: Wed, 09 Dec 2020 18:17:36 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03963520579110660441c33c667140fb39609b27154b470b220794e13c0c0ea`  
		Last Modified: Wed, 09 Dec 2020 18:17:39 GMT  
		Size: 10.3 MB (10261061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f32bd7dbd6b861017c593de4a3d367d238d56a3b0013770cbec49b896f2e41e`  
		Last Modified: Wed, 09 Dec 2020 18:17:36 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e5eed0508720791a7e796e1fb300fe473fb6e39e241092afd772ee3ef134a2`  
		Last Modified: Thu, 10 Dec 2020 00:08:36 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6153042aafffa83d231de8f50da9e5899e6c8d934398c338669e9976ffcb0304`  
		Last Modified: Thu, 10 Dec 2020 00:08:43 GMT  
		Size: 5.5 MB (5518727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba01a8c885d32962d40ba40f80b6df79b3d1fbd5971c5efb03fde6facb9f3ef`  
		Last Modified: Thu, 10 Dec 2020 00:08:37 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
