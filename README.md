# static web

This role clones git repository to the given directory on the target server.


## Requirements

None 

## Role Variables

| Variable name | Required | Description |
| -------- | -------- | -------- |
| `static_web_folder_to_copy`     | :heavy_check_mark:     | The variable contains every pair of `src` and `to` that is needed to deploy a git repository     |
| `static_web_folder_to_copy[0].src`     | :heavy_check_mark:     | `src` variable can be anything that git allows as source |
| `static_web_folder_to_copy[0].to`     | :heavy_check_mark:     | Path to clone the git repository to |


## Example Playbook
```
static_web_folder_to_copy:
  - src: git@github.com:stuvusIT/www_ak_quer
    to: /var/www/ak_quer
  - src: git@github.com:stuvusIT/www_uno
    to: /var/www/uno
  - src: git@github.com:stuvusIT/www_campusbeach
    to: /var/www/campusbeach
  - src: git@github.com:stuvusIT/www_fsen_paedagogik
    to: /var/www/paedagogik
  - src: git@github.com:stuvusIT/www_fsen_sozialwissenschaften
    to: /var/www/www_fsen_sozialwissenschaften
  - src: git@github.com:stuvusIT/www_ak_zeitung
    to: /var/www/zeitung
```

## License

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).


## Author Information

 * [Fritz Otlinghaus (Scriptkiddi)](https://github.com/Scriptkiddi) _fritz.otlinghaus@stuvus.uni-stuttgart.de_
