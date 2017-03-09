.center[

# Superbalist and Kubernetes

![](phlippy_sunset.png)

## A Journey
]

.left[
  `@zoidbergwill`
]

---

class: center

<br>

## <p lang="en" dir="ltr">This is not a zero sum game. People will be using Kubernetes, Swarm, and Mesos for time to come. Don&#39;t be afraid of competition, embrace it.</p>&mdash; Kelsey Hightower (@kelseyhightower) <a href="https://twitter.com/kelseyhightower/status/744946988739756032">June 20, 2016</a>

---

.center[
  # Who Am I Really

  ![:scale 40%](pot-plant.jpg)
]

### William Stewart

#### Site Reliability and DevOps Team at Superbalist.com

- Only cried about Docker 7 times
- Plays French Horn and rides a fixie
- Denies being a hipster
- Yes, I know DevOps isn't supposed to be a person or a team

---

# Who is Superbalist

.center[
  ![:scale 100%](superbalist.png)
]

---

class: center

# Black Friday 2015

<br>

## <i class="fa fa-shopping-basket" aria-hidden="true"></i> <i class="fa fa-shopping-basket superb" aria-hidden="true"></i> <i class="fa fa-shopping-basket" aria-hidden="true"></i> <i class="fa fa-shopping-basket superb" aria-hidden="true"></i> <i class="fa fa-shopping-basket" aria-hidden="true"></i> <i class="fa fa-shopping-basket superb" aria-hidden="true"></i> <i class="fa fa-shopping-basket" aria-hidden="true"></i> <i class="fa fa-shopping-basket superb" aria-hidden="true"></i> <i class="fa fa-shopping-basket" aria-hidden="true"></i> <i class="fa fa-shopping-basket superb" aria-hidden="true"></i> <i class="fa fa-shopping-basket" aria-hidden="true"></i>

<br>

## <i class="fa fa-building" aria-hidden="true"></i> 4 services
## <i class="fa fa-server" aria-hidden="true"></i> ±30 servers

<br>

## <i class="fa fa-shopping-basket superb" aria-hidden="true"></i> <i class="fa fa-shopping-basket" aria-hidden="true"></i> <i class="fa fa-shopping-basket superb" aria-hidden="true"></i> <i class="fa fa-shopping-basket" aria-hidden="true"></i> <i class="fa fa-shopping-basket superb" aria-hidden="true"></i> <i class="fa fa-shopping-basket" aria-hidden="true"></i> <i class="fa fa-shopping-basket superb" aria-hidden="true"></i> <i class="fa fa-shopping-basket" aria-hidden="true"></i> <i class="fa fa-shopping-basket superb" aria-hidden="true"></i> <i class="fa fa-shopping-basket" aria-hidden="true"></i> <i class="fa fa-shopping-basket superb" aria-hidden="true"></i>

---

# HA can mean wasted resources

.center[
  ![:scale 90%](resource-usage.png)
]

---

# Sharing is better

.center[
  ![:scale 90%](better-resource-usage.png)
]

---

class: center

# Docker

![](phlippy_and_whale.png)

---

# What is Docker?

<br>

.center[
  ![:scale 48%](what-is-vm-diagram.png) ![:scale 48%](what-is-docker-diagram.png)
]

---

# What Docker gives us?

## The `Dockerfile`

```
FROM python
ADD src/requirements.txt .
RUN pip install -r requirements.txt --no-cache-dir
ADD src .
```

---

class: center, middle

# Kubernetes

![](phlippy_cloning.png)

---

class: center, middle

# What is Kubernetes?

.center[
  ![:scale 60%](logo_with_border.png)
]

---

# A Kubernetes Overview

![](k8s_architecture_overview.png)

---

# Running an Example App

![:scale 90%](examples/docker_counter_dashboard.png)

---

class: center, middle

# Kubernetes Primitives

# Deployments

![](resource-breakdown.png)

---

class: center, middle

# Kubernetes Primitives

# Services

---

class: center

# Kubernetes at Superbalist

![](phlippy_whale_captain_kube.png)

---

class: center

# 2016 and Beyond

<br>

## <i class="fa fa-shopping-basket" aria-hidden="true"></i> <i class="fa fa-shopping-basket superb" aria-hidden="true"></i> <i class="fa fa-shopping-basket" aria-hidden="true"></i> <i class="fa fa-shopping-basket superb" aria-hidden="true"></i> <i class="fa fa-shopping-basket" aria-hidden="true"></i> <i class="fa fa-shopping-basket superb" aria-hidden="true"></i> <i class="fa fa-shopping-basket" aria-hidden="true"></i> <i class="fa fa-shopping-basket superb" aria-hidden="true"></i> <i class="fa fa-shopping-basket" aria-hidden="true"></i> <i class="fa fa-shopping-basket superb" aria-hidden="true"></i> <i class="fa fa-shopping-basket" aria-hidden="true"></i>

<br>

## <i class="fa fa-building" aria-hidden="true"></i> ±15 services
## <i class="fa fa-server" aria-hidden="true"></i> &lt;20 servers
## ⎈ 80% into Kubernetes

<br>

## <i class="fa fa-shopping-basket superb" aria-hidden="true"></i> <i class="fa fa-shopping-basket" aria-hidden="true"></i> <i class="fa fa-shopping-basket superb" aria-hidden="true"></i> <i class="fa fa-shopping-basket" aria-hidden="true"></i> <i class="fa fa-shopping-basket superb" aria-hidden="true"></i> <i class="fa fa-shopping-basket" aria-hidden="true"></i> <i class="fa fa-shopping-basket superb" aria-hidden="true"></i> <i class="fa fa-shopping-basket" aria-hidden="true"></i> <i class="fa fa-shopping-basket superb" aria-hidden="true"></i> <i class="fa fa-shopping-basket" aria-hidden="true"></i> <i class="fa fa-shopping-basket superb" aria-hidden="true"></i>


---

class: center, middle

# Black Friday (in the war room)

```
$ gcloud container clusters resize hive --size="one billion"
$ kubectl scale deployment/website --replicas 500
```

---

class: center, middle, title

# 2015
# November

---

class: center

# Dev vs. Ops Experience

![](phlippy_ghosts.png)

---

# Deployment evolution

## sed

```
sed "s@image: ${DEPLOYED_IMAGE_URL}@image: ${NEW_IMAGE_URL}@"
```
## envsubst

```
envsubst deployment.yml.template
```

## jinja2 (with j2-cli)

---

class: center, middle, title

# Ephemeral containers

---

class: center, middle, title

# Migrations

---

class: center, middle, title

# 2016
# Part 1

---

class: center, middle, title

# Local Dev

---

class: center, middle, title

# Storage volumes

---

class: center, middle, title

# 2016
# Part 2

---

class: center, middle, title

# Logging

---

class: center, middle, title

# Cron

<br>

## and

<br>

# Long Running Processes

---

# Init Systems

`CMD "python my_server.py"`
![](dumb-init-scenario-1.png)
`CMD ["python", "my_server.py"]`
![](dumb-init-scenario-2.png)
`CMD ["dumb-init", "python", "my_server.py"]`
![](dumb-init-scenario-3.png)

---

class: center, middle, title

# 2017
# Part 1

---

class: center, middle, title

# Build-time secrets

---

class: center, middle, title

# Questions

<br>
<br>

[<i class="fa fa-slack" aria-hidden="true"></i> @zoidbergwill on Slack: zatech.co.za](http://zatech.co.za)

[<i class="fa fa-twitter" aria-hidden="true"></i> twitter.com/zoidbergwill](http://twitter.com/zoidbergwill)

[<i class="fa fa-github" aria-hidden="true"></i> github.com/zoidbergwill](http://github.com/zoidbergwill)

<i class="fa fa-pied-piper-pp" aria-hidden="true"></i> `zoidbergwill` basically everywhere

<br>
<br>

### [zoidbergwill.com/presentations/2017/kubernetes-scaleconf/](http://zoidbergwill.github.io/presentations/2017/kubernetes-scaleconf/)

