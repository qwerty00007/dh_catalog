---
hide:
  - toc
---

# Security Overview

<link href="https://truecharts.org/_static/trivy.css" type="text/css" rel="stylesheet" />

## Helm-Chart

##### Scan Results

#### Chart Object: littlelink/templates/common.yaml



| Type         |    Misconfiguration ID   |   Check  |  Severity |                   Explaination                   | Links  |
|:----------------|:------------------:|:-----------:|:------------------:|-----------------------------------------|-----------------------------------------|
| Kubernetes Security Check         |    KSV001   |   Process can elevate its own privileges  |  MEDIUM | <details><summary>Expand...</summary> A program inside the container can elevate its own privileges and run as root, which might give the program control over the container and node. <br> <hr> <br> Container &#39;RELEASE-NAME-littlelink&#39; of Deployment &#39;RELEASE-NAME-littlelink&#39; should set &#39;securityContext.allowPrivilegeEscalation&#39; to false </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted">https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted</a><br><a href="https://avd.aquasec.com/misconfig/ksv001">https://avd.aquasec.com/misconfig/ksv001</a><br></details>  |
| Kubernetes Security Check         |    KSV001   |   Process can elevate its own privileges  |  MEDIUM | <details><summary>Expand...</summary> A program inside the container can elevate its own privileges and run as root, which might give the program control over the container and node. <br> <hr> <br> Container &#39;autopermissions&#39; of Deployment &#39;RELEASE-NAME-littlelink&#39; should set &#39;securityContext.allowPrivilegeEscalation&#39; to false </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted">https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted</a><br><a href="https://avd.aquasec.com/misconfig/ksv001">https://avd.aquasec.com/misconfig/ksv001</a><br></details>  |
| Kubernetes Security Check         |    KSV003   |   Default capabilities not dropped  |  LOW | <details><summary>Expand...</summary> The container should drop all default capabilities and add only those that are needed for its execution. <br> <hr> <br> Container &#39;RELEASE-NAME-littlelink&#39; of Deployment &#39;RELEASE-NAME-littlelink&#39; should add &#39;ALL&#39; to &#39;securityContext.capabilities.drop&#39; </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-capabilities-drop-index-all/">https://kubesec.io/basics/containers-securitycontext-capabilities-drop-index-all/</a><br><a href="https://avd.aquasec.com/misconfig/ksv003">https://avd.aquasec.com/misconfig/ksv003</a><br></details>  |
| Kubernetes Security Check         |    KSV003   |   Default capabilities not dropped  |  LOW | <details><summary>Expand...</summary> The container should drop all default capabilities and add only those that are needed for its execution. <br> <hr> <br> Container &#39;autopermissions&#39; of Deployment &#39;RELEASE-NAME-littlelink&#39; should add &#39;ALL&#39; to &#39;securityContext.capabilities.drop&#39; </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-capabilities-drop-index-all/">https://kubesec.io/basics/containers-securitycontext-capabilities-drop-index-all/</a><br><a href="https://avd.aquasec.com/misconfig/ksv003">https://avd.aquasec.com/misconfig/ksv003</a><br></details>  |
| Kubernetes Security Check         |    KSV012   |   Runs as root user  |  MEDIUM | <details><summary>Expand...</summary> &#39;runAsNonRoot&#39; forces the running image to run as a non-root user to ensure least privileges. <br> <hr> <br> Container &#39;autopermissions&#39; of Deployment &#39;RELEASE-NAME-littlelink&#39; should set &#39;securityContext.runAsNonRoot&#39; to true </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted">https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted</a><br><a href="https://avd.aquasec.com/misconfig/ksv012">https://avd.aquasec.com/misconfig/ksv012</a><br></details>  |
| Kubernetes Security Check         |    KSV014   |   Root file system is not read-only  |  LOW | <details><summary>Expand...</summary> An immutable root file system prevents applications from writing to their local disk. This can limit intrusions, as attackers will not be able to tamper with the file system or write foreign executables to disk. <br> <hr> <br> Container &#39;autopermissions&#39; of Deployment &#39;RELEASE-NAME-littlelink&#39; should set &#39;securityContext.readOnlyRootFilesystem&#39; to true </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-readonlyrootfilesystem-true/">https://kubesec.io/basics/containers-securitycontext-readonlyrootfilesystem-true/</a><br><a href="https://avd.aquasec.com/misconfig/ksv014">https://avd.aquasec.com/misconfig/ksv014</a><br></details>  |
| Kubernetes Security Check         |    KSV017   |   Privileged container  |  HIGH | <details><summary>Expand...</summary> Privileged containers share namespaces with the host system and do not offer any security. They should be used exclusively for system containers that require high privileges. <br> <hr> <br> Container &#39;autopermissions&#39; of Deployment &#39;RELEASE-NAME-littlelink&#39; should set &#39;securityContext.privileged&#39; to false </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#baseline">https://kubernetes.io/docs/concepts/security/pod-security-standards/#baseline</a><br><a href="https://avd.aquasec.com/misconfig/ksv017">https://avd.aquasec.com/misconfig/ksv017</a><br></details>  |
| Kubernetes Security Check         |    KSV020   |   Runs with low user ID  |  LOW | <details><summary>Expand...</summary> Force the container to run with user ID &gt; 10000 to avoid conflicts with the host’s user table. <br> <hr> <br> Container &#39;RELEASE-NAME-littlelink&#39; of Deployment &#39;RELEASE-NAME-littlelink&#39; should set &#39;securityContext.runAsUser&#39; &gt; 10000 </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-runasuser/">https://kubesec.io/basics/containers-securitycontext-runasuser/</a><br><a href="https://avd.aquasec.com/misconfig/ksv020">https://avd.aquasec.com/misconfig/ksv020</a><br></details>  |
| Kubernetes Security Check         |    KSV020   |   Runs with low user ID  |  LOW | <details><summary>Expand...</summary> Force the container to run with user ID &gt; 10000 to avoid conflicts with the host’s user table. <br> <hr> <br> Container &#39;autopermissions&#39; of Deployment &#39;RELEASE-NAME-littlelink&#39; should set &#39;securityContext.runAsUser&#39; &gt; 10000 </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-runasuser/">https://kubesec.io/basics/containers-securitycontext-runasuser/</a><br><a href="https://avd.aquasec.com/misconfig/ksv020">https://avd.aquasec.com/misconfig/ksv020</a><br></details>  |
| Kubernetes Security Check         |    KSV021   |   Runs with low group ID  |  LOW | <details><summary>Expand...</summary> Force the container to run with group ID &gt; 10000 to avoid conflicts with the host’s user table. <br> <hr> <br> Container &#39;RELEASE-NAME-littlelink&#39; of Deployment &#39;RELEASE-NAME-littlelink&#39; should set &#39;securityContext.runAsGroup&#39; &gt; 10000 </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-runasuser/">https://kubesec.io/basics/containers-securitycontext-runasuser/</a><br><a href="https://avd.aquasec.com/misconfig/ksv021">https://avd.aquasec.com/misconfig/ksv021</a><br></details>  |
| Kubernetes Security Check         |    KSV021   |   Runs with low group ID  |  LOW | <details><summary>Expand...</summary> Force the container to run with group ID &gt; 10000 to avoid conflicts with the host’s user table. <br> <hr> <br> Container &#39;autopermissions&#39; of Deployment &#39;RELEASE-NAME-littlelink&#39; should set &#39;securityContext.runAsGroup&#39; &gt; 10000 </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-runasuser/">https://kubesec.io/basics/containers-securitycontext-runasuser/</a><br><a href="https://avd.aquasec.com/misconfig/ksv021">https://avd.aquasec.com/misconfig/ksv021</a><br></details>  |
| Kubernetes Security Check         |    KSV030   |   Default Seccomp profile not set  |  LOW | <details><summary>Expand...</summary> The RuntimeDefault/Localhost seccomp profile must be required, or allow specific additional profiles. <br> <hr> <br> Either Pod or Container should set &#39;securityContext.seccompProfile.type&#39; to &#39;RuntimeDefault&#39; </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted">https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted</a><br><a href="https://avd.aquasec.com/misconfig/ksv030">https://avd.aquasec.com/misconfig/ksv030</a><br></details>  |
| Kubernetes Security Check         |    KSV030   |   Default Seccomp profile not set  |  LOW | <details><summary>Expand...</summary> The RuntimeDefault/Localhost seccomp profile must be required, or allow specific additional profiles. <br> <hr> <br> Either Pod or Container should set &#39;securityContext.seccompProfile.type&#39; to &#39;RuntimeDefault&#39; </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted">https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted</a><br><a href="https://avd.aquasec.com/misconfig/ksv030">https://avd.aquasec.com/misconfig/ksv030</a><br></details>  |
| Kubernetes Security Check         |    KSV105   |   Containers must not set runAsUser to 0  |  LOW | <details><summary>Expand...</summary> Containers should be forbidden from running with a root UID. <br> <hr> <br> securityContext.runAsUser should be set to a value greater than 0 </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted">https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted</a><br><a href="https://avd.aquasec.com/misconfig/ksv105">https://avd.aquasec.com/misconfig/ksv105</a><br></details>  |
| Kubernetes Security Check         |    KSV106   |   Container capabilities must only include NET_BIND_SERVICE  |  LOW | <details><summary>Expand...</summary> Containers must drop ALL capabilities, and are only permitted to add back the NET_BIND_SERVICE capability. <br> <hr> <br> container should drop all </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted">https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted</a><br><a href="https://avd.aquasec.com/misconfig/ksv106">https://avd.aquasec.com/misconfig/ksv106</a><br></details>  |
| Kubernetes Security Check         |    KSV106   |   Container capabilities must only include NET_BIND_SERVICE  |  LOW | <details><summary>Expand...</summary> Containers must drop ALL capabilities, and are only permitted to add back the NET_BIND_SERVICE capability. <br> <hr> <br> container should drop all </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted">https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted</a><br><a href="https://avd.aquasec.com/misconfig/ksv106">https://avd.aquasec.com/misconfig/ksv106</a><br></details>  |

## Containers

##### Detected Containers

          tccr.io/truecharts/alpine:v3.16.0@sha256:16dc15f3d61a1e30b1df9f839e53636847b6097286b2b74c637b25fd8264f730
          tccr.io/truecharts/littlelink-server:latest@sha256:1cd27733dfd4896d9b2532a35e0a92db81655dda6f17b3eecf315a747074c2b6

##### Scan Results


#### Container: tccr.io/truecharts/alpine:v3.16.0@sha256:16dc15f3d61a1e30b1df9f839e53636847b6097286b2b74c637b25fd8264f730 (alpine 3.16.0)


**alpine**


| No Vulnerabilities found         |
|:---------------------------------|




#### Container: tccr.io/truecharts/littlelink-server:latest@sha256:1cd27733dfd4896d9b2532a35e0a92db81655dda6f17b3eecf315a747074c2b6 (alpine 3.15.4)


**alpine**


| No Vulnerabilities found         |
|:---------------------------------|



**node-pkg**


| Package         |    Vulnerability   |   Severity  |  Installed Version | Fixed Version |                   Links                   |
|:----------------|:------------------:|:-----------:|:------------------:|:-------------:|-----------------------------------------|
| npm         |    CVE-2022-29244   |   MEDIUM  |  8.5.5 | 8.11.0 | <details><summary>Expand...</summary><a href="https://access.redhat.com/security/cve/CVE-2022-29244">https://access.redhat.com/security/cve/CVE-2022-29244</a><br><a href="https://github.com/advisories/GHSA-hj9c-8jmm-8c52">https://github.com/advisories/GHSA-hj9c-8jmm-8c52</a><br><a href="https://github.com/nodejs/node/pull/43210">https://github.com/nodejs/node/pull/43210</a><br><a href="https://github.com/nodejs/node/releases/tag/v16.15.1">https://github.com/nodejs/node/releases/tag/v16.15.1</a><br><a href="https://github.com/nodejs/node/releases/tag/v17.9.1">https://github.com/nodejs/node/releases/tag/v17.9.1</a><br><a href="https://github.com/nodejs/node/releases/tag/v18.3.0">https://github.com/nodejs/node/releases/tag/v18.3.0</a><br><a href="https://github.com/npm/cli/releases/tag/v8.11.0">https://github.com/npm/cli/releases/tag/v8.11.0</a><br><a href="https://github.com/npm/cli/security/advisories/GHSA-hj9c-8jmm-8c52">https://github.com/npm/cli/security/advisories/GHSA-hj9c-8jmm-8c52</a><br><a href="https://github.com/npm/cli/tree/latest/workspaces/libnpmpack">https://github.com/npm/cli/tree/latest/workspaces/libnpmpack</a><br><a href="https://github.com/npm/cli/tree/latest/workspaces/libnpmpublish">https://github.com/npm/cli/tree/latest/workspaces/libnpmpublish</a><br><a href="https://github.com/npm/npm-packlist">https://github.com/npm/npm-packlist</a><br><a href="https://nvd.nist.gov/vuln/detail/CVE-2022-29244">https://nvd.nist.gov/vuln/detail/CVE-2022-29244</a><br></details>  |
