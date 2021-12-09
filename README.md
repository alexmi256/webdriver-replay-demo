# What?
WebDriverIO + ReplayIO demo
Record tests using the custom ReplayIo browser recorder

# Install

```bash
wget https://static.replay.io/downloads/linux-replay-chromium.tar.xz
wget https://static.replay.io/downloads/linux-replay.tar.bz2
tar -jxf linux-replay-chromium.tar.xz -C replay-chromium/
tar -jxf linux-replay.tar.bz2 -C replay/
npm install
```

# Running
Export environment variables so that Replay browser will record on start.
```bash
export BROWSER=chrome
export RECORD_REPLAY_API_KEY=<your replay API key>
export RECORD_ALL_CONTENT=1
node node_modules/@wdio/cli/bin/wdio.js run wdio.conf.js
```

Finding and uploading replay
```bash
replay-recordings ls
replay-recordings upload <replay id>
```

# Notes
- Don't use [geckodriver 0.30.0](https://github.com/mozilla/geckodriver/issues/1935)
