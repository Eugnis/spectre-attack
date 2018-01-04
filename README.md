# Spectre Attack Example
Example of using revealed "Spectre" exploit from 2 Jan 2018 (CVE-2017-5753 and CVE-2017-5715)

Spectre breaks the isolation between different applications. It allows an attacker to trick error-free programs, which follow best practices, into leaking their secrets. In fact, the safety checks of said best practices actually increase the attack surface and may make applications more susceptible to Spectre.

* [Spectre paper] - Spectre paper and source of code

## Language
C, uses libs:
* stdio.h
* stdlib.h
* stdint.h
* intrin.h - for rdtscp and clflush

## What's example do?
In this example we're putting text "The Magic Words are Squeamish Ossifrage." in memory and then we're trying to read it using exploit. If system is vulnerable, you'll see same text in output, readed from memory.

## Sources
* [Spectre exploits info]
* [CVE-2017-5753] - Variant 1: bounds check bypass
* [CVE-2017-5715] - Variant 2: branch target injection

[Spectre paper]: <https://spectreattack.com/spectre.pdf>
[Spectre exploits info]: <https://spectreattack.com>
[CVE-2017-5753]: <http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=2017-5753>
[CVE-2017-5715]: <http://www.cve.mitre.org/cgi-bin/cvename.cgi?name=2017-5715>
