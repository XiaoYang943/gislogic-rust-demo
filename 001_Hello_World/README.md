## main函数
- main函数是每个Rust可执行程序最先运行的代码
## 编译和运行
- 运行Rust程序之前必须先编译`rustc main.rs`
  - 编译结果
    - 生成一个二进制文件`main.exe`
    - 在windows上还会生成一个包含调试信息的文件`main.pdb`
  - 运行：`main.exe`
- Rust是预编译语言
  - 先编译，在没有安装Rust的环境中也可以执行编译后的可执行文件
- `rustc`只适合简单的Rust程序，复杂的程序用`Cargo`
## Cargo
- Cargo是Rust的构建系统和包管理工具
  - `cargo --version`
### 创建项目
- `cargo new projectName`
  - Cargo.toml是项目的配置文件
  - 第三方库叫crate
### 构建项目
- `cargo build` 编译代码，用于开发环境
  - 第一次运行会在顶层目录生成cargo.lock文件
    - 追踪项目依赖的精确版本
    - 不需要手动修改该文件
- `cargo build --release` 编译代码，用于生产环境
  - 编译时会进行优化，代码运行更快，编译时间更长
  - 在target/release下生成可执行文件
- `cargo run` 编译代码并执行
- `cargo check` 检查代码，确保能通过编译，但是不产生可执行文件
  - 比`cargo build`快，用于检查代码
