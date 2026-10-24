# Ciel

パソコンの中で動いている Claude Code や Codex を、ブラウザの画面から使う道具です。

**当面無料**で使えます。感想を聞かせてもらえたらうれしいです（shopsupport0@gmail.com）。

**1.5.0 から、アプリになりました。** 開くと Ciel 専用の窓で出ます（1.5.1 から・Chrome か Edge があるとき）。 落としてダブルクリックで入ります。Python や Homebrew は要りません。
新しい版が出ると、Ciel の画面に「新しい版」と出て、押すだけで更新できます（1.5.4 から。1.5.0〜1.5.3 を入れた方は、下の「1.5.0〜1.5.3 を入れた方へ」の手順で一度だけ入れ直してください）。

## 要るもの

- **Claude Code** か **Codex**（ChatGPT の）。入っていて、ログインできていること
  - Claude Code：https://code.claude.com/docs/en/setup
  - Codex：https://developers.openai.com/codex/cli
- **Mac**：Apple のチップ（M1 以降）で、**macOS 15 以上**
- **Windows**：Windows 11

## 入れる

[Releases](../../releases/latest) の「Assets」から、自分のパソコンの分を1つ落としてください。

| パソコン | 落とすファイル |
|---|---|
| Mac | `Ciel-<版>.dmg`（例 `Ciel-1.5.9.dmg`） |
| Windows 11 | `Ciel-<版>-setup.exe` |

### Mac

1. 落とした dmg をダブルクリックする
2. 出てきた窓の **Ciel** を、**アプリケーション** フォルダへドラッグする
3. アプリケーションの **Ciel** を開く
   （はじめては「インターネットからダウンロードされたアプリです」と聞かれます。「開く」を押してください）
4. ブラウザが開いて、そのまま使えます

画面の上のメニューバーに **Ciel** が出ます。止めるときは、そこから「Cielを終了」。

### Windows 11

1. 落とした setup.exe をダブルクリックする
2. 「Windows によって PC が保護されました」と出たら、「詳細情報」→「実行」を押す
   （まだ署名をしていないため出ます）
3. 入れる画面は「次へ」で進めて、最後の画面で「Ciel を開く」にチェックが入ったまま「完了」を押す
4. ブラウザが開いて、そのまま使えます

止めるときは、スタートメニューの **Ciel を終了**。次からはスタートメニューの **Ciel** で立ち上がります。

### Codex で使う人

Claude Code と Codex の両方が入っていると、Claude Code の方で立ち上がります。
Codex にしたいときは、設定ファイル（Mac は `~/.config/ciel/ciel.toml`、Windows は `%USERPROFILE%\.config\ciel\ciel.toml`）の
`[[windows]]` の中の `command = "claude …"` の行を `command = "codex"` にして、Ciel を立ち上げ直してください。

## 1.5.0〜1.5.3 を入れた方へ

1.5.0〜1.5.3 には、**画面に「新しい版」が出ない（アプリの中で更新できない）**穴がありました。
Windows の 1.5.0・1.5.1 は、**Claude Code の窓が開かない**穴もありました。
お手数ですが**一度だけ**、手で入れ直してください。**設定と合言葉は残ります。** 次からは「新しい版」から更新できます。

**Mac**

1. メニューバーの **Ciel** →「Cielを終了」で止める
2. 上の「入れる」の手順で、新しい dmg の **Ciel** を **アプリケーション** へドラッグする（「置き換えますか」と聞かれたら「置き換える」）

**Windows**

1. スタートメニューの **Ciel を終了** で止める
2. 上の「入れる」の手順で、新しい setup.exe を入れる（前の版の上にそのまま入ります）

## 前の版（1.4.0 まで）を入れた方へ

1.4.0 までは `pipx` で入れる形でした。**一度だけ**、次の手順でアプリに入れ替えてください。
**設定と合言葉は残ります。** ブラウザで入り直す必要もありません。

1. 動いている Ciel を止める（ターミナルや黒い窓で動いていれば、その窓で `Ctrl+C`）。
   Mac で自動起動にしていた人は、先に `ciel autostart off`
2. 前の版を外す：`pipx uninstall ciel`
3. 上の「入れる」の手順でアプリを入れて、開く

## スマホから開く（使いたい人だけ）

Ciel の画面の **Settings → スマホから開く** から、1押しでつなげます。
使うのは **Tailscale**（自分の端末どうしだけをつなぐ無料の VPN）で、インターネットには出ません。
パソコンに Tailscale のアプリを入れる必要はありません。スマホには入れてもらいます（画面に QR が出ます）。

> **気をつけること**
> 合言葉を渡したスマホは、**そのパソコンでコマンドを打てます**。
> スマホを無くしたら、同じ所の「閉じる」を押してください（つないだスマホの合言葉も消えます）。

## 困ったとき

記録は、Mac は `~/Library/Logs/Ciel/Ciel.log`、Windows は `%LOCALAPPDATA%\Ciel\Logs\Ciel.log` にあります。
困ったことは、その最後の数十行を添えて、下の問い合わせへ。

## 問い合わせ

shopsupport0@gmail.com

---

## AI への手順（Claude Code・Codex）

> ここから下は、Claude Code や Codex が読んで進めるための手順です。
> 人が読む必要はありません。使う人は、Claude Code か Codex に次の1文を貼るだけです。
>
> ```
> https://github.com/dbafitge6/ciel-download の README の「AI への手順」どおりに、Ciel を入れて起動まで進めてください
> ```

あなた（Claude Code または Codex）は、この機体に Ciel のアプリを入れて、立ち上げる所まで進めます。
**1手ずつ、結果を確かめてから次へ進んでください。**

### 守ること

- 使う人のファイル・設定を消さない。`~/.config/ciel` と Ciel の置き場（Mac は `~/.ciel`、Windows は `%LOCALAPPDATA%\ciel`）は触らない
- 手順と違うことが起きたら、推測で進めず、出た文面をそのまま使う人に見せて止まる
- 落とすのは、この置き場（`github.com/dbafitge6/ciel-download`）の最新のリリースの物だけ

### 1. 機体を見分ける

- **Mac**：`uname -m` が `arm64`、`sw_vers -productVersion` が 15 以上であること。違えば、対応していないと伝えて止める
- **Windows 11**：PowerShell で進める
- それ以外：対応していないと伝えて止める

`claude --version` か `codex --version` のどちらかが動くことを確かめる。どちらも動かなければ、
上の「要るもの」の住所を使う人に見せて、入れてもらってから進む。

### 2. 前の版を確かめる

`pipx list` に `ciel` が出たら、前の版（1.4.0 まで）が入っている。使う人に「前の版を外してアプリに入れ替えます。設定と合言葉は残ります」と伝え、
動いている Ciel を止めてもらってから（Mac で自動起動なら `ciel autostart off` も）、`pipx uninstall ciel` を打つ。

Windows で `$env:LOCALAPPDATA\Programs\Ciel\Ciel.exe` が在れば、アプリの形の前の版が入っている。使う人に「新しい版を上に入れ直します。設定と合言葉は残ります」と伝え、
スタートメニューの「Ciel を終了」で止めてもらってから、3. へ進む（setup.exe は前の版の上にそのまま入る）。
Mac で `/Applications/Ciel.app` が在れば、同じように伝え、メニューバーの Ciel →「Cielを終了」で止めてもらう。
3. の「`/Applications/Ciel.app` が既に在れば、上書きせずに使う人に聞く」で、置き換えてよいかを聞いてから置き換える。

### 3. 落として入れる

**Mac**

```
URL=$(curl -fsSL https://api.github.com/repos/dbafitge6/ciel-download/releases/latest | grep -o '"browser_download_url": *"[^"]*\.dmg"' | head -1 | sed 's/.*"\(https[^"]*\)"/\1/')
curl -fL -o /tmp/Ciel.dmg "$URL"
hdiutil attach -nobrowse -quiet -mountpoint /tmp/ciel-dmg /tmp/Ciel.dmg
```

`/Applications/Ciel.app` が既に在れば、上書きせずに使う人に聞く。無ければ：

```
cp -R /tmp/ciel-dmg/Ciel.app /Applications/
hdiutil detach -quiet /tmp/ciel-dmg
open -a /Applications/Ciel.app
```

**Windows 11**

```
$r = Invoke-RestMethod https://api.github.com/repos/dbafitge6/ciel-download/releases/latest
$u = ($r.assets | Where-Object name -like '*-setup.exe' | Select-Object -First 1).browser_download_url
Invoke-WebRequest $u -OutFile "$env:TEMP\Ciel-setup.exe" -UseBasicParsing
Start-Process "$env:TEMP\Ciel-setup.exe" -ArgumentList '/VERYSILENT','/SUPPRESSMSGBOXES','/NORESTART' -Wait
Start-Process "$env:LOCALAPPDATA\Programs\Ciel\Ciel.exe"
```

### 4. 確かめる

20秒ほど待って、`http://127.0.0.1:8765/enroll` が 200 を返すことを確かめる
（Mac は `curl -s -o /dev/null -w "%{http_code}"`、Windows は `(Invoke-WebRequest http://127.0.0.1:8765/enroll -UseBasicParsing).StatusCode`）。
返らなければ、さらに20秒待ってもう1度。それでも返らなければ、上の「困ったとき」の記録の最後の30行を使う人に見せて止まる。

### 5. 使う人に伝える

- ブラウザが開いて、そのまま使えること（開いていなければ `http://127.0.0.1:8765/` を開いてもらう）
- 止めるとき：Mac はメニューバーの Ciel →「Cielを終了」、Windows はスタートメニューの「Ciel を終了」
- 当面無料で使えること。問い合わせは shopsupport0@gmail.com
