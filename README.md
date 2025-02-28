# My Starship configuration for Windows machine

```toml
format = """
$directory\
$git_branch\
$git_status\
$fill\
$memory_usage\
$battery\
$lua\
$jobs\
$cmd_duration\
$line_break\
$docker_context\
$character"""

[directory]
truncation_length = 0
truncate_to_repo = false
format = '[$path]($style)[$read_only]($read_only_style) '
fish_style_pwd_dir_length = 0

[git_branch]
symbol = '🌱 '
truncation_length = 4
truncation_symbol = ''
#ignore_branches = ['master', 'main']

[git_status]
conflicted = '🏳'
ahead = '🏎💨'
behind = '😰'
diverged = '😵'
up_to_date = '✓'
untracked = '🤷'
stashed = '📦'
modified = '📝'
staged = '[++\($count\)](green)'
renamed = '👅'
deleted = '🗑'

[fill]
symbol = ' '

[lua]
format = 'via [󰢱 $version](bold blue) '

[docker_context]
format = 'via [🐋 $context](blue bold)'

[memory_usage]
disabled = false
threshold = -1
symbol = ' '
format = '$symbol [${ram}]($style) '
style = 'bold dimmed green'

[battery]
full_symbol = '🔋 '
charging_symbol = '⚡️ '
discharging_symbol = '💀 '

[[battery.display]]
threshold = 10
style = 'bold red'
discharging_symbol = '󰂎 '

[[battery.display]]
threshold = 80
style = 'bold yellow'
discharging_symbol = '󰁽 '
```
