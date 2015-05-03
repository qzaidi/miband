# miband
miband data

# Extracting Data

Take a backup using adb, confirm backup on device after prompt

```
adb backup -f mi.ab -noapk -noshared com.xiaomi.hm.health
```

Skip the first 25 bytes
```
tail -c +25 mi.ab > mi.zlb 
cat mi.zlb | /usr/local/Cellar/openssl/1.0.1l/bin/openssl  zlib -d > mi.tar
```

