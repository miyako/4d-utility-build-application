# 4d-utility-build-application
Tools to simplify BUILD APPLICATION

---

## Syntax

```
identity:=find_identity 
```


Parameter|Type|Description
------------|------------|----
identity|COLLECTION|

Returns a list of signing identities installed in the default keychain.  

Internally calls  

```
security find-identity -p codesigning -v
```

<img width="1013" alt="2019-03-08 1 52 30" src="https://user-images.githubusercontent.com/1725068/53974380-cc70bc80-4145-11e9-8282-fb5ea23dbd18.png">
