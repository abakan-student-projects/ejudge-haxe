                                        Инструкция установки ЯП Haxe

    1. Перейти в каталог /home/judges/compile/conf и открываем файл compile.cfg.
    2. В конец файла добавить следующий код:
        [language]
        id = 73
        short_name = «haxe»
        long_name = «Haxe»
        src_sfx = «.hx»
        cmd = «haxe»
        arch = «linux-shared»
    3. Перейти в каталог /home/judges/compile/scripts. Создать файлы haxe и haxe-version и в данные файлы вставить код из исходных.
    4. В терминале запустить программу ejudge-configure-compilers и проверить наличие ЯП Haxe.
    5. Перейти в каталог /home/judges/000001/conf и открыть файл serve.cfg. В него записать строку compile_real_time_limit = 300.
    6. Перейти в serve-control и зайти под администратором. (https://localhost/cgi-bin/serve-control)
    7. В таблице напротив test contest перейти settings/language settings. В списке найти ЯП Haxe и напротив него нажать activate.
