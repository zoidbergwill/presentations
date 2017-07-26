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
class: title

# Some actual code

---
# Errors

```go
if err != nil {
    return "", err
}
return result, nil
```

or

```go
if err != nil {
    log.Print(err)
}
return result
```

---

# Case statements

```go
switch node.Data {
case "a", "link":
    foundURL = getKeyFromNode(node, "href")
case "img", "script":
    foundURL = getKeyFromNode(node, "src")
case "form":
    foundURL = getKeyFromNode(node, "action")
}
```

---

# Merging arrays

```
urls = append(urls, getURLsFromDOM(c)...)
```

---
# Goroutines

Synchronous function:

```go
sleep(1000)
```

Asynchronous version:
```go
go sleep(1000)
```
---

# Simple syncing

```go
wg := &sync.WaitGroup()
wg.Add(1)
go func() {
    defer wg.Done()
    sleep(1000000)
}
wg.Wait()
```

---
# Channels

Magic, sort of...

```go
select {
msg := <- chan1:
    fmt.Println(msg)
<- doneChannel:
    return
}
```

---
class: center, title

## Fin.