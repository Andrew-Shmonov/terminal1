### terminal1

1. Ознакомьтесь с графическим интерфейсом VirtualBox, посмотрите как выглядит виртуальная машина, которую создал для вас Vagrant, какие аппаратные ресурсы ей выделены. Какие ресурсы выделены по-умолчанию?  
По умолчанию выделяет 1Гб ОЗУ, 2 ЦПУ, 64Гб дискового  

2. Ознакомьтесь с возможностями конфигурации VirtualBox через Vagrantfile: документация. Как добавить оперативной памяти или ресурсов процессора виртуальной машине?  
Доработка вагрантфайла записями вида:  
`config.vm.provider "virtualbox" do |v|  
  v.memory = 1024  
  v.cpus = 2  
end`  

3. какой переменной можно задать длину журнала history, и на какой строчке manual это описывается?  
HISTFILESIZE (586 str)  

4. что делает директива ignoreboth в bash?  
есть две директивы: одна позволяет убирать дубли из истории, вторая - все, что начинается с пробела и чтобы убрать и то, и то используется ignoreboth  

5. В каких сценариях использования применимы скобки {} и на какой строчке man bash это описано?  
Для выделения резервированных переменных (133 стр), описания массивов.

6. Основываясь на предыдущем вопросе, как создать однократным вызовом touch 100000 файлов? А получилось ли создать 300000?  
touch file{1..100000}  
Нет, слишком много аргументов.

7. В man bash поищите по `/\[\[`. Что делает конструкция `[[ -d /tmp ]]`
Если есть директория `/tmp` вернёт true, если нет - false

8. Основываясь на знаниях о просмотре текущих (например, PATH) и установке новых переменных; командах, которые мы рассматривали, добейтесь в выводе type -a bash в виртуальной машине наличия первым пунктом в списке:
mkdir /tmp/my_dir
cp /bin/bash /tmp/my_dir/
PATH=$PATH:/tmp/my_dir/

9. Чем отличается планирование команд с помощью batch и at?
`at` планирует задачу на конкретное время, на один раз. а `batch` выполняется, когда позволяет уровень загрузки системы, то есть в неизвестное время.
















