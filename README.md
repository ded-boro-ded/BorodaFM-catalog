# BorodaFM — каталог станций

Публичный каталог для авто-обновления списка станций в приложении BorodaFM.
Код приложения здесь не хранится.

- `stations.json` — список станций (обёртка: `schema` / `version` / `updatedAt` / `stations`).
- `stations.json.sig` — detached-подпись (`ECDSA P-256`, `SHA-256`), base64 (DER).

Раздаётся через GitHub Pages:
`https://ded-boro-ded.github.io/BorodaFM-catalog/stations.json`

Обновление публикуется из основного репозитория BorodaFM:
```
python3 tools/publish_catalog.py --out-dir /Users/ded/Documents/BorodaFM-catalog --push
```

Подпись проверяется приложением публичным ключом `CATALOG_PUBLIC_KEY`.
Приватный ключ в git не хранится (`tools/catalog_key.pem` в основном репозитории).
