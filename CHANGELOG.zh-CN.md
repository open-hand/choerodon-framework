# Changelog

这个项目的所有显著变化都将被记录在这个文件中。

## [0.6.0] - 2018-06-04

### 移除

- 移除pom中source，javadoc，gpg的依赖，这些依赖会导致服务无法直接通过`mvn install`。