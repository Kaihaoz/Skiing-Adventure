# Project: Skiing Adventure - An HCI Interaction Prototype
# 项目名称：滑雪冒险 - 人机交互原型实验

## 🟢 Project Overview / 项目概述

EnglishSkiing Adventure is an interactive skiing game controlled by a physical potentiometer. It combines Arduino hardware and Unity to create an immersive ski experience. 

中文Skiing Adventure 是一款通过物理电位器控制的交互式滑雪游戏，结合 Arduino 硬件 与 Unity 游戏引擎 实现沉浸式滑雪体验。





## 🟡 Visual Gallery / 视觉展示

### Final Scene Render / 最终场景渲染
The environment uses a Low-poly aesthetic with custom particle effects and ambient lighting.

场景采用低多边形美学，结合自定义粒子效果与环境光照。

---

![3](https://github.com/user-attachments/assets/c88283fa-3aad-4301-8170-c8b03a7eae10)
<img width="2061" height="576" alt="3" src="https://github.com/user-attachments/assets/3e73750d-be80-455c-8e64-d7b92984c346" />
![4](https://github.com/user-attachments/assets/52c3c257-0119-4488-aec5-2a39a5f24c6b)


---

## 🛠️ Hardware & Software / 硬件与软件

- Potentiometer (B100k)  电位器（B100k）
- Arduino board  Arduino 开发板
- Unity
- Arduino IDE
- TRIPO AI (3D asset generation)

## ✨ Core Features / 核心功能

- Potentiometer controls left/right movement  电位器控制角色左右移动
- Click to start the game; auto-skiing forward 点击开始游戏，角色自动向前滑行
- Press Space to trigger backflip animation 空格键触发后空翻动画
- Collision detection system 碰撞检测系统
- 3D scene, animation, lighting & particle effects 3D 场景、动画、灯光与粒子特效
- Background music & immersive experience 背景音乐与沉浸式体验
- Hardware-software interaction 软硬件联动交互

---
**Unity Collision System**
<img width="2048" height="1201" alt="unity collision system" src="https://github.com/user-attachments/assets/c4cd5386-ccbf-4a6b-ad7f-6ec40e65d8d6" />


**Game Interaction Design & File Packaging**
<img width="2048" height="1244" alt="Game interaction design" src="https://github.com/user-attachments/assets/e00b1d6a-3558-479c-8d1a-043bd648d2b6" />

---

## 🚀 Implementation Process / 实现流程

- Arduino + Unity CommunicationRead potentiometer value and send to Unity via serial port to control character movement.  Arduino + Unity 通信读取电位器数值，通过串口发送到 Unity，控制角色移动。
- Unity Collision SystemBuilt collision detection to support player-scene interaction.  Unity 碰撞系统搭建碰撞检测，实现玩家与场景的基础交互。
- Game Interaction & Visual DesignCharacter animation, motion binding, follow camera, particle effects, ambient lighting.  游戏交互与视觉设计角色动画、运动绑定、跟随相机、粒子特效、环境灯光。
- 3D Scene ConstructionGenerated 3D assets with TRIPO AI and built ski slope environment.  3D 场景搭建使用 TRIPO AI 生成 3D 资源，构建滑雪坡道场景。

<img width="1089" height="290" alt="4" src="https://github.com/user-attachments/assets/a70cf8de-4455-48ba-92e9-a2dfb24ef15a" />

---

### **Character Animation and Camera Binding**

- Click to start the animation and move the character  点击开始动画并移动角色
- Loop charactern skiing pose animation  循环播放滑雪角色的姿势动画
- Space to trigger a character backflip pose 空格键触发角色后空翻姿势
- Setting the character's initial state speed 设置角色初始状态的速度
- Add potentiometer and linked with Unity 添加电位器并与 Unity 连接
- Setting motion camera 设置运动摄像机
- Add background music 添加背景音乐

---

<img width="2276" height="1060" alt="1" src="https://github.com/user-attachments/assets/b2039a3d-b53e-4e70-b915-66d076b914ed" />

<img width="1108" height="268" alt="2" src="https://github.com/user-attachments/assets/2fadf113-7879-4050-b149-c120661f0bcc" />

![1](https://github.com/user-attachments/assets/e614888c-36db-41fa-983a-f8c1f05a8da4)

![2](https://github.com/user-attachments/assets/f64cf840-a19f-4c22-ba6f-f0150421b739)

---

## 💻 Arduino Code / Arduino 代码
```
#include <SoftwareSerial.h>

void setup() {
  Serial.begin(9600); 
}

void loop() {
  int potValue = analogRead(A1); 
  Serial.println(potValue);
  delay(100); 
}
```

## 📊 Feedback & Optimization / 反馈与优化

Peer Feedback

- Large, immersive scene with consistent visual style  场景宏大、视觉风格统一、沉浸感强
- Hardware interaction has strong expansion potential  硬件交互有很强扩展潜力
- Collision detection accuracy needs improvement  碰撞检测精度需要优化
