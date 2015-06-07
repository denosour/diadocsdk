InvoiceCorrectionRequestInfo
============================

::

    message InvoiceCorrectionRequestInfo {
        required string ErrorMessage = 1;
        required Signer Signer = 2;
    }
        

| Структура данных InvoiceCorrectionRequestInfo представляет исходные
| данные для формирования уведомления об уточнении счета-фактуры при
| помощи метода
| `GenerateInvoiceCorrectionRequestXml <GenerateInvoiceCorrectionRequestXml>`__:

-  ErrorMessage - обязательный текст уведомления об уточнении.

-  | Signer - обязательная информация о подписанте уведомления в виде
   | структуры данных `Signer <Signer>`__.
