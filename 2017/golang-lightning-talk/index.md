class: center, inverted, title

<br style="font-size: 36px;">

# A Pythoneer among the Gophers

---
class: center, title

<br style="font-size: 36px;">

![](morning-coffee-3x.gif)

## Came for the gophers
## Stayed for the gophers

---
class: center, title

# Disclaimer

![](opinion.jpg)

---
class: center, title

# Go vs Python

![:scale 40%](Hugging_Gophers.png)

## We don't have to pick a side

---
class: title, inverted

# Why

---
class: title

# Why

They share some strengths:

- Community
- Ecosystem
- Simple
- Influenced by C

---

# The New `curl | bash`

```bash
curl -Lo stuff https://random-thing-on-internet
chmod +x stuff
./stuff
Done!
```

<div class="footer">
Note: Let's hope that isn't doing anything naughty...
</div> 

---

# Why Go?

- No run-time dependencies

--
- Awesome tooling
  - gofmt
  - testing and benchmarking builtin
  - dep?

--
- Good stdlib
  - net/http

--
- Great concurrency primitives
  - go routines
  - channels
  - sync.WaitGroup

---

# Pros or Cons?

- Compilation
- Static typing

---
class: title

# When

.footer[
    Always?
]

--

- "Systems"/networking programming
- CLIs
  - spf13's cobra / urfave's cli
- Microservices
  - stdlib http2
- Utility tools (±10 MB images)
  - Metrics
  - Cache purging
- Static sites

---
class: title

# When I Wouldn't?

- Django is amazing

- Data processing / machine learning

---
class: center, title

## Fin.