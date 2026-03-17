# 2026-calcolatrice

Adesso ho la:

- somma



## Setup ambiente di sviluppo con uv

Installare [uv](https://docs.astral.sh/uv/) per gestire l'ambiente di sviluppo:

```bash 
- uv venv
- source .venv/bin/activate  ( o equivalente su Windows )
- uv pip compile requirements.in -o requirements.txt
- uv pip install -r requirements.txt
```

## Testing con pytest

Useremo [pytest](https://docs.pytest.org/en/stable/) per eseguire i tests:

### Eseguire i test

Per eseguire tutti i test nel progetto:

```bash
pytest -v
```

Per eseguire i test in un file specifico:

```bash
pytest test/test_somma.py -v
```

### Scrivere test

I test sono organizzati nella cartella `test/`. Ogni file di test dovrebbe iniziare con `test_` e contenere funzioni che iniziano con `test_`.

Esempio di test per la funzione `somma`:

```python
from funzioni.somma import somma

def test_somma_positivi():
    assert somma(1, 2) == 3

def test_somma_con_zero():
    assert somma(0, 5) == 5
```

I test utilizzano `assert` per verificare che il risultato sia corretto. Se l'assert fallisce, pytest mostra un errore dettagliato.
