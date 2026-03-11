# Python Virtual Environments

Správa izolovaných Python prostředí.

## Basic

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

```bash
# Kontrola aktivního Pythonu
which python && python --version

# Ověření aktivace venv
echo $VIRTUAL_ENV

# Přeinstalace všech balíčků
pip install -r requirements.txt --force-reinstall
```

## Common Mistakes

- Commitování .venv do gitu — vždy přidejte do .gitignore.
- Použití systémového Pythonu místo venv Pythonu.
- Nespecifikování verzí závislostí v requirements.txt.
