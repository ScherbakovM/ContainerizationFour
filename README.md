# ContainerizationFour

Контейнеризация семинар 4

### Создаём при помощи Dockerfile контейнер который будет автоматически исполняться при запуске

Для начала создадим папку куда поместим наш __py__ фаил 

`mkdir pyProject`  
`cd pyProject/` - сразу перейдём в неё  
`nano test.py` - создаём __py__  приложение   


![image](https://github.com/ScherbakovM/ContainerizationFour/assets/109952823/ff6e437a-45b6-4985-828a-ba20e219e189)

### далее создаём докер фаил 

`nano Dockerfile` 

Заполняем фаил инструкциями для докера 


`FROM python:3`    
`COPY test.py ./app/ `  
`WORKDIR /app/`    
`CMD ["python", "test.py"]`   

![image](https://github.com/ScherbakovM/ContainerizationFour/assets/109952823/0645f248-10bd-403e-9c88-d31d99b0ecc0)

Сохраняем и запускаем  сборку 


`docker build -t testbuild .` - testbuild название сборки можно указать любое \ __.__ точка указывает на то что Dockerfile находится в этой же директории 


![image](https://github.com/ScherbakovM/ContainerizationFour/assets/109952823/093c2722-29f7-4ec3-989c-a9b36b45c68e)

