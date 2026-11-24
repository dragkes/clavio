# Clavio

**Learn and play piano with any MIDI keyboard.** Open sheet music (MusicXML, MuseScore or MIDI files),
play along while Clavio waits for you and scores your notes, practise the hard bars, learn hands
separately or phrase by phrase, play with a band, record yourself and track your progress - in English
and Russian.

## Download

Get the newest version from **[Releases](https://github.com/dragkes/clavio/releases/latest)**:

| System | File |
|---|---|
| Windows 10/11 (64-bit) | `Clavio-<version>-setup.exe` - installer (recommended) |
| | `Clavio-windows-x64-portable.zip` - no installation, unzip and run |
| macOS (Apple Silicon) | `Clavio-macos-arm64.zip` |
| Linux (x64) | `Clavio-linux-x64.tar.gz` |

**Windows**: SmartScreen may warn about an unknown publisher - choose *More info > Run anyway*.
**macOS**: right-click `Clavio.app` > *Open* the first time.
**Linux**: `sudo apt install libfluidsynth3 libportaudio2`, then run `Clavio`.

Clavio updates itself: when a new version is out, the app offers it (you can turn the check off in
*Settings*).

## Activation

Clavio is free. It is activated once per computer, automatically when you install it (or on the first
start). Activation sends only an anonymous code of the computer (a one-way hash, not its serial numbers),
the app version and the name of the operating system - details in the [privacy note](PRIVACY.md).

## Your first steps

1. Connect your MIDI keyboard (USB) before starting Clavio.
2. On first start, choose a sound library (Clavio downloads a free one for you, or use your own `.sf2`).
3. Open a piece in **Learn**, or find free sheet music with **Library > Find music**.

## Verify your download (optional)

Each release has `SHA256SUMS.txt` (the SHA-256 of every file) and its GPG signature `SHA256SUMS.txt.asc`.
The signing key is [`signing-key.asc`](signing-key.asc) in this repository.

```
gpg --import signing-key.asc
gpg --verify SHA256SUMS.txt.asc SHA256SUMS.txt
```
then compare the hash of your file (Windows: `certutil -hashfile <file> SHA256`; macOS / Linux:
`shasum -a 256 <file>`) with the line in `SHA256SUMS.txt`.

## Privacy

Apart from the activation, nothing is sent unless you allow it: crash reports and anonymous usage
statistics are both **off** until you tick them. See [PRIVACY.md](PRIVACY.md).

## Support

Questions, problems, ideas: **support@kaidadrg.xyz** (please add your computer code from
*Settings > Licence* if it is about activation).

## Licence

Clavio is free to use but not open source: see [LICENSE](LICENSE). It contains third-party components
under their own licences, listed in the app under *Help > Licences*. This repository holds the downloads
only.
