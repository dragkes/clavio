# Clavio privacy

Clavio needs to be **activated** once per computer (free), and renews that licence automatically about once a year - see *Activation* below. Apart from that, **nothing is sent anywhere unless you agree to it**, and you can change your mind at any time in *Settings > Privacy*. The first time you use the app it asks once; both choices are **off** by default:

- **Send crash reports**
- **Send anonymous usage statistics**

Setting the environment variable `CLAVIO_NO_TELEMETRY=1` switches both off for good, whatever the settings say.

## Activation (required)

The app does not run without a licence for the computer it is installed on. To get one (and to renew it,
about once a year, automatically) it sends the Clavio activation service:

- an anonymous code of the computer: a one-way SHA-256 hash of the operating system's installation id
  (Windows: MachineGuid; macOS: the platform UUID; Linux: machine-id) - the id itself never leaves the
  computer and cannot be worked out from the hash;
- the app version and the name of the operating system (e.g. "Windows 11");
- a random installation number made when Clavio was first started.

The service stores those, the licence number it issues and the dates of the first and last activation. It
does not store your IP address (to stop abuse it counts requests per hour under a salted hash of the IP,
which is deleted after two hours), and it never receives your name, e-mail, files or playing. The licence
itself is kept on your computer and works offline until it expires.

## Anonymous usage statistics (if you agree)

Counted with [Aptabase](https://aptabase.com), a privacy-friendly analytics service (no cookies, no user profiles). Events:

| Event | What it contains |
|---|---|
| `app_started` | app version, operating system name and version, language (en/ru), light or dark theme |
| `feature_used` | the name of a feature (for example `trainer`, `concert`, `phrases`, `duet`, `dynamics`, `find_music`, `improvise`, `record`, `learn_mode_play`), at most once per run |
| `piece_opened` | only the file type (`midi`, `musicxml`, `mscz`) and a rough number of parts (`1`, `2`, `3-4`, `5+`) |
| `app_error` | only the kind of error (for example `KeyError`) |

Every event also carries the time and a random session number made at each start. The session number is not saved and cannot identify you or your computer.

## Crash reports (if you agree)

Sent to [Sentry](https://sentry.io) when the app hits an unexpected error:

- the error type and its message, with every file path removed
- the place in Clavio's own code where it happened (file and line inside the app)
- the app version and the name and version of your operating system

## What is never sent

- your pieces, recordings or the notes you play
- file names, folder names, your user name or your computer's name
- keyboard input, MIDI device names or the values of your settings
- personal data of any kind: no name, e-mail address, licence key or account; no IP address is stored with the data

## Licence keys

A supporter licence key is checked on your own computer (an offline signature check). Entering one contacts no server.

## Control

- *Settings > Privacy* turns each kind off immediately; events that were waiting to be sent are discarded.
- If a build has no reporting service configured, nothing is sent whatever you choose.
- *Settings > Privacy* in the app lists exactly what is and is not sent.

Personal data is handled in line with the UAE Federal Decree-Law No. 45 of 2021 on the Protection of Personal Data.
Contact: support@kaidadrg.xyz
