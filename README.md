# devops-ci-app

Учебное Flask-приложение для практической работы №10.
Тараканов Леонид Валентинович, ЭФБО-11-24.

CI: Pylint → pytest → Docker build → smoke-test → GHCR.
Публикация образа выполняется только из `main`. В Pull Request выполняются проверки без push.

- health endpoint: `/health`;
- образ: `ghcr.io/inexcusableevil/devops-ci-app`;
- workflow: `.github/workflows/ci.yml`.

Сборка и smoke-test выполняются на стандартном ARM64 runner `ubuntu-24.04-arm`,
чтобы опубликованный образ подходил учебной VM на Mac ARM64.
Адаптация архитектуры согласована владельцем стенда.
