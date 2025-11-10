# Spook 👻 中文版

一个功能强大的 Home Assistant 集成，提供 100+ 实用服务和自动配置检查功能。完整中文汉化版本。

## ✨ 核心功能

### 🔧 强大的服务扩展

- **区域管理** - 创建、删除、修改区域及其别名
- **楼层管理** - 管理楼层及区域分配
- **标签管理** - 为实体、设备、区域添加标签
- **实体操作** - 重命名、隐藏、启用/禁用实体
- **设备控制** - 启用/禁用设备和配置条目
- **蓝图管理** - 导入蓝图
- **统计导入** - 导入历史统计数据

### 👻 智能配置检查

自动检测配置问题：

- 🔍 未知实体引用
- 📍 未知区域引用
- 🏢 未知楼层引用
- 🏷️ 未知标签引用
- 🔌 未知设备引用
- 🎯 未知动作引用

所有问题显示在 **设置 → 系统 → 修复** 中。

### 📊 实用传感器

- 实体统计
- 集成统计
- 区域统计
- 设备统计
- 修复问题统计

### 🔘 便捷按钮

- 重新加载 Home Assistant
- 重启系统
- 批量忽略/恢复修复问题

## 📖 使用示例

### 创建区域

```yaml
service: spook.homeassistant_create_area
data:
  name: 书房
  icon: mdi:book-open-page-variant
  aliases:
    - 读书室
    - 办公室
```

### 为实体添加标签

```yaml
service: spook.homeassistant_add_label_to_entity
data:
  entity_id: light.living_room
  label_id: 客厅设备
```

### 导入蓝图

```yaml
service: spook.blueprint_import
data:
  url: https://github.com/xxx/blueprint.yaml
```

## 🌟 特色功能

### Inverse 反转助手

包含实用的子集成，可以反转实体的状态：
- 反转二元传感器（open ↔ close）
- 反转开关（on ↔ off）

## ⚠️ 注意事项

- 需要 Home Assistant 2024.6.0+
- 首次安装后需要重启
- 部分服务可能会修改配置，请谨慎使用
- 建议使用前备份配置

---

**原版仓库**: [frenck/spook](https://github.com/frenck/spook)
