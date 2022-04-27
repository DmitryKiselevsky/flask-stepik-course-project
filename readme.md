# This is the Stepik final project for Python Flask course

В задании было: 
* Проект должен находиться на git или в облачном хранилище, чтобы другие участники смогли его скачать и протестировать. 
* Виртуальную среду в папку не помещайте и лишние файлы уберите.
* К проекту должно быть небольшое пояснение: что он делает, как с ним работать и другие уместные примечания.
* Проект должен запускаться и не выдавать критических ошибок во время работы.
* Должен присутствовать базовый шаблон, примененный к другим страницам.
* Используйте html-теги, где это уместно. 
* Не нужно создавать профессиональную верстку  этот курс о серверной разработке.
* В проекте необходимо применить css. Для этого можете использовать готовые стили из интернета. Например Bootstrap 3. Насколько хорошо выглядит сайт оцениваться не будет. Задача в том, чтобы подключить какие либо используемые стили к тегам. Изображения тоже приветсвуются.
* В программе должно использоваться расширение Flask-WTF и присутствовать как миниму одна форма, наследуемая от класса FlaskForm.
* Необходимо применить как минимум 4 различных поля (SubmitField принимаем за одно из полей).
* Должно присутствовать как минимум 2 разных валидатора и их применение должно быть обосновано.
* В проекте должно находиться как минимум две функции представления: должен быть как статический, так и динамический маршруты.
* Одна из функций представления должна иметь возможность срабатывать на POST-запрос.
* Код в проекте цельный и логически завершенный.

## Prerequisites:

* docker is installed 

## Steps to run the app locally:

1. Build the container locally: `docker build -t my-flask-app .`
2. Run the container locally: `docker run -it --rm -p 80:80 --name my-flask-app -v $(pwd)/app:/app my-flask-app`
3. Access the app via your browser: [http://localhost](http://localhost)


## Testing:

`pytest` is ran from within the `/app` directory inside the container on build. The container build will not be successful if a test fails. 
For the test to be successful the build has to happen within Daimler's internal network and with the certificate in the `/app` directory.

The following screenshot helps to configure testing in pycharm:


<p align="center">
  <img src="img/pycharm-test-run-configuration.png" width=75%>
</p>

## Api Documentation:

<details><summary><b>Sample API request: </b><code>GET /api/&#60;string:variable&#62;</code></summary>
<p>

This an endpoint of the api.

**Endpoint**: `GET /api/<string:variable>`

**Return constraints:**

```json
{
    "name": String, 
    "data": {
        "age": Int,
        "height": String
    }
}
```

**Return example:**

```json
{
    "name": "jonnylangefeld", 
    "data": {
        "age": 27,
        "height": "6 ft 5.5"
}
```

</p>
</details>