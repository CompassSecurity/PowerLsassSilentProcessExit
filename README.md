# PowerLsassSilentProcessExit

PowerShell script to dump lsass.exe process memory to disk for credentials extraction via silent process exit mechanism.

## Description

The script causes WerFault.exe to dump lsass.exe process memory to disk for credentials extraction via silent process exit mechanism without crasing lsass.exe. This technique is adapted from: https://github.com/deepinstinct/LsassSilentProcessExit

## Parameters

### DumpMode

- 0 - Call RtlSilentProcessExit on LSASS process handle
- 1 - Call CreateRemoteThread with RtlSilentProcessExit on LSASS

### DumpPath
- Path wherer the dumpfile shall be stored

### Demo

The following demo shows the dumping:

![Demo](demo.gif)

## Known Issue

At the time of writing, we could not get the DumpMode 1 (using CreateRemoteThread) to work.

## Authors

- Ville Koch ([Twitter](https://twitter.com/vegvisir87))
- Sylvain Heiniger ([Twitter](https://twitter.com/sploutchy))
