DocumentInfo
============

.. code-block:: protobuf

   message DocumentInfo
   {
       optional DocumentType DocumentType = 1 [default = UnknownDocumentType];
       optional DocumentDirection DocumentDirection = 2 [default = UnknownDocumentDirection];
       optional bool IsTest = 3;
       optional string CustomDocumentId = 4;
       optional string FromDepartmentId = 5;
       optional string ToDepartmentId = 6;
       optional string CounteragentBoxId = 7;
       optional DocumentDateAndNumber DocumentDateAndNumber = 8;
       optional BasicDocumentInfo BasicDocumentInfo = 9;
       optional InvoiceDocumentInfo InvoiceInfo = 10;
       optional InvoiceCorrectionDocumentInfo InvoiceCorrectionInfo = 11;
       optional PriceListDocumentInfo PriceListInfo = 12;
       optional ContractDocumentInfo ContractInfo = 13;
   }

Структура представляет данные документа, которые не меняются в течение его жизненного цикла (метаданные). Как часть структуры :doc:`DocumentWithDocflow`, возвращается методами :doc:`../http/GetDocflows`, :doc:`../http/GetDocflowsByPacketId`, :doc:`../http/SearchDocflows`.

-  *DocumentType* - типа документа.
-  *DocumentDirection* - направление документа относительно данного ящика (например, исходящий).
-  *IsTest* - признак того, что документ тестовый.
-  *CustomDocumentId* - произвольный идентификатор документа, присвоенный ему во время отправки интеграционным решением.
-  *FromDepartmentId* - идентификатор подразделения-отправителя документа.
-  *ToDepartmentId* - идентификатор подразделения-получателя документа.
-  *CounteragentBoxId* - идентификатор ящика контрагента.
-  *DocumentDateAndNumber* - дата и номер документа.
-  Поля, содержащие метаданные документа. В зависимости от типа документа заполняется только одно из полей:

   -  *BasicDocumentInfo* - для документов XmlTorg12, XmlAcceptanceCertificate, Torg12, AcceptanceCertificate, ProformaInvoice, Torg13.
   -  *InvoiceInfo* - для документов Invoice или InvoiceRevision.
   -  *InvoiceCorrectionInfo* - для документов InvoiceCorrection или InvoiceCorrectionRevision.
   -  *PriceListInfo* - для документов PriceList.
   -  *ContractInfo* - для документов Contract.
