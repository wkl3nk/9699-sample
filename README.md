# 9699-sample
Sample project to reproduce [ORT#9699](https://github.com/oss-review-toolkit/ort/issues/9699).

The root folder contains Angular CLI release 16.

In the `package-lock.json` in this folder, lines with `resolved` or `integrity`
have been removed intentionally.

To reproduce the issue, use `allowDynamicVersions": false` and enable Package Manager `Npm`.

With ORT Server, you would have the following section in the configuration for
the Analyer:

```yaml
"analyzer": {
   "enabledPackageManagers" : [
      "Npm"
   ],
   "allowDynamicVersions": false,
   "packageCurationProviders": []
},
```



