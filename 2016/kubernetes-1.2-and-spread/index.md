# What this talk isn't

- An advanced / in-depth look at Kubernetes

  (Unfortunately we don't have the time)

  Hopefully this will be a decent foundation

- A comparison of Kubernetes vs:
  - Mesos/Marathon
  - ECS
  - Helios
  - Swarmkit

- <p lang="en" dir="ltr">This is not a zero sum game. People will be using Kubernetes, Swarm, and Mesos for time to come. Don&#39;t be afraid of competition, embrace it.</p>&mdash; Kelsey Hightower (@kelseyhightower) <a href="https://twitter.com/kelseyhightower/status/744946988739756032">June 20, 2016</a>


---

# What is Docker?

Docker is a simple standard way of building applications into containers, which means we can build and test the same Docker containers that we are running in production.

Containers are a lighter and more portable version of virtualisation compared to virtual machines.

.center[
![Docker](what-is-docker-diagram.png) ![VM](what-is-vm-diagram.png)]

---

# Running Docker in production

.center[
![Docker in production](docker-production.jpg)]

class: center, middle

# Container cluster managers
# can help

---

# Automate the boring stuff

> “Automation is a force multiplier, not a panacea”

## Value of automation
  - Consistency
  - Extensibility
  - MTTR (Mean Time To Repair)
  - Faster non-repair actions
  - Time savings

.bottom.right[
[Dan Luu's Notes on Google's Site Reliability Engineering book](http://danluu.com/google-sre-book/)]

---

# Enter Kubernetes

![Cluster overview](image_13.png)

---

# How does it help?

- Container hosting
- Config changes
- Supervision
- Monitoring
- Rolling deployments
- Networking
- and more...

---

# The building blocks

### `Node`

- Containers have to run somwehere

- All machines that talk to the Kubernetes API Server, and can have pods
scheduled on them

- They can have unique `label`s which can be useful, for different sized
  boxes, or guaranteeing `Pod`s run on certain `Node`s.

- Whether it's AWS, DigitalOcean, GCP, or your own tin, they're destined
  to die some day.

# War stories

- Memcached
- Kafka
- Migrations
- Accurate local dev
- Logging
- Cron
- Long running processes
- Signal propagation



