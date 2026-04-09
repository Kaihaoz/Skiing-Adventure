# Project: Skiing Adventure - An HCI Interaction Prototype
# 项目名称：滑雪冒险 - 人机交互原型实验

## 🟢 Project Overview / 项目概述
This project is an immersive skiing simulation prototype built with Unity and Arduino. By replacing traditional keyboard inputs with a physical potentiometer, we explored the "Game Feel" of linear resistance in sports simulations. The project also integrates AIGC (Tripo AI) to streamline the 3D asset production pipeline.

本项目是一个基于 Unity 和 Arduino 开发的沉浸式滑雪模拟原型。通过利用物理电位计替代传统的键盘输入，我们探索了运动模拟中“线性阻尼感”对游戏手感的影响。同时，项目引入了 AIGC (Tripo AI) 技术，极大地优化了 3D 环境资产的生产流程。

## 🟡 Key Technical Features / 核心技术亮点

**1. Hardware-Software Integration (HCI) / 软硬结合交互**
Hardware: Arduino Uno + B100k Potentiometer.

Logic: Captured analog signals (0-1023) and mapped them to the character's horizontal movement in Unity via Serial Communication (C#).

Goal: Achieved a smooth, intuitive steering experience that mimics real skiing turns.

硬件方案： Arduino Uno + B100k 电位计。

实现逻辑： 捕获模拟信号并通过 C# 串口通信 将其映射为 Unity 角色的水平位移。

目标： 实现了模拟真实滑雪转弯的平滑、直观操控感。

**2. AI-Driven 3D Workflow / AI 驱动的 3D 工作流**
Tool: Tripo AI (Text-to-3D).

Efficiency: Generated complex environment assets (e.g., icy ruins, obstacles) within minutes. This reduced the asset production cycle by approximately 60%, allowing the team to focus on interaction logic and gameplay balance.

工具： Tripo AI (Text-to-3D)。

效率提升： 在数分钟内生成复杂的环境资产（如冰原遗迹、障碍物）。将资产生产周期缩短了约 60%，使团队能够集中精力于交互逻辑和游戏平衡性。

## 🔵 Logical Breakdown / 核心逻辑拆解
Arduino Logic (Snippet)

```
// Mapping potentiometer value to serial output
void loop() {
  int sensorValue = analogRead(A1); // Read rotation
  Serial.println(sensorValue);      // Send to Unity
  delay(10);                        // High-frequency sampling for smooth movement
}
```

Unity Integration
Data Processing: Implemented a buffer to handle serial data jitter, ensuring the character doesn't "stutter" during high-speed turns.

Collision System: Optimized Mesh Colliders for AI-generated assets to ensure precise interaction between the skier and the environment.

数据处理： 实现了数据缓冲区以处理串口信号抖动，确保角色在高速转弯时不会出现“跳帧”。

碰撞系统： 针对 AI 生成的模型优化了 Mesh Collider（网格碰撞体），确保滑雪者与环境交互的精确性。

## 🔴 Reflection & Iteration / 项目复盘与迭代

User Feedback: Testing revealed that while the potentiometer increased immersion, the collision sensitivity needed calibration for high-speed segments.


用户反馈： 测试显示，虽然电位计增加了沉浸感，但在高速阶段的碰撞灵敏度仍需微调。

## 🛠 Tools Used / 开发工具
Engine: Unity 2022.3 LTS

Hardware: Arduino IDE, Potentiometer, Breadboard

AI Tool: Tripo AI (Text-to-3D)

Language: C#, C++


