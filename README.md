# 3D_rebuild_model
## Day1 3D重建算法（缺少同一时刻图像的条件下)
程序与算法设计部分：
1. 收集图像数据。首先需要采集拉伸实验前后采集的图像。确保获得足够的角度信息。拉伸前后图像尽可能多的不同角度。将这些图像转化为矩阵。将每个矩阵视为时间序列
2. 定义自变量和因变量。将每个时间序列的一部分用作自变量。另一部分用作因变量。拉伸实验采集前后的图像作为自变量。拉伸之后采集的图像作为因变量。这样我们可以使用自变量预测因变量中未来时间点的值。
3. 拟合多元线性回归模型。使用多元线性回归模型来你和自变量和因变量之间的关系。每个时间序列都是一个矩阵。此时对矩阵进行结构化。保证每个变量在相同的尺度上。
4. 验证模型：使用多元线性回归模型后，进行验证确保其准确性。使用交叉验证等技术评估模型性能（MSE）和决定系数（R²）
5. 预测未来值；使用拟合的模型来预测未来时间点。在拉伸实验期间。使用这个模型预测在无法拍摄到图像的角度。进而重建3D图像，以获得完整的TEM 3D重建


未来可以尝试循环神经网络或卷积更好的捕获时间序列数据中的动态变化
