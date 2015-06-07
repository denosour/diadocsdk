TimeBasedFilter
===============

.. code-block:: protobuf

   message TimeBasedFilter
   {
       optional Timestamp FromTimestamp = 1;
       optional Timestamp ToTimestamp = 2;
       optional SortDirection SortDirection = 3 [default = Ascending];
   }

Структура представляет фильтр, который можно передать на :doc:`вход <GetDocflowEventsRequest>` методу :doc:`../http/GetDocflowEvents`. Фильтр позволяет ограничить по времени возвращаемые методом события и указать порядок их сортировки.

-  *FromTimestamp* - нижняя граница.
-  *ToTimestamp* - верхняя граница.
-  *SortDirection* - порядок сортировки событий.
