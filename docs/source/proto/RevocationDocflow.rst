RevocationDocflow
=================

.. code-block:: protobuf

   message RevocationDocflow
   {
       optional bool IsFinished = 1;
       optional SignedAttachment RevocationRequestAttachment = 2;
       optional RecipientSignatureDocflow RecipientSignatureDocflow = 3;
       optional RecipientSignatureRejectionDocflow RecipientSignatureRejectionDocflow = 4;
       optional string InitiatorBoxId = 5;
       optional bool IsRevocationAccepted = 6;
       optional bool IsRevocationRejected = 7;
   }

Структура представляет информацию об аннулировании документа.

-  *IsFinished* - признак того, что документооборот по аннулированию завершен, т.е. не требует дальнейших действий.
-  *RevocationRequestAttachment* - информация о файле предложения об аннулировании.
-  *RecipientSignatureDocflow* - информация об ответной подписи под предложением об аннулировании.
-  *RecipientSignatureRejectionDocflow* - информация об отказе в подписи предложения об аннулировании.
-  *InitiatorBoxId* - идентификатор ящика организации, которая инициировала аннулирование документа.
-  *IsRevocationAccepted* - признак того, что запрос на аннулирование был одобрен.
-  *IsRevocationRejected* - признак того, что запрос на аннулирование был отклонен.
