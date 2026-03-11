# Python Virtual Environments

Správa izolovaných Python prostředí.

## Basic

- Vytvoření, aktivace a základní práce s venv.

```bash
# Vytvoření virtuálního prostředí
python3 -m venv .venv

# Aktivace (Linux/macOS)
source .venv/bin/activate

# Aktivace (Windows)
.venv\Scripts\activate

# Instalace závislostí
pip install -r requirements.txt

# Deaktivace
deactivate

# Smazání prostředí
rm -rf .venv
```

## Advanced

- Verzování závislostí a údržba balíčků.

```bash
# Vytvoření s konkrétní verzí Pythonu
python3.11 -m venv .venv

# Export instalovaných balíčků
pip freeze > requirements.txt

# Instalace s přesnými verzemi bez závislostí
pip install -r requirements.txt --no-deps

# Výpis zastaralých balíčků
pip list --outdated
```

## Troubleshooting

- Rychlá kontrola aktivního interpreteru a stavu prostředí.

```bash
# Kontrola aktivního Pythonu
which python && python --version

# Ověření aktivace venv
echo $VIRTUAL_ENV

# Přeinstalace všech balíčků
pip install -r requirements.txt --force-reinstall
```

## Common Mistakes

- Commitnutí `.venv` do gitu (chybí `.gitignore`).
- Instalace balíčků mimo aktivní venv.
- `requirements.txt` bez pinovaných verzí.
