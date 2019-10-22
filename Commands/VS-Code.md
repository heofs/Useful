# VS Code

## CMDER terminal on Windows
Add this to `settings.json`.

```
  "terminal.integrated.shell.windows": "cmd.exe",

  "terminal.integrated.env.windows": {
  "CMDER_ROOT": "C:\\yourlocation\\cmder"
  },
  "terminal.integrated.shellArgs.windows": [
    "/k C:\\yourlocation\\cmder\\vendor\\init.bat"
  ],
```
