RecipientSignatureDocflow
=========================

.. code-block:: protobuf

   message RecipientSignatureDocflow
   {
       optional bool IsFinished = 1;
       optional Signature RecipientSignature = 2;
       optional Timestamp DeliveryTimestamp = 3;
   }

Структура представляет информацию об ответной подписи, поставленной контрагентом под документом.

-  *IsFinished* - признак того, что подпись проверена и доставлена контрагенту.
-  *RecipientSignature* - подробная информация о содержимом подписи, результатах его проверки, и пр.
-  *DeliveryTimestamp* - метка времени доставки подписи контрагенту.
