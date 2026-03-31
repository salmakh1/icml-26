# icml-26

## 📊 Experimental Results

### Mean Return on Foraging (8x8, 4p, 3f)

![Mean Return Curve](./Additional_experiment_on_LBF.png)


The figure above shows the training performance in terms of **mean episodic return** over time (timesteps) on the **Foraging-8x8-4p-3f-v3** environment from the **LBF (Level-Based Foraging)** benchmark.

We compare three methods:
- **LIMARL (red)** — *our proposed method*
- **MA2E (gray)** — a baseline multi-agent exploration method  
- **FT-QMIX (blue)** — a fine-tuned variant of QMIX  

---

## 🔍 Key Observations

- **Faster learning:** LIMARL achieves higher returns earlier in training.
- **Improved stability:** Smoother learning curve with fewer fluctuations.
- **Sample efficiency:** Reaches strong performance with fewer timesteps.
- **Comparable final performance:** All methods converge similarly, but LIMARL does so faster.

---

## 🧠 Environment Description

### LBF: Level-Based Foraging (Foraging-8x8-4p-3f-v3)

This experiment is conducted in the **LBF (Level-Based Foraging)** environment, a widely used **cooperative multi-agent reinforcement learning benchmark**.

#### 📐 Setup
- **Grid size:** 8 × 8  
- **Number of agents:** 4  
- **Number of food items:** 3  
- **Environment type:** Cooperative, partially observable  

#### ⚙️ Dynamics
- Each agent is assigned a **level**.
- Food items also have **levels**.
- Agents can move in four directions or stay in place.
- To collect food:
  - The **sum of agent levels** must meet or exceed the food level.
  - This enforces **coordination between agents**.
- Rewards are:
  - **Shared among all agents**
  - Proportional to successful food collection
- Each agent has **limited local observations**, making coordination non-trivial.

---

## 🚀 LIMARL (Our Method)

**LIMARL** is our proposed multi-agent reinforcement learning method designed to improve:

- **Coordination efficiency** in cooperative environments  
- **Learning speed** under sparse and delayed rewards  
- **Training stability**

### Key Ideas
- Better **representation learning** across agents  
- Improved **credit assignment**  
- More effective **interaction modeling** between agents  

---

## 📌 Summary

LIMARL consistently outperforms baseline methods in early and mid training stages, demonstrating superior **sample efficiency** and **stability**, while achieving competitive final performance.

