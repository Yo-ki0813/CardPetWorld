# CardPetWorld 🃏🐾 — AI-Generated Virtual Pet Crafting Game

CardPetWorld is a modular Python-based prototype game system that allows players to scan real trading cards or objects using YOLO-based object detection. The scanned item is converted into a virtual pet, which can then explore, battle, and evolve inside the game world. The collected items and pets can be exported as 3D printable models (OBJ/STL).

---

### ✨ Key Features

- 📷 **Card Scanning**
  Detect physical trading cards using the camera and YOLO to generate in-game pets.

- 🐾 **Virtual Pets**
  Each scanned card becomes a unique pet with rarity, skills, and attributes.

- 🎮 **Adventure Mode**
  Explore a pixel-style world, battle enemies, gain resources, and unlock upgrades.

- 📦 **Inventory System**
  Store scanned pets and scored items and manage crafting materials.

- 🛠 **Crafting & Fusion**
  Combine resources or pet fragments to create new pets or rare items.

- 🧱 **3D Export**
  Export collected items and pets as OBJ/STL files for 3D printing or AR viewing.

---

### 🧪 Technology Stack

| Component | Technology |
|----------|------------|
| Game engine | Python + Pygame |
| AI recognition | YOLO object detection |
| UI & state design | Modular game states with screen manager |
| 3D model handling | OBJ/STL export + external viewer |
| AR / Web demo | HTML + Three.js viewer |

---

### 📁 Project Structure
CardPetWorld/
│
├─ core/              # Core game logic
├─ detection/         # YOLO object detection
├─ game_world/        # Adventure gameplay
├─ inventory/         # Item & pet storage system
├─ screens/           # UI screens & state transitions
├─ web_ar/            # Web 3D viewer (Three.js demo)
├─ assets/            # Images, models, config files
├─ requirements.txt   # Dependencies
└─ main.py            # Entry point    
---

### 🚧 Current Status (Prototype)

✔ Working features:

- Card scanning prototype  
- Inventory system  
- Adventure movement  
- Basic 3D export and viewer  
- UI navigation and game state handling  

🚀 Next steps:

- Add animations & sound design  
- Improve AR integration  
- Polish gameplay, balance stats  

---

### 📜 License

This project is for academic and experimental use only.  
Commercial use requires permission.

---

### 👩‍💻 Author

> Qi Yang — Kwansei Gakuin University  
> Research Topic: *Game systems using AI recognition and mixed reality content generation.*
> 
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

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

---

**CardPetWorld** - 让卡片活起来！ 🎴✨
# CardPetWorld
