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

Returns a list of codesigning identities installed in the default keychain.  

Internally calls  

```
security find-identity -p codesigning -v
```

<img width="1013" alt="2019-03-08 1 52 30" src="https://user-images.githubusercontent.com/1725068/53974380-cc70bc80-4145-11e9-8282-fb5ea23dbd18.png">

```
status:=codesign (path;identity{;keys})

```


Parameter|Type|Description
------------|------------|----
path|TEXT|
identity|TEXT|
keys|OBJECT|addtional keys to add to ``Info.plist`` 

In ``keys`` you can specify ``CFBundleIdentifier`` to customise the bundle identifier. By default, it is set to ``4d.com.{appName}.app``

<img width="1013" alt="2019-03-08 1 40 28" src="https://user-images.githubusercontent.com/1725068/53974568-2ec9bd00-4146-11e9-984e-1c8d0adf86b9.png">


