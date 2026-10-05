# Kein AI Slop

Entfernt über 25 typische KI-Muster aus deutschen Texten, ohne deine persönliche Stimme zu glätten.

## Problem

Mit KI entstehen schnell saubere Texte, die alle gleich klingen. Auf Deutsch kommt etwas dazu: Viele KI-Texte lesen sich wie übersetzt. Typisch sind Sätze wie diese:

- „Es geht nicht um X. Es geht um Y.“
- „Was dir niemand sagt …“
- „Am Ende des Tages macht das den Unterschied.“
- „Die Durchführung der Optimierung erfolgt im Rahmen des Projekts.“

Wer KI zum Überarbeiten nutzt, verliert außerdem oft genau den Wortschatz, die Satzmelodie, den Humor und die Ecken, die einen Text nach dir klingen lassen.

## Installation

Am einfachsten fügst du das in ChatGPT, Claude Code, Codex oder deinen Coding-Agenten ein:

```text
Installiere den Skill /kein-ai-slop global von https://github.com/vanHolk/kein-ai-slop
```

Oder mit `npx`:

```sh
npx skills add vanHolk/kein-ai-slop --skill kein-ai-slop --global --yes
```

## Nutzung

### Text überarbeiten

```text
/kein-ai-slop (dein Text)
```

Der Skill entfernt die KI-Muster, bewahrt deine Stimme und listet auf, was er geändert hat.

### Text prüfen

```text
/kein-ai-slop Ist das Slop? (dein Text)
```

Der Skill zitiert jedes gefundene Muster, ohne zu raten, ob eine KI den Text geschrieben hat.

### Slop zum Spaß erzeugen

```text
Schreib einen LinkedIn-Post über (Thema) voller KI-Slop
```

Für Satire: der peinlichste KI-Text, der möglich ist.

## Was der Skill findet

Kein AI Slop prüft über 25 Muster, darunter:

1. **Übersetzungsdeutsch.** „Am Ende des Tages“, „einen Unterschied machen“, „in 2026“
2. **Nominalstil.** „Die Umsetzung der Maßnahme erfolgt zeitnah.“
3. **Binäre Kontraste.** „Das ist kein Tool. Das ist eine Haltung.“
4. **Vorgeplänkel.** „Mal ehrlich:“, „Klartext:“
5. **Falsche Geheimtipps.** „Was dir niemand sagt“, „Was die meisten übersehen“
6. **Doppelpunkt-Enthüllungen.** „Das Beste daran: Es lernt.“
7. **Dramatische Fragmente.** „Das war's. Mehr nicht.“
8. **Bedeutungsgetue.** „ein Meilenstein“, „ein Zeugnis für“, „setzt neue Maßstäbe“
9. **Wieselformulierungen.** „Experten sind sich einig“, „Studien zeigen“
10. **Synonymkarussell.** „Der Agent prüft deine Mails. Der Assistent schreibt Antworten.“
11. **Pseudotiefe Schlusssätze.** „Die Zukunft kommt nicht. Sie ist längst da.“
12. **Englische Typografie.** "Gerade Anführungszeichen", Geviertstriche, Title Case in Überschriften

Dazu prüft er die Grundlagen: Verben statt Substantive, Aktiv statt Passiv, entwirrte Schachtelsätze und konkrete Details statt Abstraktionen. Anrede (Du oder Sie), Gender-Schreibweise und Sprachvariante (Deutschland, Österreich, Schweiz) übernimmt er vom Original und macht sie nur einheitlich.

## Inhalt

- [`SKILL.md`](skills/kein-ai-slop/SKILL.md) enthält die Regeln und den Ablauf.
- [`eval.md`](skills/kein-ai-slop/eval.md) enthält die Prüfliste, mit der der Skill seine Arbeit kontrolliert.
- [`.codex-plugin/plugin.json`](.codex-plugin/plugin.json) enthält die Plugin-Metadaten für ChatGPT und Codex.
- [`build_plugin.py`](scripts/build_plugin.py) baut und validiert das Plugin-Paket.

## Herkunft

Kein AI Slop ist eine deutsche Adaption von [No AI Slop](https://github.com/petergyang/no-ai-slop) von Peter Yang. Regeln, Beispiele und Prüfliste wurden für deutsche Texte neu geschrieben und um deutschsprachige Muster ergänzt.

## Lizenz

MIT
