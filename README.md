# Ciel

パソコンの中で動いている Claude Code や Codex を、ブラウザの画面から使う道具です。

**2026年12月31日まで無料**で使えます。1月1日からは止まります（続けるときは製品版）。

## ダウンロード

[Releases](../../releases/latest) の「Assets」から、**自分のパソコンと Python の版に合うファイルを1つ**落としてください。

| パソコン | ファイル名の終わり |
|---|---|
| Mac（Apple のチップ） | `macosx_…_arm64.whl` |
| Windows 11 | `win_amd64.whl` |

ファイル名の `cp312` / `cp313` / `cp314` が Python の版（3.12 / 3.13 / 3.14）です。
版は、ターミナル（Windows は PowerShell）で `python3 --version`（Windows は `python --version`）と打つと分かります。

## 入れ方

Mac

    pipx install ~/Downloads/ciel-*.whl
    ciel setup
    ciel serve

Windows 11

    pipx install (Get-Item $HOME\Downloads\ciel-*.whl).FullName
    ciel setup
    ciel serve

## 問い合わせ

shopsupport0@gmail.com
