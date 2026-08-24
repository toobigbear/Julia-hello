# Hello-Project: Julia 学习工程

标准的 Julia 工程结构，包含学习示例和实战项目。

## 工程结构

```
hello-project/
├── Project.toml              # 工程配置文件（依赖、版本）
├── README.md                 # 本文件
├── src/                      # 源代码目录
│   └── HelloProject.jl       # 主模块文件
├── basics/                   # 基础语法（01-15）
│   ├── 01_hello_world.jl
│   ├── 02_variables.jl
│   ├── 03_operators.jl
│   ├── 04_strings.jl
│   ├── 05_arrays.jl
│   ├── 06_tuples.jl
│   ├── 07_dicts.jl
│   ├── 08_loops.jl
│   ├── 09_conditionals.jl
│   ├── 10_functions.jl
│   ├── 11_multiple_dispatch.jl
│   ├── 12_structs.jl
│   ├── 13_error_handling.jl
│   ├── 14_comprehensions.jl
│   └── 15_types.jl
├── advanced/                 # 高级主题（16-19）
│   ├── 16_modules.jl
│   ├── 17_file_io.jl
│   ├── 18_macros.jl
│   └── 19_performance.jl
└── projects/                 # 实战项目
    └── 20_practical_projects.jl
```

## 快速开始

### 1. 运行学习示例

```bash
# 进入工程目录
cd D:\OtherProject\JuliaProject\hello-project

# 运行基础语法示例
julia basics/01_hello_world.jl
julia basics/02_variables.jl

# 运行高级主题
julia advanced/16_modules.jl

# 运行实战项目
julia projects/20_practical_projects.jl
```

### 2. 使用工程模块

```julia
# 在 Julia REPL 中
julia> ]

(@v1.10) pkg> activate .  # 激活当前工程

(hello-project) pkg> instantiate  # 安装依赖

julia> using HelloProject

julia> greet("Alice")
Hello, Alice! 欢迎来到 Julia 世界！

julia> add(3, 5)
8
```

### 3. 在 VS Code 中使用

1. 打开 `hello-project` 文件夹
2. 按 `Ctrl+Shift+P` → `Julia: Activate This Environment`
3. 打开任意 `.jl` 文件
4. 按 `Ctrl+F5` 运行

## 学习路径

### 第一阶段：基础语法（1-2 周）
- **目标**：掌握 Julia 的基本语法
- **文件**：`basics/01` 到 `basics/09`
- **重点**：变量、数组、字典、循环、条件

### 第二阶段：进阶特性（2-3 周）
- **目标**：理解 Julia 的核心特性
- **文件**：`basics/10` 到 `basics/15`
- **重点**：函数、多重派发、结构体、类型系统
- **里程碑**：能写出自定义类型和函数

### 第三阶段：高级主题（2-3 周）
- **目标**：掌握 Julia 的高级功能
- **文件**：`advanced/16` 到 `advanced/19`
- **重点**：模块、文件 IO、宏、性能优化
- **里程碑**：能优化代码性能

### 第四阶段：实战项目（1-2 周）
- **目标**：综合应用所学知识
- **文件**：`projects/20_practical_projects.jl`
- **重点**：完成 10 个实战项目
- **里程碑**：能独立开发小型应用

## 工程配置

### 添加依赖包

```julia
# 在 Julia REPL 中
julia> ]

(hello-project) pkg> add DataFrames Plots CSV

# 会自动更新 Project.toml
```

### 常用第三方包推荐

```julia
# 数据分析
add DataFrames CSV Query

# 可视化
add Plots StatsPlots PlotlyJS

# 机器学习
add Flux MLJ Knet

# 优化
add JuMP Optim

# Web 开发
add HTTP Genie Oxygen

# 数据库
add SQLite MySQL PostgreSQL
```

## 开发建议

1. **先学习，后开发**：按顺序完成 `basics/` → `advanced/` → `projects/`
2. **动手实践**：每个文件都运行一遍，理解每一行代码
3. **做笔记**：在代码中添加自己的注释
4. **修改实验**：改变示例代码，观察结果变化
5. **提问交流**：遇到问题查文档或提问

## Julia 学习资源

- **官方文档**: https://docs.julialang.org/
- **Julia 中文社区**: https://cn.julialang.org/
- **包管理器**: https://juliahub.com/
- **论坛**: https://discourse.julialang.org/
- **知乎专栏**: 搜索 "Julia 编程"

## 常见问题

### Q: 为什么 Julia 从 1 开始索引？
A: Julia 设计目标是科学计算，数学公式通常从 1 开始（矩阵第一行第一列是 a₁₁）。

### Q: struct 和 mutable struct 的区别？
A: `struct` 不可变，性能更好；`mutable struct` 可以修改字段，但稍慢。优先使用 `struct`。

### Q: 如何提高 Julia 代码性能？
A: 查看 `advanced/19_performance.jl`，核心原则：
- 保持类型稳定
- 避免全局变量
- 预分配内存
- 使用内置函数

### Q: Julia 的多重派发是什么？
A: Julia 最核心的特性，查看 `basics/11_multiple_dispatch.jl`。

## 下一步

完成本工程的学习后，你可以：

1. **数据分析**: 学习 DataFrames.jl，处理真实数据
2. **机器学习**: 学习 Flux.jl，训练神经网络
3. **Web 开发**: 学习 Genie.jl，开发 Web 应用
4. **科学计算**: 学习 DifferentialEquations.jl，解微分方程
5. **并行计算**: 学习 Distributed.jl，编写并行程序

## 贡献

欢迎提交 issue 和 pull request！

## 许可证

MIT License

---

**Happy Coding with Julia! 🎉**
