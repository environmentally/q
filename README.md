# Punchy's Alt Control — Deobfuscated

[Original repository](https://github.com/Nuclearpotato69/Punchy-Alt-Control/tree/main)

This repository contains a deobfuscated version of Punchy's Alt Control, modified so I can add back **3D rendering on an alt**.

## Features

- Deobfuscated source code for easier modification.
- Configurable main account and alt accounts.
- FPS limit setting.
- Optional notification suppression, including side notifications and the Alt Control overlay text.
- Anti-tamper bypass configuration.

## Configuration

Edit the settings in the script before running it:

```lua
getgenv().Settings = {
    prefix = "/";
    mainAccount = "mainaccount";
    altAccounts = {
        ["altaccount"] = true,
        ["altaccount2"] = true,
    };
    fpslimit = 30;
};

-- Set to true to silence side notifications and Alt Control overlay text.
local SILENCE_NOTIFICATIONS = true

-- Bypass anti-tamper
getgenv()._ufLpQBksSMvM = 'Script made by Punchy39 (punchingfella on Discord .gg/j4PgkQ72wp)';
getgenv().AltControlLoaded = false;

loadstring(game:HttpGet("https://raw.githubusercontent.com/environmentally/q/refs/heads/main/ctrl", true))()
```

### Settings

| Setting | Description |
|---|---|
| `prefix` | Prefix used for commands. |
| `mainAccount` | Username of the main account. |
| `altAccounts` | Table of authorized alt account usernames. |
| `fpslimit` | FPS limit setting. |
| `SILENCE_NOTIFICATIONS` | `true` suppresses side notifications and the Alt Control overlay text; `false` allows them to appear. |

**Note:** `SILENCE_NOTIFICATIONS` must be set inside the script itself, not just in the `Settings` table.

## Anti-tamper bypass

The configuration above includes the environment values used by this version's anti-tamper bypass.

## Purpose

This repository was made so I can modify Punchy's Alt Control and add back 3D rendering on an alt.
