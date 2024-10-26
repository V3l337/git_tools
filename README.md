
# Ответы на задания по репозиторию Terraform

## 1. Полный хеш и комментарий коммита, хеш которого начинается на `aefea`

Для поиска полного хеша и комментария коммита использовалась следующая команда:

```bash
git log --oneline | grep aefea
```

**Результат:**
```
aefead2207 Update CHANGELOG.md
```

---

## 2. Какому тегу соответствует коммит `85024d3`?

Команда для получения информации о тегах, соответствующих коммиту:

```bash
git tag --contains 85024d3
```

**Результат:**
- v0.12.23
- v0.12.24
- v0.12.25
- v0.12.26
- v0.12.27
- v0.12.28
- v0.12.29
- v0.12.30
- v0.12.31

---

## 3. Сколько родителей у коммита `b8d720`? Напишите их хеши.

Чтобы узнать количество родителей и их хеши, была использована команда:

```bash
git rev-list --parents -n 1 b8d720
```

**Результат:**
- Хеши родителей:
  - `56cd7859e05c36c06b56d013b55a252d0bb7e158`
  - `9ea88f22fc6269854151c571162c5bcf958bee2b`

---

## 4. Хеши и комментарии всех коммитов, сделанных между тегами `v0.12.23` и `v0.12.24`. 

Для перечисления коммитов использовалась команда:

```bash
git log v0.12.23..v0.12.24 --oneline
```

**Результат:**
```
33ff1c03bb (tag: v0.12.24) v0.12.24
b14b74c493 [Website] vmc provider links
3f235065b9 Update CHANGELOG.md
6ae64e247b registry: Fix panic when server is unreachable
5c619ca1ba website: Remove links to the getting started guide's old location
06275647e2 Update CHANGELOG.md
d5f9411f51 command: Fix bug when using terraform login on Windows
4b6d06cc5d Update CHANGELOG.md
dd01a35078 Update CHANGELOG.md
225466bc3e Cleanup after v0.12.23 release
```

---

## 5. Найдите коммит, в котором была создана функция `func providerSource`. 

Команда для поиска коммита с определением функции:

```bash
git log -S 'func providerSource' --oneline
```

**Результат:**
```
5af1e6234a main: Honor explicit provider_installation CLI config when present
8c928e8358 main: Consult local directories as potential mirrors of providers
```

---

## 6. Найдите все коммиты, в которых была изменена функция `globalPluginDirs`. 

Для нахождения коммитов использовалась команда:

```bash
git log -S 'globalPluginDirs' --oneline
```

**Результат:**
```
65c4ba7363 Remove terraform binary
125eb51dc4 Remove accidentally-committed binary
22c121df86 Bump compatibility version to 1.3.0 for terraform core release (#30988)
7c7e5d8f0a Don't show data while input if sensitive
35a058fb3d main: configure credentials from the CLI config file
c0b1761096 prevent log output during init
8364383c35 Push plugin discovery down into command package
```

---

## 7. Кто автор функции `synchronizedWriters`?

Для определения автора использовалась команда:

```bash
git log -S 'synchronizedWriters' --pretty=format:'%h %an'
```

**Результат:**
```
bdfea50cc8 James Bardin
fd4f7eb0b9 James Bardin
5ac311e2a9 Martin Atkins
```

---
