InboundInvoiceReceiptDocflow
============================

.. code-block:: protobuf

   message InboundInvoiceReceiptDocflow
   {
       optional bool IsFinished = 1;
       optional SignedAttachment ReceiptAttachment = 2;
       optional InvoiceConfirmationDocflow ConfirmationDocflow = 3;
   }

Структура представляет информацию о извещении о получении (ИоП) в рамках документооборота входящего счёта-фактуры.

-  *IsFinished* - признак того, что документооборот ИоП завершен. Значение true говорит о том, что ИоП имеет корректную подпись, и на него было получено подтверждение оператора с корректной подписью.
-  *ReceiptAttachment* - информация о файле ИоП.
-  *ConfirmationDocflow* - информация о подтверждении оператора на данное ИоП.
