# lab_cicd №11
1. Убедилась, что публичный ключ ssh добавлен на профиль в гите

   <img width="1280" height="319" alt="image" src="https://github.com/user-attachments/assets/fff0e7ee-e8a7-4014-b402-aff54bf99512" />

2. Создаем репо

   <img width="940" height="834" alt="image" src="https://github.com/user-attachments/assets/567164e9-49c1-488f-8e9c-ad44225d1121" />

3. Клонируем репозиторий

  <img width="782" height="202" alt="image" src="https://github.com/user-attachments/assets/3631afa3-b66a-4379-a829-ae59eae472cd" />

4. Будущая структура каталогов

   <img width="444" height="242" alt="image" src="https://github.com/user-attachments/assets/ecf94949-2858-49f3-9bff-eb5ab62cbe8a" />

5. Создаем приложение server/application.py, в котором есть класс для демонстрации работы тестов и веб-сервер, отвечающий на любой запрос

      <img width="662" height="658" alt="image" src="https://github.com/user-attachments/assets/c335e757-0619-4f1c-8fa3-e99a173a44dc" />

6. Юнит-тесты server/test-application.py, в которых используется библиотека pytest, импортируется приложение, проверяются наши функции из server/application.py

   <img width="626" height="306" alt="image" src="https://github.com/user-attachments/assets/15c9a320-ed5f-48e7-bbd0-01de1237426f" />

7. Создаем файл с зависимостями для самих тестов requirements.txt

   <img width="585" height="212" alt="image" src="https://github.com/user-attachments/assets/c5af2b5c-5828-47c2-aea6-ff13c6810279" />

8. Создаем файл для сборки образа dockerfile

   <img width="664" height="348" alt="image" src="https://github.com/user-attachments/assets/08d15db1-5e8f-4cd1-a18c-d6c43b835fd2" />

9. Пушим в гитхаб (в ветку main - основная)

   <img width="848" height="439" alt="image" src="https://github.com/user-attachments/assets/3f96da22-c6f4-4eeb-82c7-3f054176ee98" />

10. Переходим в отдельную ветку dev

    <img width="862" height="313" alt="image" src="https://github.com/user-attachments/assets/d788eb2a-52a5-4e34-a898-2af9f7f1f285" />

11. Защищаем ветку main от прямых изменений, только merge-requests

    <img width="1254" height="893" alt="image" src="https://github.com/user-attachments/assets/d7c686a2-df0b-4a47-9336-ca152cd54fba" />
    <img width="988" height="836" alt="image" src="https://github.com/user-attachments/assets/68de8106-193c-4cc8-b786-6212ed9e751c" />

12. Добавляем сценарии

    <img width="1280" height="810" alt="image" src="https://github.com/user-attachments/assets/a450aafe-3031-4510-9814-921005be1b33" />

13. Создаем базовый сценарий .github/workflows/devops_course_pipeline.yml и пушим в dev изменения

    <img width="680" height="433" alt="image" src="https://github.com/user-attachments/assets/67077fba-c324-4d3c-ba19-f009ddfa0b07" />
    <img width="856" height="394" alt="image" src="https://github.com/user-attachments/assets/d6c090dd-d300-4643-8f8a-92b446352845" />

14. Проверяем, как отработал

    <img width="1280" height="747" alt="image" src="https://github.com/user-attachments/assets/2fdde296-3c4e-4977-a1a5-b186059b1de9" />

15. Теперь создаем "боевой" сценарий .github/workflows/cicd.yml и пушим его

    <img width="1005" height="716" alt="image" src="https://github.com/user-attachments/assets/884a84b7-2032-4ece-845e-b297782e15e2" />
    <img width="877" height="373" alt="image" src="https://github.com/user-attachments/assets/c32918bf-4adf-4ee1-81ab-0d4292efa95a" />

16. Успешно отработал

    <img width="1280" height="639" alt="image" src="https://github.com/user-attachments/assets/782104c9-6859-4574-b275-a57a24432995" />

17. Далее необходимо создать k8s-манифест devops-psu для куберизирования нашего приложения

    <img width="589" height="652" alt="image" src="https://github.com/user-attachments/assets/5208c1c8-0009-4b8e-988b-e1564f475189" />

18. Запускаем minikubе, применяем манифесты и проверяем поды, если с ними все отлично, пушим в гит

    <img width="807" height="315" alt="image" src="https://github.com/user-attachments/assets/a7cf2ba5-b5d1-4b46-92e2-5cb7c182f6af" />
    <img width="875" height="401" alt="image" src="https://github.com/user-attachments/assets/7480234e-3c7c-4d69-8288-715bd01d758d" />

19. Проверка на гитхабе

     <img width="1280" height="407" alt="image" src="https://github.com/user-attachments/assets/29589609-8086-45b6-98b4-f5400659c513" />

20. Регистрируемся через гит, добавляем публикацию докер-образа приложения в хранилище, создаем токены для доступа 

    <img width="1280" height="615" alt="image" src="https://github.com/user-attachments/assets/b54b808e-5d90-4fec-a916-e5d82d29db5a" />

21. Также логинимся в ВМ

    <img width="875" height="357" alt="image" src="https://github.com/user-attachments/assets/fd1b759b-c68c-42bf-af60-929c14f2bc54" />

22. Добавляем Action Secrets на гит

    <img width="1280" height="388" alt="image" src="https://github.com/user-attachments/assets/cae263c8-fa77-42b6-9553-dfe800625aec" />
    <img width="1280" height="519" alt="image" src="https://github.com/user-attachments/assets/583ecd5a-f921-499b-b6d3-7c9ea296f84b" />
    <img width="1137" height="370" alt="image" src="https://github.com/user-attachments/assets/9f822c2d-32f6-4fa7-aa1b-2e5de9898e6a" />

23. Создаем пайплайн .github/workflows/release.yml для сборки и публикации образа в докер

    <img width="944" height="677" alt="image" src="https://github.com/user-attachments/assets/801d7391-d72a-4f40-bc21-3ce7781b81a5" />

24. Делаем коммит новых файлов в репозиторий, создаем pull-request и выполняем merge в main

    <img width="1163" height="375" alt="image" src="https://github.com/user-attachments/assets/bab2b782-e868-4b31-8124-98904b6a939a" />
    <img width="1280" height="397" alt="image" src="https://github.com/user-attachments/assets/498851f7-413d-48e2-8c73-b0ce5ebe59ae" />

25. А дальше пошло веселье... Почему-то докер со мной не хотел вести диалог, поэтому пайплайн подкидывал образы в сам докерхаб, а отображать отказывался. Я уже и так и этак с ним пыталась разобраться и ничего, хотя производили с одногруппницей аналогичные действия, у нее все корректно отображалось в тэгах

    <img width="1280" height="460" alt="image" src="https://github.com/user-attachments/assets/e85f37c4-a2cf-4897-962d-1f62ce56146f" />

26. Переходим к шупалцам многострадальным (как были в шутку прозваны после миллионной попытки), то есть к ArgoCD

    а) Создаем отдельное пространство имен (скриншот потерян...) и скачиваем, устанавливаем все из манифеста

    <img width="874" height="384" alt="image" src="https://github.com/user-attachments/assets/60db6c9f-1654-4c02-9c41-7dd7196e8a37" />

    б) Ждем пока модули будут готовы

    <img width="816" height="199" alt="image" src="https://github.com/user-attachments/assets/8e4e4df5-0780-469b-9e11-24e6a368e8e2" />

    в) Вытаскиваем админский пароль

    <img width="826" height="80" alt="image" src="https://github.com/user-attachments/assets/61b6d7ca-3195-48dc-bef0-c34c77c9fc06" />

    г) Пробрасываем api-сервис

      <img width="851" height="87" alt="image" src="https://github.com/user-attachments/assets/82f475c4-62cf-48c6-b549-4268ec0c7c59" />
      <img width="835" height="96" alt="image" src="https://github.com/user-attachments/assets/e6f6a5ff-dfb0-4d01-afee-792a8ff7e11f" />

27. Шупалца захвачены с помощью украденного из шага 26-в пароля и логина admin

    <img width="1171" height="567" alt="image" src="https://github.com/user-attachments/assets/857fac31-3e3f-4e97-be88-ad0936668ed5" />

28. Подключаем к ArgoCD наш гит с использованием приватного ключа

     <img width="621" height="250" alt="image" src="https://github.com/user-attachments/assets/5cb07cc7-8131-4f90-afd2-497b59fa3d1c" />
      <img width="937" height="327" alt="image" src="https://github.com/user-attachments/assets/fc64f22a-21a4-4abb-9be8-3a122e853637" />

29. Выбираем репозиторий, указываем ветку для отслеживания и путь к манифестам (произошел тупняк и все это в дальнейшем окажется в ветке dev, а не release, как должно быть, но прошу понять и простить, ибо с Argo было больше всего мучений и голова думала не в нужном направлении)

    <img width="840" height="538" alt="image" src="https://github.com/user-attachments/assets/94f4ca22-dd14-42a1-b429-16300080132a" />

30. Указываем реквизиты кластера k8s и пространство имен

    <img width="560" height="292" alt="image" src="https://github.com/user-attachments/assets/a4170b11-f7bc-42be-bd22-d1d5e7ac0c43" />

31. Успех! Приложение взято на карандаш ArgoCD

    <img width="592" height="548" alt="image" src="https://github.com/user-attachments/assets/449afa8a-2456-4216-86a8-95c2dac1eb4d" />
    <img width="1039" height="353" alt="image" src="https://github.com/user-attachments/assets/8e74fa1b-2f8f-4ce9-a5e7-2cb4d86a2a89" />

32. Создаем индексный файл и правим докерфайл, пушим в dev

    <img width="690" height="327" alt="image" src="https://github.com/user-attachments/assets/91c2b15d-8393-47ea-a461-573cabe5e948" />

33. Делаем pull-request и merge после успешных тестов

    <img width="1280" height="627" alt="image" src="https://github.com/user-attachments/assets/5445e153-a716-4c1c-81f5-a816e6ff801a" />

    Скрин из ArgoCD забыла сделать, но по факту он аналогичен тому, что в пункте 31, раз я указала ветку dev

33. А тем временем докер на меня окончательно обиделся

    <img width="1280" height="465" alt="image" src="https://github.com/user-attachments/assets/412cd701-d357-454d-a535-0e8b78773603" />
    <img width="1280" height="700" alt="image" src="https://github.com/user-attachments/assets/e004edf8-d333-40d0-bbe4-4d04f80ca999" />

    
