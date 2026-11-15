# XChange fingerprint probe

The page a person opens to turn their computer into a persona for the XChange
catalogue: the machine's GPU, screen, fonts and speech-synthesis voices, measured
in ordinary Chrome.

Open **https://dx5tool.github.io/detect-suite/** in Google Chrome — not XChange,
not another anti-detect browser. A persona has to describe the machine, not the
browser running on top of it.

1. Press «Снять отпечаток», then «Скачать JSON». The file stays on your machine;
   the page sends nothing anywhere.
2. Drop the file into
   [the issue form](https://github.com/dx5tool/tiktoklead/issues/new?template=persona.yml)
   and say what the machine is. GitHub attaches it for you.

The capture is converted with `xchange-detect persona` and checked with
`personas-check` — the same code the application ships — and the machine joins the
catalogue under your handle.

**The file is your computer's fingerprint.** Publishing it publishes how your
computer looks to every site it visits. Capture from a machine that does not run
live accounts. There is no personal data in it — no name, no addresses, no
history — but the GPU serial and the font list are enough to recognise the machine.

## What this repository is

`probe.html`, `probe.js` and `sw-probe.js` are the probe exactly as it ships in
XChange's detect-suite, plus the landing page. Nothing else — the browser, the
agent and the application are not here.

The probe has to run in a browser, so its JavaScript is public by nature: the
page this repository serves is the same code anybody loads to measure a machine.

## Licence

AGPL-3.0-or-later. See [LICENSE](LICENSE).
