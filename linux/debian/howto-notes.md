# Linux/debian How-To Notes

Průběžně ukládané praktické poznámky z raw LLM odpovědí.

## Basic

<!-- Jak na běžné postupy -->

<!-- raw-note:78d401481e58 -->
### Pro výměnu klíčů a nastavení bezheslového přihlašování můžete použít následující příkaz:

```bash
ssh-copy-id username@ip_adresa
```

Tento příkaz kopíruje váš veřejný SSH klíč do autorizačního souboru na cílovém zařízení, čímž umožní bezheslové přihlášení.

Pokud nemáte vygenerovaný žádný SSH klíč, můžete jej vytvořit pomocí:

```bash
ssh-keygen
```

Tento příkaz vás provede procesem generování nového klíče. Ve výchozím nastavení bude klíč uložen v ~/.ssh/id_rsa a ~/.ssh/id_rsa.pub.

Po erfolgreiche instalaci klíče můžete testovat bezheslové přihlášení pomocí:

```bash
ssh username@ip_adresa
```

Z bezpečnostních důvodů je důležité, aby byl váš soukromý klíč (id_rsa) chráněn heslem a uložen na bezpečném místě. Nikdy jej nedávejte nikomu jinému.

Pokud chcete automatizovat tento proces pro více zařízení, můžete použít skript, který bude iterovat přes seznam IP adres a uživatelů, nicméně to již vyžaduje znalost programování a práce se skripty.

## Advanced

<!-- Pokročilé varianty -->

## Troubleshooting

<!-- Diagnostické a opravné kroky -->

## Common Mistakes

<!-- Časté chyby a anti-patterny -->
