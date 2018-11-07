# ipfs-web

### View the webpage by either way:
* https://gateway.ipfs.io/ipfs/QmYwgL3yVJvPCzxk4v2SKdeSCXofiQuSTxoRCmoxK3YewW
* http://localhost:8080/ipfs/QmYwgL3yVJvPCzxk4v2SKdeSCXofiQuSTxoRCmoxK3YewW
* http://localhost:8080/ipns/QmQnoFHgrF4iMQZqtNTKSeWuXBz9UtoGpsH5Xs4RvB7RNB
* https://gateway.ipfs.io/ipns/QmQnoFHgrF4iMQZqtNTKSeWuXBz9UtoGpsH5Xs4RvB7RNB

P.S.
The hash ending with `ewW` is the hash of `index.html` being deployed to IPFS.
The has ending with `RNB` is my IPFS peer ID. (**`ipns`** instead of `ipfs` in this case)

## Deploy to IPFS

```shell
# Start the IPFS peer
$ ipfs daemon

# Upload the content to the IPFS
$ ipfs add -r index.html
added QmYwgL3yVJvPCzxk4v2SKdeSCXofiQuSTxoRCmoxK3YewW index.html
 357 B / 357 B [=========================================================================================================================================================] 100%
```
After this step, you can view the webpage at `http://gateway.ipfs.io/ipfs/<YOUR_FILE_HASH>`

### Publish using IPNS (InterPlanetary Naming System)
```shell
$ ipfs name publish QmYwgL3yVJvPCzxk4v2SKdeSCXofiQuSTxoRCmoxK3YewW
Published to QmQnoFHgrF4iMQZqtNTKSeWuXBz9UtoGpsH5Xs4RvB7RNB: /ipfs/QmYwgL3yVJvPCzxk4v2SKdeSCXofiQuSTxoRCmoxK3YewW
```
View the website at `http://gateway.ipfs.io/ipns/QmQnoFHgrF4iMQZqtNTKSeWuXBz9UtoGpsH5Xs4RvB7RNB`

You should change the *FILE_HASH* with your own hash generated in the above step!

## Great Resources
* [IPFS for websites](https://ipfs.io/docs/examples/example-viewer/example#../websites/README.md)
* [The definitive guide to publishing content on the decentralized web](https://medium.com/textileio/the-definitive-guide-to-publishing-content-on-ipfs-ipns-dfe751f1e8d0)
