# Create a FLOSS scan micro-service :new: :construction:

```bash
$ docker run -d -p 3993:3993 malice/floss web

INFO[0000] web service listening on port :3993
```

## Now you can perform scans like so

```bash
$ http -f localhost:3993/scan malware@/path/to/evil/malware
```

> **NOTE:** I am using **httpie** to POST to the malice micro-service

```bash
HTTP/1.1 200 OK
Content-Length: 124
Content-Type: application/json; charset=UTF-8
Date: Sat, 21 Jan 2017 05:39:29 GMT

{
  "floss": {
    "decoded": [
      {
        "Location": "0x401047",
        "Strings": [
          "Ie_nkokbpAtep",
          "+^]g*dpi",
          "Ie_nkokbpD]ra=_g"
        ]
      },
      {
        "Location": "0x401059",
        "Strings": [
          "*lecnaC*",
          "Software\\Microsoft\\CurrentNetInf",
          "SYSTEM\\CurrentControlSet\\Control\\Lsa",
          "Software\\Microsoft\\Windows\\CurrentVersion\\Policies\\Explorer\\Run",
          "MicrosoftZj",
          "LhbqnrnesDwhs",
          "MicrosoftHaveExit",
          "LhbqnrnesG`ud@bj",
          "IEXPLORE.EXE",
          "/ver.htm",
          "/exe.htm",
          "/app.htm",
          "/myapp.htm",
          "/hostlist.htm",
          ".a`j-gsl",
          "/SomeUpList.htm",
          "/SomeUpVer.htm",
          "www.flyeagles.com",
          "www.km-nyc.com",
          "/restore",
          "/dizhi.gif",
          "/connect.gif",
          "\\$NtUninstallKB900727$",
          "\\netsvc.exe",
          "\\netscv.exe",
          "\\netsvcs.exe",
          "System Idle Process",
          "Program Files",
          "\\Internet Exp1orer",
          "forceguest",
          "AudioPort",
          "AudioPort.sys",
          "SYSTEM\\CurrentControlSet\\Services",
          "SYSTEM\\ControlSet001\\Services",
          "SYSTEM\\ControlSet002\\Services",
          "\\drivers\\",
          "\\DriverNum.dat"
        ]
      },
      {
        "Location": "0x40511A",
        "Strings": [
          "\\A|{@"
        ]
      },
      {
        "Location": "0x403DDA",
        "Strings": [
          ",pVA."
        ]
      },
      {
        "Location": "0x404DDE",
        "Strings": [
          "SMBs",
          "NTLMSSP",
          "Windows 2000 2195",
          "Windows 2000 5.0",
          "SMBr",
          "PC NETWORK PROGRAM 1.0",
          "LANMAN1.0",
          "Windows for Workgroups 3.1a",
          "LM1.2X002",
          "LANMAN2.1",
          "NT LM 0.12"
        ]
      }
    ],
    "stack": [
      "\\A|{@",
      "CAAA\\",
      "cmd.exe"
    ]
  }
}
```
