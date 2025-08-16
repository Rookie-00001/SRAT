# SRAT
Advanced Cerebrovascular Disease Risk Prediction System Based on Machine Learning Models

# Stroke Risk Assessment Tool (SRAT) — Parameter Scoring + Machine-Learning Inference

A **browser-based** clinical reference tool that provides **predicted stroke probability** using **parameter scoring** and **pre-built ML inference**.
**No model retraining, no server dependency** — all computation runs locally in the browser, with an optional **AI analysis** highlight.

<img width="2758" height="1440" alt="image" src="https://github.com/user-attachments/assets/14017f9a-2240-4d5e-992a-81aabaa582c4" />


## Key Notes

* **Scoring rules on the homepage**: vessel-specific stenosis → points, X\_score, Framingham, etc. are **implemented and displayed on the `homepage`**, so users can see how each input contributes.
* **Prediction only**: probabilities are computed in the browser using preloaded data and statistics.
* **Purpose of `models/`**: stores **calibrated training datasets for inference** only.
* **Evaluation & calibration**: AUC/ROC, Brier score, Hosmer–Lemeshow (H–L), etc. (if enabled).
* **AI (optional)**: Markdown-formatted health recommendations.

## Quick Start

### Online

Visit: **[https://rookie-00001.github.io/SRAT](https://rookie-00001.github.io/SRAT)**

### Local Deployment

```bash
# Clone the repo
git clone https://github.com/Rookie-00001/SRAT.git
cd SRAT

# Serve with any HTTP server
python -m http.server 8000
# or
npx serve .

# Open in the browser
# Windows
start http://localhost:8000
# macOS
open http://localhost:8000
```
<img width="2758" height="1440" alt="image" src="https://github.com/user-attachments/assets/ec461ab8-f46d-4016-bc64-0908011bb110" />

## Workflow Overview

1. **Choose a model**: open the homepage, click “Start Evaluation,” and select a model.
2. **Enter examination indicators**: input the patient’s data.
3. **Click Evaluate**: after entering indicators, click the evaluate button to obtain the result.
4. **AI Analysis**: after getting the predicted probability, optionally use AI analysis for recommendations.
5. **Patient history analysis**: save historical data to view risk trends and AI suggestions.

## Project Structure

```
.
├─ index.html          # Single-page app & scoring implementation (UI + logic)
├─ data/               # Data
├─ models/             # Training datasets & stats for inference
└─ pictures/           # Images / icons
```

## Privacy

* All computation is performed in the browser. If AI is enabled, the API key is stored locally (localStorage) and can be cleared in settings.

## License (Recommended)

**MIT License**


---

# 卒中风险评估工具（Web）— 参数赋分 + 机器学习推断

用于**临床参考**的浏览器端工具：基于**参数赋分**与**预置的机器学习推断**给出预测卒中概率。  
**不重新训练模型、不依赖服务器**，所有计算在本地浏览器完成，以及还有**AI 分析**的亮点功能。

## 关键说明
- **赋分规则在首页**：如分血管狭窄→积分、X_score、Framingham 等，均**在 `首页` 中实现并在页面展示**，便于查看每项输入如何贡献。  
- **仅做预测**：预测基于预置的数据与统计量在浏览器中完成。  
- **`models/` 目录的作用**：仅存放**用于推断的校准化后的训练集数据**。  
- **评估与校准**：可显示 AUC/ROC、Brier、H–L 等指标（若启用）。  
- **AI（可选）**： Markdown 格式的健康分析建议。

## 快速开始
### 在线使用
直接访问：**https://rookie-00001.github.io/SRAT**

### 本地部署
```bash
# 克隆项目
git clone https://github.com/Rookie-00001/SRAT.git
cd SRAT

# 使用任意 HTTP 服务器运行
python -m http.server 8000
# 或者
npx serve .

# 打开浏览器访问
# Windows
start http://localhost:8000
# macOS
open http://localhost:8000
```

## 概要流程
1. **选择模型**：进入首页，点击开始评估，选择模型。  
2. **录入检查指标**：录入患者各项指标。  
3. **点击评估**：录入患者对应指标后，点击评估按钮评估。  
4. **AI分析**：可在获得预测的卒中概率后使用AI分析给出建议。  
5. **患者历史数据分析**：可保存历史数据，查看卒中风险趋势以及AI分析建议。  

## 目录结构
```
.
├─ index.html          # 单页应用与赋分实现（UI + 逻辑）
├─ data/               # 数据
├─ models/             # 用于推断的训练集与统计
└─ pictures/           # 图片/图标
```

## 隐私
- 计算全部在浏览器内完成；若启用 AI，API Key 仅存于本地（localStorage），可在设置中清除。

## 许可证（建议）
**MIT License**
