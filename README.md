# Plantilla Jekyll — Cròniques de la Família

Aquesta plantilla està pensada per publicar **cròniques familiars** organitzades per:

- **Períodes** (cada període = vida d’un patriarca/matriarca)
- **Històries** (fets/relats dins d’un període, amb data i etiquetes)

## Estructura

- `_periodes/` → fitxes de cada període (patriarca)
- `_histories/` → relats/històries (cada fitxer és una història)
- `index.md` → portada amb llista de períodes i últimes històries
- `timeline.md` → línia temporal de totes les històries

## Com executar en local

> Requisits: Ruby + Bundler

```bash
bundle install
bundle exec jekyll serve
```

La web s’obrirà a `http://localhost:4000`.

## Publicar a GitHub Pages (recomanat)

1. Puja aquest projecte a un repositori.
2. Activa **Settings → Pages**.
3. Recomanat: configura l’opció de GitHub Actions per construir Jekyll.

## Afegir contingut

### 1) Crear un període
Crea un fitxer a `_periodes/` com `1900-1960-joan.md`.

### 2) Crear una història
Crea un fitxer a `_histories/` com `1924-casament.md` i indica a quin període pertany amb `periode: joan`.

---

Bon projecte! 📚
