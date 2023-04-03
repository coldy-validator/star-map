# 🌌

repository of statically-linked chain binaries, tracking the [cosmos chain registry](https://github.com/cosmos/chain-registry), available at [autobuild.coldyvalidator.net](https://autobuild.coldyvalidator.net)

### apt repo

add repo gpg key and source list:
```
curl -sL https://github.com/coldy-validator/star-map/raw/%E2%9C%A8/release/repo.key |
  gpg --dearmor | tee /etc/apt/trusted.gpg.d/star-forge.gpg
echo "deb [arch=amd64 signed-by=/etc/apt/trusted.gpg.d/star-forge.gpg] https://deb.coldyvalidator.net stable main" |
  tee /etc/apt/sources.list.d/star-forge.list
apt update
```

install desired executables:
```
apt install osmosisd junod
```
suite | ledger | goleveldb | pebbledb | skip mev
 :--- | :---: | :---: | :---: | :---:
**stable** | ✅ | ✅ | ❌ | ❌
**mev** | ✅ | ✅ | ❌ | ✅
**experimental** | ❌ | ❌ | ✅ | ❌
**experimental_mev** | ❌ | ❌ | ✅ | ✅
