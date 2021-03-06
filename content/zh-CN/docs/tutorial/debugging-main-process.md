# 调试主进程

The DevTools in an Electron browser window can only debug JavaScript that's executed in that window (i.e. the web pages). To debug JavaScript that's executed in the main process you will need to use an external debugger and launch Electron with the `--debug` or `--debug-brk` switch.

## 命令行开关

Use one of the following command line switches to enable debugging of the main process:

### `--debug=[port]`

Electron will listen for V8 debugger protocol messages on the specified `port`, an external debugger will need to connect on this port. The default `port` is `5858`.

```shell
electron --debug=5858 your/app
```

### `--debug-brk=[port]`

Like `--debug` but pauses execution on the first line of JavaScript.

## 外部调试器

You will need to use a debugger that supports the V8 debugger protocol, the following guides should help you to get started:

- [在 VSCode 中调试主进程](debugging-main-process-vscode.md)
- [Debugging the Main Process in node-inspector](debugging-main-process-node-inspector.md)