DocumentWithDocflow
===================

.. code-block:: protobuf

   message DocumentWithDocflow
   {
       optional DocumentId DocumentId = 1;
       optional string LastEventId = 2;
       optional Timestamp LastEventTimestamp = 3;
       optional DocumentInfo DocumentInfo = 4;
       optional Docflow Docflow = 5;
       repeated DocumentId InitialDocumentIds = 6;
       repeated DocumentId SubordinateDocumentIds = 7;
       repeated ForwardDocumentEvent ForwardDocumentEvents = 8;
   }

Структура представляет информацию о документе (метаданные и состояние документооборота), возвращаемую методами :doc:`../http/GetDocflows`, :doc:`../http/GetDocflowsByPacketId`, :doc:`../http/SearchDocflows`.

-  *DocumentId* - идентификатор документа.
-  *LastEventId* - идентификатор последнего события по документу, которое было учтено при формировании данной структуры.
-  *LastEventTimestamp* - метка времени последнего события.
-  *DocumentInfo* - метаданные документа.
-  *Docflow* - информация о состоянии документооборота.
-  *InitialDocumentIds* - идентификаторы документов, на которые ссылается данный документ.
-  *SubordinateDocumentIds* - идентификаторы документов, которые ссылаются на данный документ.
-  *ForwardDocumentEvents* - список событий по перемещению данного документа.
