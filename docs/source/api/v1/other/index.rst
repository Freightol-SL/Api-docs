==================
Other endpoints
==================

.. toctree::
   :glob:
   :maxdepth: 2

   aerial/index
   courier/index
   maritime/index
   pickup-time/index
   
=============================
Shipment Tracking Enable
=============================

Shipment IsActiveTracking
----------------
Receives the shipment id and the status (true, false), and returns an HTTP response code.

**Example request**:
    
.. http:get:: /v1/shipment/{shipmentId}/status/enable

.. tabs::
    .. code-tab:: bash

        $ curl \
            -H "Content-Type: application/json" \
            -H "Authorization: Bearer <token>" \
            https://<env>.freightol.com/v1/shipment/{shipmentId}/status/enable

=============  =======  =================================================
Name           Type     Description
=============  =======  =================================================
ShipmentId     Guid     Shipment identifier
status         bool     0-Disabled / 1-Enabled
=============  =======  =================================================

**Example response**:

200	
Success

400	
Bad Request

401	
Unauthorized

403	
Forbidden
