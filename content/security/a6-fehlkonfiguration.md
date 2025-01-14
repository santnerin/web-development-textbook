---
title: A6 - Fehlkonfiguration
order: 60
---

Auf [Platz 6 der OWASP Top 10 2017](https://owasp.org/www-project-top-ten/2017/de/A6_2017-Sicherheitsrelevante_Fehlkonfiguration).

Die OWASP beschreibt dieses Problem allgemein so:

> Sicherheitsrelevante Fehlkonfiguration kann auf jeder Ebene der Anwendung, inkl. Plattform, Web- und Anwendungs-server, Frameworks oder Programmcode vorkommen. Die Zusammenarbeit zwischen Entwicklern und Administratoren ist wichtig, um eine sichere Konfiguration aller Ebenen zu gewährleisten.

In größeren Projekten / Firmen ist eine Arbeitsteilung üblich zwischen
Entwicklung (Development) und Systemadmistration (Operations).

## Ebenen

Für eine Web-Applikation muss man dabei mindestens folgende Schichte beachten:

- Physikalische Sicherheit (Wer kann den Server ein- und ausschalten, zerlegen,...)
- Virtualisierungs-Schicht, z.B. VMWare
- Betriebssystem, z.B. Ubuntu, CentOS, Debian
- Datenbank, z.B. PosgreSQL, MySQL, MongoDB
- Interpreter, z.B. PHP, Ruby
- Webserver, z.B. Apache, nginx
- Framework, z.B. Laravel, Rails
- Fremd-Applikation, z.B. Wordpress, Redmine
- Selbstgeschreibene Applikation

Jeder dieser Schichten gilt es richtig zu konfigurieren
und Sicherheits-Updates einzuspielen.

Wenn es eine Arbeitsteilung zwischen Development und Operations gibt
ist zu klären wer für welche Schicht zuständig ist.

## Konfiguration + Hardening

Zwei Szenarien:

- Entwicklungs-Rechner: möglichst viele Debug-Möglichkeiten, Bequemlichkeit wichtiger als Sicherheit
- Produktions-Server: Sicherheit wichtiger als Bequemlichkeit, Logging / Monitoring ja, aber nicht öffentlich zugänglich

Dafür gibt es oft schon fertige Konfigurationen, oder Tutorials. Ein guter Suchbegriff ist "hardening". 

## Sicherheitsupdates

Keine Software ist sicher, in jeder Software werden Sicherheitsprobleme
entdeckt. Die relevante Fragen sind: werden Sicherheitsprobleme die
bekannt werden möglichst schnell behoben? Und in Folge: Wenn ein Update
zur Verfügung steht, wird es möglichst schnell installiert?

- [Heise Security](http://www.heise.de/security/)

