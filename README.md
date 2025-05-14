# 个性化营养助手 (Colab版)

本项目是一个基于Google Colab实现的个性化营养需求计算与食材推荐原型。用户输入身体数据和健康目标后，程序会计算每日所需的宏量营养素，并从预设的食物数据库中推荐一份食材搭配方案。

## 功能
- 根据用户输入（年龄、性别、身高、体重、活动水平、目标）计算BMR、TDEE。
- 基于目标调整每日热量，并推荐蛋白质、碳水化合物、脂肪的摄入量。
- 设有蛋白质摄入上限，避免因体重基数过大导致蛋白质推荐量过高。
- 从食物数据库中选择食材，尝试满足宏量营养素目标。
- 食材选择逻辑考虑了食物的单次最大推荐量和最小推荐量，并尝试平衡营养素。

## 如何运行
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jinv2/NutritionalAssistantColab/blob/main/NutritionalAssistant.ipynb)

1. 点击上面的 "Open In Colab" 徽章在Google Colab中打开本 Notebook。
2. （可选）如果使用了独立的 `food_database.csv`，请确保在Colab中能访问到它（例如从同一GitHub仓库加载，或上传到Colab环境）。当前Notebook可能内嵌了数据库或从固定路径加载。可以通过修改 Notebook 开头下载最新 CSV 的代码来确保使用 GitHub 上的最新数据。
3. 按顺序运行Notebook中的所有单元格。
4. 在“用户输入”单元格中按提示输入您的个人信息。
5. 查看输出的营养需求和推荐食材方案。

## 食物数据库
- 当前食物数据库（`food_database.csv` 或Notebook内嵌）包含有限的常见食物。
- 营养数据主要基于常见估算值。
- 欢迎通过Pull Request扩展食物数据库。

## 依赖
- pandas
- numpy
(Google Colab通常已预装这些库)

## 已知局限性与未来改进
- 食材选择算法为启发式，结果可能并非绝对最优。
- 食物数据库需要持续扩充。
- 未考虑微量营养素、三餐分配、具体烹饪方法。
- 未来可以考虑：更复杂的优化算法、用户偏好精细处理、移植到Web框架等。

## 许可证
本项目采用 [MIT许可证](LICENSE)。
