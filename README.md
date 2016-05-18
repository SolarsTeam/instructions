<html>
  <head>
  </head>
  <body>
    <div class="container">
      <table>
        <thead>
          <tr>
            <th>Тэг</th>
            <th>Название / Описание</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td class="required">_Connection_</td>
            <td><span class="title">[Подключение](#)</span><br />
              Информация о подключении к базе данных. Имеет 4 обязательных внутренних тэга:
              <ul>
                <li>Server - сервер базы данных</li>
                <li>User - имя пользователя</li>
                <li>Password - пароль пользователя (в виде зашифрованной base64 строки)</li>
                <li>DataBase - имя базы данных (её alias или полный путь на диске)</li>
              </ul>
            </td>
          </tr>
          <tr class="even">
            <td class="required">_OurOrgnId_</td>
            <td><span class="title">[<a>Идентификатор "Нашей организации"</a>](#)</span><br />
            Идентификатор организации, которая помечена как "Наша"</td>
          </tr>
          <tr>
            <td class="required">_UserId_</td>
            <td><span class="title">[Идентификатор пользователя](#)</span><br />
            Идентификатор пользователя от имени котоого будет выполняться запуск системы</td>
          </tr>
          <tr class="even">
            <td class="required">_StoreGroupId_</td>
            <td><span class="title">[Группа складов](#)</span><br />
            Идентификатор группы складов</td>
          </tr>
          <tr>
            <td>_StoreForLoadedDocumentsId_</td>
            <td><span class="title">[Идентификатор склада для импорта накладных](#)</span><br />
            Идентификатор склада, в который будут оприходованы позиции из накладной</td>
          </tr>
          <tr class="even">
            <td>_ImageTextSource_</td>
            <td><span class="title">[Источник текста над картинкой](#)</span><br />
            Источник, из которого будет браться текст для вывода над картинкой товара в меню, задается как число и может иметь значения:
              <ul>
                <li>0 - Наименование товара</li>
                <li>1 - Полное наименование товара</li>
                <li>2 - Описание товара</li>
              </ul>
            </td>
          </tr>
          <tr>
            <td>_AllowSNForGoodsCategories_</td>
            <td><span class="title">[Разрешение серийных номеров для категорий товаров](#)</span><br />
            В тэге содержится набор тэгов "Id", которые указывают на категории товаров для которых можно задать штрих-код при работе с заказом</td>
          </tr>
          <tr class="even">
            <td>_IsPersonIdentification RequiredForDiscountOperations_</td>
            <td><span class="title">[Требование авторазиции для работы с ручными скидками](#)</span><br />
            Принимает значения:
              <ul>
                <li>true - необходима авторизация менеджера</li>
                <li>false - авторизация не требуется</li>
              </ul>
            </td>
          </tr>
          <tr>
            <td>_IsPersonIdentification RequiredForAPLOperations_</td>
            <td><span class="title">[Требование авторазиции для работы с альтернативными прайслистами](#)</span><br />
            Принимает значения:
              <ul>
                <li>true - необходима авторизация менеджера</li>
                <li>false - авторизация не требуется</li>
              </ul>
            </td>
          </tr>
          <tr class="even">
            <td>_GoodsCategories_</td>
            <td><span class="title">[Разрешение скидок для категорий товаров](#)</span><br />
            В тэге содержится набор тэгов "Id", которые указывают на категории товаров для которых можно задать ручную скидку</td>
          </tr>
          <tr>
            <td>_IsAllGoodsManualDiscountAllowed_</td>
            <td><span class="title">[Разрешения скидки для всех товаров в заказе](#)</span><br />
            Принимает значения:
              <ul>
                <li>true - в скидках появитс кнопка "Все товары в заказе"</li>
                <li>false - скидка возможно только по ранее выбранным категориям товара</li>
              </ul>
            </td>
          </tr>
          <tr class="even">
            <td>_ClientCardFormats_</td>
            <td><span class="title">[Форматы карточек клиентов](#)</span><br />
            В тэге содержится набор тэгов "Format", которые содержат форматы карточек клиентов, например: "636F6665000=52657374407274=NNNNNNNNNN", "211NNNNNNNNNN"</td>
          </tr>
          <tr>
            <td>_WeightBarcodeFormat_</td>
            <td><span class="title">[Формат весовых штрих-кодов](#)</span><br />
            !Занчение задается не внутри тэга, а в атрибуте "RegexFormat", и представляет собой регулярное выражение, которое имеет группы:
              <ul>
                <li>weight - вес</li>
                <li>id - идентификатор товара</li>
              </ul>
              Пример: "25(?&lt;weight&gt;\d{5})(?&lt;id&gt;\d{5})\d{1}"
            </td>
          </tr>
          <tr class="even">
            <td>_TaraGoodsGroups_</td>
            <td><span class="title">[Группы товаров определяющие тарру](#)</span><br />
            В тэге содержится набор тэгов "Id", которые и являются группами товаров</td>
          </tr>
          <tr>
            <td>_KeepOpenSelectGoods WindowForGoodsGroups_</td>
            <td><span class="title">[Группы товаров, при выборе из которых оставлять окно выбора позиций меню открытым](#)</span><br />
            В тэге содержится набор тэгов "Id", которые и являются группами товаров</td>
          </tr>
          <tr class="even">
            <td>_AlternativePriceLists_</td>
            <td><span class="title">[Доступные альтернативные прайслисты](#)</span><br />
            В тэге содержится набор тэгов "Price", внутри которых находятся тэги:
              <ul>
                <li>Id - идентификатор прайслиста (таблица PriceList)</li>
                <li>ShowCommentWindow - при выборе этого прайслиста будет отображаться окно для ввода примечания, значения: true - отображать, false - нет</li>
              </ul>
            </td>
          </tr>
          <tr>
            <td>_KassId_</td>
            <td><span class="title">[Идентификатор кассы](#)</span><br />
            Идентификатор кассы с которой будут производиться все операции</td>
          </tr>
          <tr class="even">
            <td>_KassInpOperations_</td>
            <td><span class="title">[Операции прихода в кассу](#)</span><br />
            В тэге содержится набор тэгов "Id", которые соответствуют идентификаторам операций из таблицы AcoprLst</td>
          </tr>
          <tr>
            <td>_KassOutOperations_</td>
            <td><span class="title">[Операции расхода из кассы](#)</span><br />
            В тэге содержится набор тэгов "Id", которые соответствуют идентификаторам операций из таблицы AcoprLst</td>
          </tr>
          <tr class="even">
            <td>_IsClosingKassDayActive_</td>
            <td><span class="title">[Закрытие кассового дня](#)</span><br />
            Активация закрытия кассового дня, принимает значения:
              <ul>
                <li>true - активировано</li>
                <li>false - не активировано</li>
              </ul>
              Также тэг может иметь атрибуты:
              <ul>
                <li>IsOrdersGroupingActive - активация группировки заказов (true - активировано, false - нет)</li>
                <li>KassInpOperation - идентификатор кассовой операции для прихода (таблица AcoprLst)</li>
                <li>KassInpOperationForExcess - идентификатор кассовой операции для излишка (таблица AcoprLst)</li>
                <li>KassOutOperationForShortage - идентификатор кассовой операции для недостачи (таблица AcoprLst)</li>
                <li>KassOutOperationForCollection - идентификатор кассовой операции для инкассации (таблица AcoprLst)</li>
                <li>UnremovableSumma - остаток в кассе на следующий день (если сумма не указана или равна нулю - этот остаток можно вводить/редактировать при закрытии кассового дня)</li>
                <li>ProcessCardClients - активация обработки заказов безналичного расчета (true - активно, false - нет)</li>
                <li>InpOperationForCards - безналичный расчет, идентификатор кассовой операции для прихода (таблица AcoprLst)</li>
                <li>OrganizationBankAccount - безналичный расчет, идентификатор расчетного счета (таблица OrgnBankAccn)</li>
                <li>CardClientComment - безналичный расчет, примечание для кассовой операции</li>
              </ul>
            </td>
          </tr>
          <tr>
            <td>_PaymentTypes_</td>
            <td><span class="title">[Типы оплат](#)</span><br />
            Активные типы оплат, может содержать следующие тэги:
              <ul>
                <li>PaymentTypeId - идентификатор типа оплаты (таблица CsDtKtHb)</li>
                <li>IsCash - оплата производится наличными (true - да, false - нет)</li>
                <li>IsCertificate - оплата производится сертификатом (true - да, false - нет)</li>
                <li>IsWriteOff - списание в производство, признак важен для расчета инвентаризационных данных (true - да, false - нет)</li>
                <li>ShowCardWindow - оплата производится наличными, (true - да, false - нет), имеется атрибут "IsInSilentMode", значениями которого могут быть:
                  <ul><li>true - окно ввода информации о карте и транзакции отображаться не будет</li><li>false - будет отображено окно для ввода номера карты и информации о транзакции</li></ul>
                 </li>
                <li>ShowAccountInfoWindow - оплата производится по расчетному счету, отображается соответствующее окно ввода информации (true - да, false - нет)</li>
                <li>ShowCommentWindow - отображать окно примечания (true - да, false - нет), имеет атрибут "ForceStandartCommentChoose", значениями которого могут быть:
                  <ul><li>true - не давать возможности провести заказ пока не выбрано стандартное примечание</li><li>false - выбор стандартного примечания необязателен</li></ul>  
                </li>
                <li>ShowDateWindow - отображать окно выбора даты</li>
                <li>IsGoodsCategoriesFilterActive - активация фильтра категорий товаров (true - запрещается проводить заказ, в котором находятся товары с категорием, которая не разрешена (см. ниже), false - проводить можно любые товары)</li>
                <li>AllowedGoodsCategories - разрешенные категории товаров для типа оплаты, работает при активированом тэге выше. В тэге содержится набор тэгов "Id", которые соответствуют идентификаторам категорий товаров</li>
                <li>TheoreticPaymentSumToOrderComment - подсчет теоретической суммы заказа, если есть необходимость (true - да, false - нет), в данный момент уже не используется</li>
                <li>DoNotPrintFiscalCheck - Не печатать чеков на фискальном регистраторе для этого типа оплат (true - да, false - нет)</li>
                <li>IsExcludedFromOrdersGrouping - Не учитывать заказы данного типа оплаты при групповой обработке во время закрытия кассового дня (true - да, false - нет)</li>
                <li>OrderToProvider - заказы будут переадресованы поставщику, внутренние тэги:
                  <ul>
                    <li>IsActive - активация возможности (true - да, false - нет)</li>
                    <li>ProviderOurOrganizationId - идентификатор "нашей организации" поставщика</li>
                    <li>ProviderStoreGroupId - идентификатор группы складов поставщика</li>
                    <li>ProviderPriceListId - идентификатор прайслиста, по ценам которого будут считаться позиции товаров</li>
                    <li>OrderNumberPrefix - префикс, который будет добавлен к номеру заказа(строковое значение)</li>
                    <li>IsClientRequired - обязательно необходимо выбрать клиента (true - да, false - нет)</li>
                    <li>AllowDiscountsForGoodsCategories - В тэге содержится набор тэгов "Id", которые соответствуют идентификаторам категорий товаров, для которых разрешены скидки, то есть это категории товаров,
                      для которых не разрешены ручные скидки, но в случае данного типа оплаты - скидка разрешается (или же скидка запрещена, если категория товара не задана, хотя для общих настроек программного обеспечения разрешена)
                    </li>
                  </ul>
                </li>
              </ul>
            </td>
          </tr>
          <tr class="even">
            <td>_RequirePersonIdentification ForKassOperations_</td>
            <td><span class="title">[Требовать персонализацию для кассовых операций](#)</span><br />
            Сканирование карточки клиента, номер которой введен в коле "Код" в личных делах персонала (true - возможность активирована, false - деактивирована)</td>
          </tr>
          <tr>
            <td>_UseBonusSystem_</td>
            <td><span class="title">[Исользовать бонусную систему](#)</span><br />
            Использование бонусных систем (true - возможность активна, false - деактивна), имеет атрибут "IsBonusMoneyUsingActive" - использование бонус денег (true - возможность активна, false - деактивна),
              обратите внимание, что для активации использования бонус-денег также необходимо активировать и использование бонусов вообще
            </td>
          </tr>
          <tr class="even">
            <td>_AllowCuttingForBonuses_</td>
            <td><span class="title">[Разрешить снятие бонусов](#)</span><br />
            В тэге содержится набор тэгов "Id", которые опеределяют идентификаторы бонусов (таблица DK_Bns), для которых разрешено снятие бонусов, конечно же при наличии полседних на карточке клиента</td>
          </tr>
          <tr>
            <td>_AllowExchangeForBonuses_</td>
            <td><span class="title">[Разрешить размен бонусов](#)</span><br />
            В тэге содержится набор тэгов "Id", которые опеределяют идентификаторы бонусов (таблица DK_Bns), для которых разрешен размен на другие бонусы, возможные варианты размена определяются по совпадению поля "Type"
              и курсу по полю "Val" (в случае бонус-денег курс оперделяется с помощью поля "CurrTypId") в таблице DK_Bns
            </td>
          </tr>
          <tr class="even">
            <td>_GiftCertificates_</td>
            <td><span class="title">[Подарочные сертивикаты](#)</span><br />
            В тэге содержится набор тэгов "Id", которые опеределяют идентификаторы товаров из меню, которые будут считаться подарочными сертификатами, стоит заметить, что эти товары исчезнут из меню (таблица Goods)</td>
          </tr>
          <tr>
            <td>_AllowInventoryOnlyAfterTime_</td>
            <td><span class="title">[Разрешать инвентаризацию только после определенного времени](#)</span><br />
            Строковое значение в формате "hh:mm"</td>
          </tr>
          <tr class="even">
            <td>_FiscalPrinterInfo_</td>
            <td><span class="title">[Информация о фискально принтере](#)</span><br />
            Внутри имеются тэги:
              <ul>
                <li>IsActive - активация возможности (true - активирована, false - деактивирована)</li>
                <li>OrderPaymentConfirm - подтверждать проведение заказа (true - появится диалоговое окно с просьбой подтвердить проведение заказа, false - подтверждение не требуется)</li>
                <li>Model - модель принтера, в данный момент не используется</li>
                <li>Port - COM-порт принтера, если он использует этот тип подключения</li>
                <li>Speed - скорость подключения COM-порта, если он использует этот тип подключения</li>
                <li>Host - URL фискального принтера, если используется подключение по HTTP</li>
                <li>Operator - информация об операторе, внутри имеются тэги: "Id" - идентификатор оператора (целочисленное значение), "Password" - пароль для оператора</li>
                <li>Protocol - протокол подключения к фискальному регистратору (HTTPHelpMicro, COMExellio)</li>
                <li>DefaultTaxGroup - налоговая группа по умолчанию (в случае необходимости)</li>
                <li>GoodsCategoryTaxGroups - привязка налоговых груб к категориям товаров, внутри может присутствовать набор тэгов "GoodsCategoryTaxGroup", в каждом из которых заданы еще 2 элемента-тэга:
                  <ul><li>"GoodsCategoryId" - идентификатор категории товаров</li><li>TaxGroup - идентификатор налоговой группы в терминале (целочисленное значение)</li></ul>
                </li>
            </td>
          </tr>
          <tr>
            <td>_Providers_</td>
            <td><span class="title">[Информация о поставщиках](#)</span><br />
            Внутри имеются тэги:
              <ul>
                <li>OKPO - идентификация поставщика производится по заданному ОКПО (таблица Orgn)</li>
                <li>Id - идентификация поставщика производится по заданному идентификатору (таблица Orgn)</li>
                <li>ConnectionString - строка подключения к базе данных поставщика (в виде зашифрованной base64 строки)</li>
              </ul>
            </td>
          </tr>
          <tr class="even">
            <td>_ProductionGoods_</td>
            <td><span class="title">[Производственные товары](#)</span><br />
            В тэге содержится набор тэгов "Id", которые опеределяют идентификаторы товаров, при выборе из меню которых програмное обеспечение попросит выбрать сырье для приготовления</td>
          </tr>
          <tr>
            <td>_CheckPrinterName_</td>
            <td><span class="title">[Наименование чекового принтера в системе](#)</span><br />
            Если задано значение - в окне оплат появится кнопка печати чека по заказу, печать будет производится на принтер с указанным именем</td>
          </tr>
          <tr class="even">
            <td>_IsClientSearchAllowed_</td>
            <td><span class="title">[Разрешение поиска клиентов по имени](#)</span><br />
            Значения: true - поиск разрешен, false - поиск запрещен</td>
          </tr>
          <tr>
            <td>_ClientSearchByPhone_</td>
            <td><span class="title">[Поиск клиентов по их телефону](#)</span><br />
            Информация для поиска и подтверждения клиентов по их телефону. Содержит атрибуты:
              <ul>
                <li>IsAllowed - активация (true - активировано, false - деактивировано)</li>
                <li>Provider - провайдер, в данный момент имеется поддержка только одного провайдера: "TurboSmsSoapProvider"</li>
                <li>UserName - имя пользователя (для авторизации у провайдера)</li>
                <li>Password - пароль, в виде зашифрованной base64 строки (для авторизации у провайдера)</li>
              </ul>
            </td>
          </tr>
          <tr class="even">
            <td>_PreventClientGroupAddEdit_</td>
            <td><span class="title">[Запрещение на редактирование групп организаций клиентов](#)</span><br />
            Содержит атрибуты:
              <ul>
                <li>IsActive - активация (true - запрет активен, false - запрет неактивен)</li>
                <li>DefaultGroupName - наименование группы организаций, в которую будет добавляться клиент при попытке редактирования его групп организаций</li>
              </ul>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </body>
</html>
