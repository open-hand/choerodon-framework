## Introduction

平台父项目，管理平台各服务和组件版本

## Dependencies

* [hzero-parent](https://github.com/open-hand/hzero-parent.git)
* [choerodon-starter-parent](https://github.com/open-hand/choerodon-starters.git)

## Component relationship list
```
└─ choerodon-parent                                CHOERODON父依赖
    ├─ hzero-parent                                HZERO父依赖
    └─ choerodon-starter-parent                    通用开发父组件
        ├─ choerodon-gitlab4j-api                  gitlab api组件
        ├─ choerodon-tool-liquibase                liquibase初始化组件 
        │  └─ hzero-installer                      hzero初始化工具 
        ├─ choerodon-starter-core                  辅助核心开发组件 
        └─ choerodon-starter-asgard                asgard分布式事务组件
```

## Links

* [Change Log](./CHANGELOG.zh-CN.md)

## Contributing

欢迎参与项目贡献！比如提交PR修复一个bug，或者新建Issue讨论新特性或者变更。

Copyright (c) 2020-present, CHOERODON