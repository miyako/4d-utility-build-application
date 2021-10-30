# 4d-utility-build-application
Tools to simplify BUILD APPLICATION

**Note**: A [newer version for v19](https://github.com/miyako/4d-class-build-application) is available.

## Syntax

```
identity:=find_identity 
```

Parameter|Type|Description
------------|------------|----
identity|COLLECTION|list of codesigning identities installed in the default keychain

Internally calls  

```
security find-identity -p codesigning -v
```

<img width="1013" alt="2019-03-08 1 52 30" src="https://user-images.githubusercontent.com/1725068/53974380-cc70bc80-4145-11e9-8282-fb5ea23dbd18.png">

![preemption xx](https://user-images.githubusercontent.com/1725068/41327179-4e839948-6efd-11e8-982b-a670d511e04f.png)

```
status:=codesign (path;identity{;keys})
```

Parameter|Type|Description
------------|------------|----
path|TEXT|path to the app to codesign
identity|TEXT|codesign identity
keys|OBJECT|optional; keys to add to the app's ``Info.plist`` 

In ``keys`` you can specify ``CFBundleIdentifier`` to customise the bundle identifier. By default, it is set to ``4d.com.{appName}.app``

The following keys are automatically added

* ``NSRequiresAquaSystemAppearance``:``YES``    
* ``NSAppleEventsUsageDescription``:``""``      
* ``NSCalendarsUsageDescription``:``""``    
* ``NSContactsUsageDescription``:``""``    
* ``NSCameraUsageDescription``:``""``    
* ``NSMicrophoneUsageDescription``:``""``  

<img width="1013" alt="2019-03-08 1 40 28" src="https://user-images.githubusercontent.com/1725068/53974568-2ec9bd00-4146-11e9-984e-1c8d0adf86b9.png">

---

for more information about notarisation:

https://developer.apple.com/documentation/security/notarizing_macos_software_before_distribution/customizing_the_notarization_workflow?preferredLanguage=occ

