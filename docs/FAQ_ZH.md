# 常见问题

## 命令行

赋予可执行权限

```bash
chmod +x ./h-ui
```

- 查看系统版本

  ```bash
  ./h-ui -v
  ```

- 自定义 Web 端口启动

  ```bash
  ./h-ui -p [端口]
  ```


- 重设系统管理员用户名和密码

  ```bash
  ./h-ui reset
  ```

## 项目工程中文件夹的含义

- bin: Hysteria2 的可执行文件和配置文件
- data: 数据库文件
- export: 所有导出的文件
- logs: 系统日志和 Hysteria2 运行日志

# 部署问题

## 无法访问面板

- 检查 h-ui 运行是否正常
- 检查防火墙是否放行端口
- 检查协议是否正确，http:// 或者 https://

## h-ui 启动失败

通过日志菜单查看 h-ui 日志排除错误原因

## Hysteria2 启动失败

- Hysteria2 配置错误，通过日志菜单查看 Hysteria2 日志排除错误原因
- 第一次使用 ACME 申请证书需要一段时间，请耐心等待 Hysteria2 启动并刷新页面

# 使用问题

## 证书如何管理？

ACME 方式（推荐）系统自动管理。自有证书方式要自己手动维护，到期之后手动替换

## 自有证书，如何设置 Hysteria2 证书路径？

将证书文件上传至服务器，在配置 Hysteria2 时，填入证书的绝对路径，通过 Docker 部署，需要将证书文件上传卷映射文件夹，推荐：/h-ui/bin

## 为什么只支持 Hysteria2 版本 >= v2.4.4？

低版本 Hysteria2 不支持最新 API

## 日志导出失败

没有日志文件