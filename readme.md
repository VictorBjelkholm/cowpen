# cowpen

Problem trying to solve:

How to deal with node modules in a better way.


## Explicit problems

### How do I use a node package from IPFS?

You can add it by doing `npm install --save lodash@ipfs-hash`

### How do I publish a node package to IPFS?

You do `ipfs add -r .` and take the hash in the end

`cowpen publish ipfs-hash` which adds it to your ipfs-package.json and adds that to IPFS + IPNS

### Where do I find new packages?

There needs to be a central index for discovery. How to build a central index decentralized? No idea

```
cowpen search lodash
# ipfs cat connected-peer/ipfs-packages.json
```

You could rely on `ipfs name publish` to host a local index of packages. So an author is bound to the ID of the IPFS daemon.

You lose the key and you loose your repository of packages.

Publishing would then look like:

```
ipfs add -r .
ipfs name publish ipfs-hash
```


```
cowpen publish 
cowpen install #hash
cowpen 
publish.sh
cowpen init
```