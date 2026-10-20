# Práctica 04: CI/CD con GitHub Actions y Databricks Asset Bundles

Proyecto de partida (bundle del Laboratorio 08 + workflows). Sigue el documento
"Laboratorio04_CICD_GitHub_Actions.docx" paso a paso.

Resumen:
1. En Databricks: crea el Service Principal `sp-dab-cicd`, genera su secret y otórgale
   permisos sobre `dab_lab_dev` y `dab_lab_prod` (catalog, esquema y Volume `health`).
2. En GitHub: crea el repo, sube `main`, crea la rama `dev`, y guarda 3 Repository secrets:
   `DATABRICKS_HOST`, `DATABRICKS_CLIENT_ID`, `DATABRICKS_CLIENT_SECRET`.
3. Trabaja en una rama `feature/...`, abre un PR hacia `dev` (corre `validate`), mergea
   (corre `deploy` + `run`), y luego promueve con un PR `dev` -> `main`.

Importante: `.github/workflows/` debe existir en `dev` Y en `main`.
