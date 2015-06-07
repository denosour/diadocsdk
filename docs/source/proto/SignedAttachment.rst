SignedAttachment
================

.. code-block:: protobuf

   message SignedAttachment
   {
       optional Attachment Attachment = 1;
       optional Signature Signature = 2;
       optional Entity Comment = 3;
   }

Структура представляет базовую информацию о документе и его подписи.

-  *Attachment* - данные файла документа.
-  *Signature* - подпись под файлом.
-  *Comment* - комментарий к файлу.
