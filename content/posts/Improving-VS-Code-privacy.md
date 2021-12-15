+++
title = "VS Code privacy settings"
date = 2021-12-15
description = "How to easily improve your privacy on VS Code by modifying some settings"
tags = ["Privacy"]
categories = ["Guides","Posts"]
+++

{{< toc >}}

In contrast to some popular beliefs, it is possible to make VS Code a very private code editor without the need of using forks such as VSCodium.

## Deprecated settings

The settings `"telemetry.enableCrashReporter": false` and `"telemetry.enableTelemetry": false` are deprecated and useless.

## New telemetry settings

`"telemetry.telemetryLevel": "off"` will disable all telemetry and crash reporting.

## Settings you might want to check

These are not necessarily Telemetry but are worth including if you don't want any more external connections coming out of VS Code.

`"workbench.settings.enableNaturalLanguageSearch": false` will disable Natural Language Search, see this
[Github Discussion](https://github.com/Microsoft/vscode/issues/44294) and this
[VS Code blog](https://vscode.trafficmanager.net/blogs/2018/04/25/bing-settings-search) for more information.

If you have not disabled telemetry, `"workbench.enableExperiments": false` will disable experiments made by Microsoft, curiously according to this
[documentation](https://github.com/Microsoft/vscode-docs/blob/main/docs/supporting/faq.md): "Our experimentation framework calls out to a Microsoft-owned
service and is therefore disabled when telemetry is disabled.", yet it will still make some GET calls to `https://vscodeexperiments.azureedge.net`, however it's
worth nothing these calls have empty content.

## Wrapping it up

If you turn off all unnecessary telemetry and crash reporting, there will still be two connections that I consider harmless:
`https://update.code.visualstudio.com/` fetches updates and `https://marketplace.visualstudio.com/_apis/public/gallery/` which is related to extensions.

If you wonder how I tested this, I used [mitmproxy](https://mitmproxy.org/) and checked which connections where being made after I opened the editor.

Happy coding.
