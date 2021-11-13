## 需要安装的依赖 ##

1. 将 `dev-lang/yasm` 添加到 `~arm64` 目录中；
2. `emerge -av dev-lang/php dev-lang/go www-servers/apache dev-lang/yasm dev-libs/libaio app-arch/p7zip dev-util/cmake`
3. `./phoronix-test-suite interactive`
4. 选择压力测试，测试项目是1,3,11,31,47,64,101,121,147,196,294,337
5. 等待结果。