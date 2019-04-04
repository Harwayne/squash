## How to run it.

1. Put the file `.ko.yaml` in the directory that where `ko` is running. The contents of the file are:

    ```yaml
    defaultBaseImage: ubuntu:bionic-20190307
    ```

1. `ko` apply the binary you are interested in.

1. ```shell
   export TAGGED_VERSION=v0.5.7
   make clean
   make squashctl
   ```

1. Open up VS code in `editor/vscode`.

1. Replace `version` in `editor/vscode/package.json` with a valid semver string (e.g. `0.1.2`).

1. Have `getremote(extPath: string)` in `editor/vscode/src/extension.ts` point at your newly built `squashctl`.

1. 'Debug' the extension from VS code by pressing F5. This will open a new VS Code windown with the local copy of the extension running.

<h1 align="center">
    <img src="https://s3.amazonaws.com/artifacts.solo.io/squash.png" alt="Squash" width="230" height="275">
 </h1>

<h4 align="center">Debug your Kubernetes applications from VS Code.</h4>
<BR><BR>

## What is Squash ?
Squash, a tool for debugging distributed applications, is designed to bring the strength of modern debuggers and the convenience of their IDEs to microservices developers. Squash uses popular, powerful and mature debuggers, and integrates them seamlessly with Kubernetes. This allows devs to use the debugger of their choice, and the IDEs that support it, to debug microservices on Kubernetes.

## What is the Squash extension ?
The Squash VS Code extenstion allows Squash to use Visual Studio Code as its user interface. 
After installing this extension Squash commands are available in VS Code command palette. 

## With Squash, you can:
* Live debugging cross multi microservices
* Debug container in a pod
* Debug a service
* Set breakpoints
* Step through the code
* View and modify values of variables
* and more ...

