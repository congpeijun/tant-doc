# 新增页面
目前创建一个页面需要执行三步，`创建页面` `配置路由` `后端创建菜单`。

## 创建页面

在 `src/views` 下新建页面的vue文件，如果相关页面有多个，可以新建一个文件夹来放置相关文件。

## 配置路由
配置路由后，可到后台创建菜单。 创建菜单时，选择对应的组件地址即可。
```bash
# src/config/componentConfigs.js

import { BasicLayout, UserLayout, RouteView, BlankLayout, PageView } from '@/layouts'

export const Components = {
  // 基础页面 layout 必须引入
  'Layout': {
    BasicLayout,
    UserLayout,
    RouteView,
    BlankLayout,
    PageView
  },
  // 普通页面
  'Page': {
    'Analysis': () => import('@/views/dashboard/Analysis'),

    // ... 在此位置添加你创建的页面文件
  }
}

```