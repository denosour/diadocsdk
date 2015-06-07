GetDocflowBatchRequest
======================

.. code-block:: protobuf

   message GetDocflowBatchRequest
   {
       repeated GetDocflowRequest Requests = 1;
   }

Структура представляет список запросов, передаваемых методу :doc:`../http/GetDocflows`.

-  *Requests* - список запросов, по одному на документ.
