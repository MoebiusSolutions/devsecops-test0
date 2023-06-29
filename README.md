# devsecops-test0-solution

__ATTENTION: DO NOT PUBLISH, PUSH, OR SHARE THIS TEST OR YOUR SOLUTION. Zip the solved project folder and email the zip file to HR.__

__Interviewees__: Please solve the following Problems.

__Interviewers__: Please contact Jonathan Trinh <jtrinh27@pm.me> for the solution.

## Prerequisite

1. Install Docker
2. (Optional) Install Go 1.19

---

## Problem 0

Fix the `dockerfile.container0` so that it builds and runs.
Provide the Docker commands you used.

### Solution to Problem 0

```bash
Docker commands used goes here.
```

---

## Problem 1

Fix the `dockerfile.container1` so that it builds.
Run the container by binding the exposed port to the host port `8082`.
Visit the application you've just ran with a web browser and use the path `EZ-E`. Provide the URL you entered into the web brower and the message shown in the web brower.
Provide the Docker commands you used.

### Solution to Problem 1

```bash
Docker commands used goes here.
```

---

## Problem 2

When building a container image, what techniques and best practices can be used for the following:

1. Minimize image size and optimize for build speed.
2. Securing and harding with Users, UID, and GUID.

### Solution to Problem 2

> ?

---

## Problem 3

Answer the following:

1. What is a reverse proxy?
2. Describe how you would use a reverse proxy to secure Problem 1.
3. List 3 opensource or commercial tools that can be used for Static application security testing (SAST) or dynamic application security testing (DAST). How each be used to help secure and harden a application or container image?

### Solution to Problem 3

> ?

---

## Problem 4

Run Nexus 3:

`sudo docker run --rm -d -p 127.0.0.1:8081:8081 -p 127.0.0.1:8089:8089 --name nexus sonatype/nexus3`

Default user is `admin` and the uniquely generated password can be found in the `admin.password` file inside the volume (`/nexus-data/admin.password`).

It can take some time (2-3 minutes) for the service to launch in a new container. You can tail the log to determine once Nexus is ready:

`$ docker logs -f nexus`

After Nexus successfully startsup, login with the uniquely generated password. Step through the Nexus wizard. When prompted to change the password, choose a password of you preference that can easily be remembered (e.g. `password`). For "Configure Anonymouse Access, choose "Disable anonymous access".

### Create a Docker repo

As a `admin`, login and Click the "Server administration and configuration" (gear icon).

On the left side pane, under "Repository", select "Blob Stores", and click "Create Blob Store". Fill in the following fields and click "Save":

- Type: `File`
- Name: `interview-docker-dev-local-blob-store`

On the left side pane, under "Repository", select "Repositories", and click "Create repository". Select `docker (hosted)` and fill in the following fields and click "Create repository":

- Name: `interview-docker-dev-local`
- HTTP: `8089`
- Blob store: `interview-docker-dev-local-blob-store`

Upload the containers you've created in Problem 0 and 1 to this Nexus docker repo. Within this docker repo, put Problem 0 and 1 under their respective `problem0` and `problem1` path. Make sure the container's name and tag are the following:

- Problem 0
  - Name: `container0`
  - Tag: `0.1.3`

- Problem 1
  - Name: `container1`
  - Tag: Today's date with the format `YYYY-MM-DD`

Provide the ___ALL___ Docker commands that solves this problem and a screenshot of the uploaded container image's tag in Nexus.

### Solution to Problem 4

```bash
Docker commands used goes here.
```
