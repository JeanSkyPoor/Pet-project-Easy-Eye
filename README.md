# Pet-project-Easy-Eye

  Мой пет-проект направленный на автоматизацию сбора данных с экрана монитора. 

  Скачать Easy Eye.exe можно справа в поле Releases, выбрав свою систему

  Шаг 1: Необходимо установить tesseract по указанному пути C:\Program Files\Tesseract-OCR. Ссылка на скачивание https://github.com/UB-Mannheim/tesseract/wiki. Выберите под вашу систему. 

  Шаг 2: Узнаем координаты интересующей области. Нужно два угла прямоугольника - левый верхний и правый нижний. Сделать это можно в Paint'e, наводите мышь на левый верхний угол нужной области и слева внизу Paint'a будет пара цифр. После чего переводите мышь на правый нижний угол прямоугольника, узнаем координаты. В итоге у вас должно быть что-то похожее на 306 904, 505 838. Область прямоугольника должна быть немного больше области цифр. (нужные углы обозначены красным цветом)
  
  ![image](https://user-images.githubusercontent.com/69383370/133995214-cfa9ba52-637b-4b76-9998-3a70a60836ae.png)


  Шаг 3: Открываем Easy Eye.exe и вбиваем полученные координаты в соответствующие поля. После чего нажимаем кнопку Тест и ждем 5 секунд. После ожидания откроется фрагмент вырезанного изображения и в поле "Результаты теста" вы увидите результат "считывания". Если надо будет удалить лишние символы, измените параметры в поле "Удаление лишних символов", дефолтное значения 0, 0.

  Шаг 4: Когда все настроено и результат корректен, для записи необходимо ввести имя будущего файла, ввести частоту записей (минимум 1 секунда, принимает только целые числа) и нажать кнопку старт. Ввиду того, что программа делает принтскрин рабочего стола, ваше приложение должно быть открыто, чтобы программа смогла считать результат. 

  Шаг 5: Если это первый запуск или вы перенесли .exe файл в другое место, локально на месте приложения создастся папка Records, куда в дальнейшем будут сохраняться файлы в CSV формате (разделитель ;). Если вы переместите приложение на другой путь, то и там будет создана новая папка. Во время сбора снизу кнопки Стоп будет информация того, сколько записей будет сохранено. Запись осуществляется только после нажатия кнопки Стоп. Это означает, если программа зависнет во время работы, то файл не будет сохранен.

  Шаг 6: чтобы завершить процесс сбора данных нажмите кнопку Стоп. После того как цикл записи будет завершен (зависит от указанного времени в поле "Частота записей (сек)", может потребоваться время пока процесс sleep завершится), процесс завершится и в папке Records появится файл с именем, которое вы указали.

  Warning: постарался словить основные ошибки в работе приложения, но вряд ли учел всевозможные ошибки. Поэтому если вы вводите странные данные или делаете что-то из ряда вон выходящее, есть шанс, что приложение крашнется и закроется.

  Интерфейс самой программы не должен вызвать особых проблем.

  Если у вас будут какие-то вопросы, можете написать мне на почту katovato2705@gmail.com
  
  FAQ: Программа не распознает данные. Решение: попробуйте сделать область прямоугольника немного больше, чем было до этого. В некоторых случаях это помогает.
  
   Работает ли программа с текстом? Да, английский язык программа способна распознавать. Остальные языки (в том числе русский) не проверял. 
   
   Увеличиваю область прямоугольника, но программа все равно работает неккоректно. Решение: его нет. Возможно, размер шрифта слишком маленький, чтобы программа смогла его распознать. Если есть возможность, увеличьте размер шрифта. 
   
   Использую большой размер шрифта, но программа его не считывает. Решение: возможно, у вас установлен какой-то экзотический шрифт. Попробуйте поставить более стандартные шрифты аля Times New Roman или Arial. 
  
![interface](https://user-images.githubusercontent.com/69383370/134298761-cd3d1ded-15b8-4696-a141-c44b0533c565.png)


