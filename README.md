## Инструкция установки Haxe в системе [Ejudge](http://ejudge.ru)

1. Перейти в каталог /home/judges/compile/conf и открываем файл compile.cfg.
2. В конец файла добавить следующий код:

    ```
    [language]
    id = 73
    short_name = «haxe»
    long_name = «Haxe»
    src_sfx = «.hx»
    cmd = «haxe»
    arch = «linux-shared»
    ```
    
3. Перейти в каталог /home/judges/compile/scripts. Создать файлы haxe и haxe-version и в данные файлы вставить код из исходных.
4. В терминале запустить программу ejudge-configure-compilers и проверить наличие ЯП Haxe.
5. Перейти в каталог /home/judges/000001/conf и открыть файл serve.cfg. В него записать строку compile_real_time_limit = 300.
6. Перейти в serve-control и зайти под администратором. (https://localhost/cgi-bin/serve-control)
7. В таблице напротив test contest перейти settings/language settings. В списке найти ЯП Haxe и напротив него нажать activate.
8. Перезапустить ejudge

## Особенности использования

1. Решения участников должны находиться в файле Solution.hx, который должен включать класс Solution с функцией main.
2. Решения будут компилироваться с использованием библиотеки hxcpp в статичные исполняемые файлы.
3. Необходимо принять во внимание долгое время компиляции. Обычно более минуты.

### Пример решения задачи A+B
```haxe
class Solution {
    public static function main() {
        var a = Std.parseInt(Sys.stdin().readLine());
        var b = Std.parseInt(Sys.stdin().readLine());
        Sys.stdout().writeString(Std.string(a+b));
    }
}
```
