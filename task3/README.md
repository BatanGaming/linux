## 1. Третье поле в файле /etc/passwd содержит?
UID - идентификатор пользователя.
## 2. Что такое Теневые файлы паролей?
Файлы, в которых хранится информация в защищённом виде (доступны только для root пользователя)
	`/etc/shadow` - информация о пользователях
	`/etc/gshadow` - информация о группах
## 3. Какой пользователь имеет UID и GID равными 0?
root.
## 4. Как сменить активный идентификатор группы?
	newgrp
## 5 Как сменить пароль пользователя?
	passwd user
## 6. Как установить время истечения пароля пользователя?
	chage -d date
## 7. Изменить права на файл в символьном и абсолютном режиме
 - r w x r- - r - -<br>
`chmod u+rwx,go+r-wx <file_name>`<br>
`chmod 744 <file_name>`
 - r - - - w- - - x<br>
`chmod u=r,g=w,o=x <file_name>`<br>
`chmod 421 <file_name>`
 - \- - x - w - r - -<br>
`chmod u=x,g=w,o=r <file_name>`<br>
`chmod 124 <file_name>`
## 8. Что означает строка -wx-w---- ?
 - Владелец имеет права на запись и исполнение;
 - Пользователи группы имеют право на запись;
 - Остальные пользователи не имеют никаких прав на действия с данным файлом.
## 9. Что означает строка прав доступа r--r-xrwx для каталога?
 - Владелец имеет право на чтение (получение списка файлов);
 - Пользователи группы имеют право на чтение и исполнение (получение списка файлов, изменение текущей рабочей директории на эту, получение доступа к файлам);
 - Остальные пользователи имеют право на любое действие с данным каталогом (получение списка файлов, создание новых файлов/директорий, изменение текущей рабочей директории на эту, получение доступа к файлам)

## 10. Какой командой установить права -wx--x-w- на файл?  
`chmod 312 <file_name>`
## 11. Какой командой в абсолютном режиме установить права rw---xr-- на файл?
`chmod 614 <file_name>`
## 12. Какая команда в абсолютном режиме разрешит полный доступ к файлу для всех?
`chmod 777 <file_name>`
## 13. Какая команда установит такие права на каталог, что удалять файлы из него смогут только владельцы этих файлов?
`chmod +t <file_name>`