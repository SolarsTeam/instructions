<html>
  <head>
    <style>
    * {
      box-sizing: border-box;
    }
      table, body {
        font-family: "Helvetica Neue",Helvetica,Arial,sans-serif; 
        font-size: 16px;
      }
      th {
        text-align: left;
      }
      @media (min-width:768px){.container{width:750px}}@media (min-width:992px){.container{width:970px}}@media (min-width:1200px){.container{width:1170px}}
      .container {
        padding-right: 15px;
        padding-left: 15px;
        margin-right: auto;
        margin-left: auto;
      }
      table {
        border-spacing: 0;
        border-collapse: collapse;
      }
      tr.even {
        background-color: #F7F7F7;
      }
      .required {
        color: red;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <table>
        <colgroup>
          <col width="22%" />
          <col width="17%" />
          <col width="59%" />
        </colgroup>
        <thead>
          <tr>
            <th>Тэг</th>
            <th>Название</th>
            <th>Описание</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td class="required">Connection</td>
            <td>Подключение</td>
            <td>
              Информация о подключении к базе данных. Имеет 4 обязательных внутренних тэга:
              <ol>
                <li>Server - сервер базы данных</li>
                <li>User - имя пользователя</li>
                <li>Password - пароль пользователя (в виде зашифрованной base64 строки)</li>
                <li>DataBase - имя базы данных (её alias или полный путь на диске)</li>
              </ol>
            </td>
          </tr>
          <tr class="even">
            <td class="required">OurOrgnId</td>
            <td>Идентификатор "Нашей организации"</td>
            <td>Идентификатор организации, которая помечена как "Наша"</td>
          </tr>
          <tr>
            <td class="required">UserId</td>
            <td>Идентификатор пользователя</td>
            <td>Идентификатор пользователя от имени котоого будет выполняться запуск системы</td>
          </tr>
          <tr class="even">
            <td class="required">StoreGroupId</td>
            <td>Группа складов</td>
            <td>Идентификатор группы складов</td>
          </tr>
          <tr>
            <td>StoreForLoadedDocumentsId</td>
            <td>Идентификатор склада для импорта накладных</td>
            <td>Идентификатор склада, в который будут оприходованы позиции из накладной</td>
          </tr>
          <tr class="even">
            <td>ImageTextSource</td>
            <td>Источник текста над картинкой</td>
            <td>Источник, из которого будет браться текст для вывода над картинкой товара в меню, задается как число и может иметь значения:
              <ol>
                <li>0 - Наименование товара</li>
                <li>1 - Полное наименование твоара</li>
                <li>2 - Описание товара</li>
              </ol>
            </td>
          </tr>
          <tr>
            <td>AllowSNForGoodsCategories</td>
            <td>Разрешение серийных номеров для категорий товаров</td>
            <td>В тэге содержится набор тэгов "Id", которые указывают на категории товаров для которых можно задать штрих-код при работе с заказом</td>
          </tr>
          <tr class="even">
            <td>IsPersonIdentificationRequiredForDiscountOperations</td>
            <td>Требование авторазиции для работы с ручными скидками</td>
            <td>Принимает значения:
              <ol>
                <li>true - необходима авторизация менеджера</li>
                <li>false - авторизация не требуется</li>
              </ol>
            </td>
          </tr>
          <tr>
            <td>IsPersonIdentificationRequiredForAPLOperations</td>
            <td>Требование авторазиции для работы с альтернативными прайслистами</td>
            <td>Принимает значения:
              <ol>
                <li>true - необходима авторизация менеджера</li>
                <li>false - авторизация не требуется</li>
              </ol>
            </td>
          </tr>
          <tr class="even">
            <td>GoodsCategories</td>
            <td>Разрешение скидок для категорий товаров</td>
            <td>В тэге содержится набор тэгов "Id", которые указывают на категории товаров для которых можно задать ручную скидку</td>
          </tr>
          <tr>
            <td>IsAllGoodsManualDiscountAllowed</td>
            <td>Разрешения скидки для всех товаров в заказе</td>
            <td>Принимает значения:
              <ol>
                <li>true - в скидках появитс кнопка "Все товары в заказе"</li>
                <li>false - скидка возможно только по ранее выбранным категориям товара</li>
              </ol>
            </td>
          </tr>
          <tr class="even">
            <td>ClientCardFormats</td>
            <td>Форматы карточек клиентов</td>
            <td>В тэге содержится набор тэгов "Format", которые содержат форматы карточек клиентов, например: "636F6665000=52657374407274=NNNNNNNNNN", "211NNNNNNNNNN"</td>
          </tr>
          <tr>
            <td>WeightBarcodeRegexFormat</td>
            <td>Формат весовых штрих-кодов</td>
            <td>!Занчение задается не внутри тэга, а в атрибуте "RegexFormat", и представляет собой регулярное выражение, которое имеет группы:
              <ol>
                <li>weight - вес</li>
                <li>id - идентификатор товара</li>
              </ol>
              Пример: "25(?&lt;weight&gt;\d{5})(?&lt;id&gt;\d{5})\d{1}"
            </td>
          </tr>
          <tr class="even">
            <td>TaraGoodsGroups</td>
            <td>Группы товаров определяющие тарру</td>
            <td>В тэге содержится набор тэгов "Id", которые и являются группами товаров</td>
          </tr>
          <tr>
            <td>KeepOpenSelectGoodsWindowForGoodsGroups</td>
            <td>Группы товаров, при выборе из которых оставлять окно выбора позиций меню открытым</td>
            <td>В тэге содержится набор тэгов "Id", которые и являются группами товаров</td>
          </tr>
          <tr class="even">
            <td>AlternativePriceLists</td>
            <td>Доступные альтернативные прайслисты</td>
            <td>В тэге содержится набор тэгов "Price", внутри каждый из них</td>
          </tr>
          <tr>
            <td></td>
            <td></td>
            <td></td>
          </tr>
        </tbody>
      </table>
    </div>
  </body>
</html>
