# GitHub Actions 组件

![alt text](./asset/image.png)

## Workflows 工作流

工作流是一个可配置的自动化流程，它会运行一个或多个作业。

- 工作流定义在 `.github/workflow` 中，每个工作流可以执行一组不同的任务。
- 可以在一个工作流中引用一个工作流。

## Events 事件

事件是存储库中触发工作流运行的特定活动，例如，pull requet 的创建、issue 的打开等等。

## Jobs 作业

作业是在同一个运行器上执行的工作流的一组步骤。每一步可能是脚本的执行，或者其他运行操作。

## Action 行动

行动是程序，它从 Github 中拉去仓库并为环境的构建设置正确的工具链。

## Runners 运行器

运行器就是一个服务器，当工作流被触发时，它就会运行工作流。每个运行程序一次可以运行一个作业。

# 工作流程的 YAML 语法

## name

工作流的名称。

## run-name

从工作流生成的工作流运行的名称，可以包含表达式。

```yaml
run-name: Deploy to ${{ inputs.deploy_target }} by @${{ github.actor }}
```

## on

工作流的触发事件。

```yaml
on：[push, fork]
```

## env

配置环境变量。

```yaml
env:
  SERVER: production
```
