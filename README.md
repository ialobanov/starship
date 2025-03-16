# Starship configuration

```powershell
vim $env:USERPROFILE\starship.toml
```

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
format = '[$path ]($style)'
# format = '[$path]($style)[$read_only]($read_only_style) '
fish_style_pwd_dir_length = 0
use_logical_path = false

[git_branch]
symbol = ' '
truncation_length = 255
truncation_symbol = ''

[git_status]
up_to_date = '󰸞'

# [git_status]
# conflicted = '🏳'
# ahead = '🏎💨'
# behind = '😰'
# diverged = '😵'
# up_to_date = '󰸞'
# untracked = '🤷'
# stashed = '📦'
# modified = '📝'
# staged = '[++\($count\)](green)'
# renamed = '👅'
# deleted = '🗑️'

[fill]
symbol = ' '

[lua]
format = 'via [$symbol($version )]($style)'
symbol = ' '

[jobs]
symbol = ' '
style = 'red'
number_threshold = 1
format = '[$symbol]($style)'

[cmd_duration]
min_time = 5000

[docker_context]
format = 'via [🐋 $context](blue bold)'

[memory_usage]
disabled = false
threshold = -1
symbol = ' '
format = '$symbol [${ram}]($style) '
style = 'green'

[battery]
full_symbol = '🔋 '
charging_symbol = '⚡️ '
discharging_symbol = '💀 '

[[battery.display]]
threshold = 10
style = 'red'
discharging_symbol = '󰂎 '

[[battery.display]]
threshold = 80
style = 'yellow'
discharging_symbol = '󰁽 '

[character]
disabled = false
success_symbol = '[➜](bold green)'
error_symbol = '[➜](bold red)'
vimcmd_symbol = '[⮜](bold green)'
vimcmd_replace_one_symbol = '[⮜](bold purple)'
vimcmd_replace_symbol = '[⮜](bold purple)'
vimcmd_visual_symbol = '[⮜](bold yellow)'
```

