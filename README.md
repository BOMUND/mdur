# Media Duration Analyzer (mdur)

Утилита командной строки для анализа длительности медиафайлов (видео и аудио).

## Возможности

- **Анализ общей длительности** - быстро посчитать суммарное время всех медиафайлов
- **Подробный детальный вывод** - таблица с информацией о каждом файле
- **Гибкая сортировка** - по имени, длительности или формату
- **Широкая поддержка форматов** - более 20 популярных видео и аудио форматов
- **Рекурсивный поиск** - анализ вложенных каталогов (по умолчанию)
- **Фильтрация по типам файлов** - анализировать только нужные форматы
- **Подробный режим** - отображение прогресса и детальной информации

## Установка

```bash
curl -sSL https://raw.githubusercontent.com/BOMUND/mdur/main/install.sh | sudo bash
```

## Использование

```bash
## Основной синтаксис
mdur [ОПЦИИ] [КАТАЛОГ]
# Базовая проверка текущего каталога
mdur

# Проверка конкретного каталога
mdur ~/Videos

# Проверка только 1 конкретного каталога без рекурсии
mdur -r ~/Videos  

# Детальный вывод с сортировкой по имени (n|name)
mdur -s n

# Только MP4/MOV файлы с подробным выводом
mdur -t mp4,mov -v

# Справка
mdur --help
```

## Параметры

| Параметр       | Описание                              |
|----------------|---------------------------------------|
| `-h`, `--help` | Показать справку                      |
| `-r`, `--no-recur` | Отключить рекурсивный поиск       |
| `-s`, `--sort` | Сортировка (n|name, d|duration, f|format) |
| `-t`, `--types`| Типы файлов (mp4,mp3 и т.д.)          |
| `-f`, `--format`| Показать формат файлов              |
| `-v`, `--verbose`| Подробный режим вывода             |


## Требования

- Bash 4.0+
- ffmpeg (для ffprobe)
- Linux/macOS

## Лицензия

[MIT](LICENSE)
