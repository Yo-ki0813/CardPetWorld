# 🎴 CardPetWorld

> Scan cards. Summon pets. Begin your adventure.

CardPetWorld is a modular Python-based game prototype that allows players to scan real or digital cards using a camera and YOLO object detection to generate virtual pets. These pets can exist as interactive desktop companions, appear in a pixel-style adventure world, collect items, battle enemies, and export collected objects as **3D-printable models**.

---

## ✨ Features

- 📷 **Card Scanning** — Identify cards using a webcam + YOLO detection  
- 🖥️ **Desktop Pet Mode** — Pets roam freely on the desktop  
- 🎮 **Adventure World** — Pixel-style exploration with movement and interaction  
- 🎒 **Inventory System** — Collect, store, and manage items and pets  
- 🏭 **3D Export** — Export objects as `.OBJ` or `.STL` for 3D printing or AR viewing  

---

## 🚀 Quick Start

### 1️⃣ Install Dependencies

```bash
cd CardPetWorld
pip install -r requirements.txt

### 2. Launch the Game

```bash
python main.py
```
### 3. Controls

- **↑↓** - Menu navigation
- **Enter/Space** - Select / Confirm
- **ESC** - Back / Exit
- **Mouse click** - UI interaction
---

### 🎮 Core Player Loop
Scan → Unlock → Collect → Craft → View in 3D → Explore → Repeat
Players continuously repeat this loop to expand their collection and progress through the game.

---

### 🔍 1) Card Scanning System

- Uses the camera and YOLO detection to identify cards  
- Supports both printed and digital images  
- Unlocks and saves the detected object to the player’s inventory  
- Planned feature: reward animation for first-time detections

**Purpose:** Turn real-world card interaction into game progression.

---

### 📦 2) Inventory System

- Stores all scanned pets, resources, and items  
- Each entry includes metadata such as rarity, category, and placeholder stats  
- UI designed to support future sorting and filtering

**Purpose:** Provide long-term ownership and record player progression.

---

### 🔧 3) Crafting System (Prototype)

- Players can combine multiple collected materials to create new items or pets  
- Current logic uses placeholder rules  
- Future direction: rule-based recipes or AI-generated crafting outputs

**Purpose:** Encourage experimentation and provide progression mechanics.

---

### 🌍 4) Adventure Mode (Exploration Concept)

- Simple movement controls within a placeholder 2D world  
- Intended future features: NPCs, battles, resource gathering, environments

**Purpose:** Expand gameplay beyond scanning and collecting.

---

### 🧊 5) 3D Viewer + Export

- Collected or crafted assets can be exported as `.OBJ` or `.STL`  
- Includes a browser-based **Three.js 3D viewer** for rotation and zoom  
- Future goal: integrate AR preview mode for mobile devices

**Purpose:** Bridge in-game assets with real-world fabrication (e.g., 3D printing or AR display).

---

### 👤 Target User Experience

| Player Motivation | Prototype Support |
|------------------|------------------|
| Collection | Scan-to-unlock system |
| Progression | Inventory + crafting |
| Ownership | Exportable 3D models |
| Exploration | Early adventure mode |
| Personalization | Planned AI-generated assets |

---
```
📁 Project Structure
CardPetWorld/
├── main.py                # Application entry
├── requirements.txt       # Dependency list
├── config.yaml            # Global configuration
├── README.md              # Documentation
│
├── core/                  # Core engine systems
│   ├── event_bus.py
│   ├── state_manager.py
│   ├── resource_loader.py
│   └── game_engine.py
│
├── detection/             # YOLO card scanning pipeline
│   ├── camera.py
│   ├── detector.py
│   └── card_mapper.py
│
├── pet/                   # Virtual pet logic
│   ├── character.py
│   ├── stats.py
│   ├── animation.py
│   ├── behavior.py
│   └── pet_factory.py
│
├── desktop/               # Desktop pet interaction
│   ├── transparent_window.py
│   ├── desktop_pet.py
│   └── tray_menu.py
│
├── game_world/            # Adventure gameplay
│   ├── world.py
│   ├── tilemap.py
│   ├── player_controller.py
│   ├── enemy.py
│   ├── combat.py
│   └── collectible.py
│
├── inventory/             # Item storage and crafting
│   ├── item.py
│   ├── inventory.py
│   ├── crafting.py
│   └── item_database.py
│
├── export_3d/             # 3D model utilities
│   ├── mesh_generator.py
│   ├── voxelizer.py
│   ├── obj_exporter.py
│   └── stl_exporter.py
│
├── ui/                    # User interface
│   ├── menu.py
│   ├── hud.py
│   └── inventory_ui.py
│
├── data/                  # JSON datasets
│   ├── pets.json
│   ├── items.json
│   ├── recipes.json
│   ├── enemies.json
│   └── maps/
│
├── assets/                # Game assets
│   ├── sprites/
│   ├── sounds/
│   └── fonts/
│
└── tests/                 # Unit tests

## 🛠️ Dependencies

### Required
- **pygame** >= 2.5.0 - UI and game engine

### Optional (Enhances Features)
- **opencv-python** >= 4.8.0 - Camera + image processing
- **ultralytics** >= 8.0.0 - YOLO detection
- **PyQt6** >= 6.5.0 - Desktop pet transparent window
- **numpy** >= 1.24.0 - Computation
```

## 📋 Development Progress

- [x] Phase 1: Project scaffolding
- [x] Phase 2: Menu + runnable app
- [ ] Phase 3: Card scanning system
- [ ] Phase 4: Desktop pet behavior
- [ ] Phase 5: Adventure world
- [ ] Phase 6: Crafting & inventory
- [ ] Phase 7: 3D export pipeline

## 🎮 Current Prototype Status

**The project is currently in Phase 2 — the application runs and includes:

- ✅ Functional Pygame menu
- ✅ Keyboard and mouse navigation
- ✅ Modular structure prepared for expansion
- ✅ Clear scripted screens
- ✅ Placeholder gameplay systems

## 📝 License

MIT License

### ⭐ Summary

This prototype validates the feasibility of a hybrid **physical-to-digital pet ecosystem** using:

- Computer vision (YOLO)
- Modular game states
- Inventory and crafting mechanics
- 3D export and visualization technology

While not a finalized game, it successfully demonstrates the **core mechanics**, technical stack, and potential player experience of CardPetWorld.

---

# 🎴 CardPetWorld - 卡片宠物世界

> 扫描卡片，召唤宠物，开启冒险！

CardPetWorld 是一个模块化的 Python 游戏系统，支持通过摄像头扫描卡片/物体来创建虚拟宠物角色。这些宠物可以作为桌面伴侣、进入像素冒险世界、收集物品、战斗敌人，并将收集的物品导出为 3D 可打印文件。

## ✨ 功能特性

- 📷 **卡片扫描** - 使用摄像头和 YOLO 检测识别卡片
- 🖥️ **桌面宠物** - 宠物在桌面上自由活动
- 🎮 **游戏世界** - 像素风格的冒险游戏
- 🎒 **库存系统** - 收集和管理物品
- 🏭 **3D 导出** - 将物品导出为 OBJ/STL 格式

## 🚀 快速开始

### 1. 安装依赖

```bash
# 进入项目目录
cd CardPetWorld

# 安装依赖
pip install -r requirements.txt
```

### 2. 运行游戏

```bash
python main.py
```

### 3. 操作说明

- **↑↓** - 选择菜单项
- **Enter/空格** - 确认选择
- **ESC** - 返回/退出
- **鼠标** - 点击选择

## 📁 项目结构

```
CardPetWorld/
├── main.py              # 主入口文件
├── requirements.txt     # 依赖列表
├── config.yaml          # 全局配置
├── README.md            # 说明文档
│
├── core/                # 核心模块
│   ├── event_bus.py     # 事件总线
│   ├── state_manager.py # 状态管理
│   ├── resource_loader.py # 资源加载
│   └── game_engine.py   # 游戏引擎
│
├── detection/           # 物体检测模块
│   ├── camera.py        # 摄像头管理
│   ├── detector.py      # YOLO 检测器
│   └── card_mapper.py   # 卡片映射
│
├── pet/                 # 宠物模块
│   ├── character.py     # 角色基类
│   ├── stats.py         # 属性系统
│   ├── animation.py     # 动画系统
│   ├── behavior.py      # 行为系统
│   └── pet_factory.py   # 宠物工厂
│
├── desktop/             # 桌面宠物模块
│   ├── transparent_window.py # 透明窗口
│   ├── desktop_pet.py   # 桌面宠物
│   └── tray_menu.py     # 系统托盘
│
├── game_world/          # 游戏世界模块
│   ├── world.py         # 世界管理
│   ├── tilemap.py       # 地图系统
│   ├── player_controller.py # 玩家控制
│   ├── enemy.py         # 敌人系统
│   ├── combat.py        # 战斗系统
│   └── collectible.py   # 收集品
│
├── inventory/           # 库存模块
│   ├── item.py          # 物品定义
│   ├── inventory.py     # 库存管理
│   ├── crafting.py      # 合成系统
│   └── item_database.py # 物品数据库
│
├── export_3d/           # 3D 导出模块
│   ├── mesh_generator.py # 网格生成
│   ├── voxelizer.py     # 体素化
│   ├── obj_exporter.py  # OBJ 导出
│   └── stl_exporter.py  # STL 导出
│
├── ui/                  # 用户界面模块
│   ├── menu.py          # 菜单系统
│   ├── hud.py           # 游戏内显示
│   └── inventory_ui.py  # 库存界面
│
├── data/                # 数据文件
│   ├── pets.json        # 宠物定义
│   ├── items.json       # 物品定义
│   ├── recipes.json     # 配方定义
│   ├── enemies.json     # 敌人定义
│   └── maps/            # 地图文件
│
├── assets/              # 资源文件
│   ├── sprites/         # 精灵图
│   ├── sounds/          # 音效
│   └── fonts/           # 字体
│
└── tests/               # 测试文件
```

## 🛠️ 依赖说明

### 必需依赖
- **pygame** >= 2.5.0 - 游戏引擎

### 可选依赖
- **opencv-python** >= 4.8.0 - 摄像头和图像处理
- **ultralytics** >= 8.0.0 - YOLO 物体检测
- **PyQt6** >= 6.5.0 - 桌面宠物透明窗口
- **numpy** >= 1.24.0 - 数值计算

## 📋 开发进度

- [x] Phase 1: 项目结构创建
- [x] Phase 2: 基础菜单系统和项目可运行
- [ ] Phase 3: 卡片扫描功能
- [ ] Phase 4: 桌面宠物功能
- [ ] Phase 5: 游戏世界功能
- [ ] Phase 6: 库存和合成系统
- [ ] Phase 7: 3D 导出功能

## 🎮 当前状态

**Phase 2 已完成** - 项目现在可以运行！

- ✅ Pygame 菜单系统
- ✅ 键盘和鼠标导航
- ✅ 占位符屏幕
- ✅ 模块化架构
- ✅ 详细的代码注释

## 📝 许可证

MIT License

### ⭐ Summary

This prototype validates the feasibility of a hybrid **physical-to-digital pet ecosystem** using:

- Computer vision (YOLO)
- Modular game states
- Inventory and crafting mechanics
- 3D export and visualization technology

While not a finalized game, it successfully demonstrates the **core mechanics**, technical stack, and potential player experience of CardPetWorld.

---

**CardPetWorld** - 让卡片活起来！ 🎴✨
# CardPetWorld
