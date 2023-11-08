Reserve a UPI TechZone cluster with the following requirements:
```
OpenShift Version: 4.10 - 4.12
OCS/ODF Size: 2TiB
Worker Node Count: 5
Worker Node Flavor: 16 vCPU x 64 GB - 100 GB ephemeral storage
```

ENABLE_COLLECTION set to false outputs the following error:

```
"msg": "ParserError: while parsing a block mapping\n  in \"<unicode string>\", line 8, column 3:\n      customerName: \"SUJN\"\n      ^\nexpected <block end>, but found '<block mapping start>'\n  in \"<unicode string>\", line 11, column 5:\n        enableCollection: false\n        ^"
```

storage role outputs the following error in ansible-runner taskRun:
```
[0;31m    "msg": "Failed to patch object: b'{\"kind\":\"Status\",\"apiVersion\":\"v1\",\"metadata\":{},\"status\":\"Failure\",\"message\":\"storageclasses.storage.k8s.io \\\\\"openshift-storage.noobaa.io\\\\\" is forbidden: User \\\\\"system:serviceaccount:funstuff:ansible-deployer-account\\\\\" cannot patch resource \\\\\"storageclasses\\\\\" in API group \\\\\"storage.k8s.io\\\\\" at the cluster scope\",\"reason\":\"Forbidden\",\"details\":{\"name\":\"openshift-storage.noobaa.io\",\"group\":\"storage.k8s.io\",\"kind\":\"storageclasses\"},\"code\":403}\\n'",[0m
```