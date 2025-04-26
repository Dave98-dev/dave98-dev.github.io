---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---

[vai al bot](bot)

# Bot di twitch

questo sito è un pannello di controllo per una serie di bot che seguono un copione

## il copione

il copione dovrà essere fornito seguendo questa espressione regolare

```
^(\d\d:\d\d)(\.\d\d\d)?\s(\w+)\s(.*)$
```

ecco un paio di righe di esempio

```
00:00 david hello everyone, how are you guys doing?
00:01 jake i'm doing ok, hbu?
00:01.500 mark i'm speaking too
00:02 david i'm doing good
```

le righe hanno queste informazioni

1. ### timestamp

   **00:00** david hello everyone, how are you guys doing?

   l'orario nel quale verrà mostrato il messaggio. deve avere minuti e secondi e opzionalmente può avere i millisecondi, come nell'esempio

   00:01**.500** mark i'm speaking too

   ### IMPORTANTE

   i messaggi **devono** essere messi nel copione in ordine dal messaggio più vecchio a quello più recente

2. ### username

   00:00 **david** hello everyone, how are you guys doing?

   username, non inserire caratteri speciali nel nome, lo username non deve per forza combaciare con un vero utente twitch.

   sarà presente un **dizionario** che si userà per collegare un username con un **Token di autenticazione**

   per sapere come creare questo token seguire [questa guida](https://dev.twitch.tv/docs/authentication/getting-tokens-oauth/){:target="\_blank"}

3. ### messaggio

   00:00 david **hello everyone, how are you guys doing?**

   questo è il messaggio che verrà inviato. non dovrebbero esserci problemi con caratteri speciali ma un controllo sicuramente non fa male

## Prova il bot

clicca [qui](bot) per vedere il bot dal vivo
