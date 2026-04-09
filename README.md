# Project: Skiing Adventure - An HCI Interaction Prototype
# 项目名称：滑雪冒险 - 人机交互原型实验

## 🟢 Project Overview / 项目概述
"Skiing Adventure" is an experimental interaction prototype built with **Unity** and **Arduino**. The project explores the potential of physical controllers in sports simulations, using a potentiometer to provide linear resistance for steering. The environment is a hybrid of manual scene construction and **AI-generated (Tripo AI)** assets.

本项目是一个基于 **Unity** 和 **Arduino** 开发的交互实验原型。项目探索了物理控制器在运动模拟中的潜力，利用电位计为转向提供线性阻尼感。游戏环境则结合了人工场景搭建与 **AI 生成 (Tripo AI)** 资产的混合。



## 🟡 Visual Gallery / 作品展示

The final environment features a cohesive low-poly aesthetic, complete with custom particle effects (snowfall) and ambient lighting to simulate a dynamic winter wilderness.
最终环境呈现了统一的低多边形（Low-poly）美学，并配有自定义粒子效果（降雪）和环境光照，以模拟动态的冬日荒野。


<img width="2061" height="576" alt="3" src="https://github.com/user-attachments/assets/6da27ca2-aca9-4a2d-a4e6-d9d406bb23fe" />


## 🟡 Key Technical Features / 核心技术亮点

**1. Hardware-Software Integration (HCI) / 软硬结合交互**
Hardware: Arduino Uno + B100k Potentiometer.

Logic: Captured analog signals (0-1023) and mapped them to the character's horizontal movement in Unity via Serial Communication (C#).

Goal: Achieved a smooth, intuitive steering experience that mimics real skiing turns.

硬件方案： Arduino Uno + B100k 电位计。

实现逻辑： 捕获模拟信号并通过 C# 串口通信 将其映射为 Unity 角色的水平位移。

目标： 实现了模拟真实滑雪转弯的平滑、直观操控感。

## 🟡 AI-Assisted Asset Production / AI 辅助资产生产

Rather than generating the entire scene, we utilized **Tripo AI** to transform images into specific 3D environmental elements. This "Hybrid Workflow" significantly accelerated the population of the game world.

本项目并非直接生成整个场景，而是利用 **Tripo AI** 将图像转化为特定的 3D 环境元素。这种“混合工作流”显著加速了游戏世界的填充。

*   **Technology:** Image-to-3D Generation.
*   **Case Study:** Generated complex **Dinosaur Bone** structures and snow-covered props from reference images.
*   **Efficiency:** Automated the modeling of organic and complex shapes, allowing the team to focus on scene composition and interaction design.
*   **技术应用：** Image-to-3D 生成技术。
*   **具体案例：** 基于参考图生成了复杂的**恐龙骨架**结构及雪地道具。
*   **效率价值：** 实现了有机且复杂形状的建模自动化，使团队能够集中精力于场景构图与交互设计。


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


