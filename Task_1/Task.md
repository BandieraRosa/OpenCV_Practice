本次作业使用的图像可随意选择，所有图像均应保存在 `picture` 下。图像命名应当标明内容，如原图命名：original_image.png，则对应灰度图像的命名：gray_image.png。每一个子题目对应一个源文件与可执行文件。

## 一、图像BGR通道操作
任选一张图像，分离其 B、G、R 三个通道，并分别保存到 `picture/` 目录下。然后，将 G 通道赋值为 0，再合并三个通道，并将合并结果保存到 `picture/` 目录下。

## 二、图像逻辑运算
任选两张图像，分别进行按位与、按位或、按位异或运算，并对其中一张图像进行按位非运算。将结果分别保存到 `picture/` 目录下。

## 三、图像整体操作
任选一张图像：

1. 将其缩小后再放大，插值方法任选，结果保存到 `picture/` 目录下。
2. 在原图上画一条红色副对角线，并在图像中心画一个绿色实心圆，结果保存到 `picture/` 目录下。
3. 将上述两张结果图像左右拼接，结果保存到 `picture/` 目录下。

## 四、滑动条改变图像二值化阈值
对以灰度格式保存的图像使用 `adaptiveThreshold()` 进行自适应阈值二值化，并将结果保存到 `picture/` 目录下。

要求：

- 创建滑动条调节 `maxValue`。
- 自适应阈值采用高斯法。
- 二值化方法使用 `THRESH_BINARY`。
- 按 `q` 键退出程序。



## 建议目录结构

```bash
./
├── CMakeLists.txt
├── README.md
├── picture/                        # 所有输入、输出图像
│   ├── original_image.png          # 任选原图
│   ├── gray_image.png              # 灰度图，Part 4 输入
│   ├── image1.png                  # Part 2 输入图 1
│   ├── image2.png                  # Part 2 输入图 2
│   ├── part1_channel_b.png         # Part 1：B 通道
│   ├── part1_channel_g.png         # Part 1：G 通道
│   ├── part1_channel_r.png         # Part 1：R 通道
│   ├── part1_g0_merged.png         # Part 1：G 通道置 0 后合并
│   ├── part2_and.png               # Part 2：与
│   ├── part2_or.png                # Part 2：或
│   ├── part2_xor.png               # Part 2：异或
│   ├── part2_not.png               # Part 2：非
│   ├── part3_resize.png            # Part 3：缩小后放大
│   ├── part3_draw.png              # Part 3：画红色副对角线、绿色实心圆
│   ├── part3_concat.png            # Part 3：左右拼接
│   └── part4_adaptive_threshold.png# Part 4：自适应阈值结果
├── include/
├── src/
│   ├── part1_bgr_channels.cpp
│   ├── part2_logic_ops.cpp
│   ├── part3_image_ops.cpp
│   └── part4_adaptive_threshold.cpp
└── build/
    ├── part1_bgr_channels
    ├── part2_logic_ops
    ├── part3_image_ops
    └── part4_adaptive_threshold
```
