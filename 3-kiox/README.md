# kiox (TBD SOON! I PROMISE!)
A tiny LAN-only declarative package manager compatible with anything. That's all it is.

---

Manifest.kiox example
```
src [
   192.168.x.xxx # for local source
   (literally any fucking protocol/domain name that's compatible) # for global source
]

pkgs [
  Google.Chromium.bin #installs from a compatible binary
  Vim.Vim.src #builds from source if it's got a makefile
  # etc 
]
```

---

Serve.kiox example
```
pkgs [
  NetBSD [
     Google.Chromium.bin /home/server/binaries/Chromium 
     Vim.Vim.src /home/server/src/Vim/*
  ]
  KolibriOS [
     idfk what people install on there
  ]
  # etc
]

fils [
   name /path/to/something 
]
```
---

kiox-get (pkg/fil) (name) -- updates `Manifest.kiox` and downloads any given package/file from the server
kiox-push (pkg/fil) (Author.Name) (path on server) -- updates `Serve.kiox` and adds a file back, if it has the permissions to
