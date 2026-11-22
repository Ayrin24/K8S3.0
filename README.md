Задание 1.

<img width="669" height="823" alt="image" src="https://github.com/user-attachments/assets/7b085d3d-0a79-49f0-ad2e-8c091fb4c3dc" />

<img width="753" height="158" alt="image" src="https://github.com/user-attachments/assets/9bb8fd4b-d206-4003-88c8-994f0a8e4fe1" />

Задание 2.

<img width="881" height="823" alt="image" src="https://github.com/user-attachments/assets/cf3c3e77-38fa-48f6-8aa7-498ae13e0eda" />

После удаления Deployment и PVC PV переходит в статус Released, а не Available. Причина в политике Retain: Kubernetes не очищает том и не отдаёт его другому claim автоматически. В PV ещё остаётся claimRef на удалённый PVC, поэтому админ должен сам почистить данные и ссылку.
После удаления PV файл на диске ноды остаётся. PV это только объект API, описывающий том. Для hostPath с Retain Kubernetes не удаляет данные на хосте, а удаляется только метаданные об объекте. Каталог придётся убрать руками.

Задание 3.

<img width="1129" height="343" alt="image" src="https://github.com/user-attachments/assets/9425eb07-5e39-4868-9250-164f12b238ad" />


