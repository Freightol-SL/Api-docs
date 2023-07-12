=====================
Tariff
=====================

Request to retrieve the tariff info matching the filters.

TariffReport
--------------------------

**Example request**:
    
.. http:get:: /v1/tariff


.. tabs::
    .. code-tab:: bash

        $ curl -X 'POST' \
            'https://<env>.freightol.com/v1/tariff' \
            -H "Content-Type: application/json" \
            -H "Authorization: Bearer <token>" \
            -d @body.json

**Example request Http**:

.. sourcecode:: json
    {
        "tariffName": null,
        "contractNumber": "CL131839T",
        "delegationId": null,
        "fromDate": "2024-09-01T00:00:00.000Z",
        "toDate": "2024-09-02T00:00:00.000Z",
        "status": null
    }

The query params are like,

=====================   ===========   =============    ================================================================
Name                     Type         Constraint       Description
=====================   ===========   =============    ================================================================
ContractNumber           String        Mandatory         Contract number
FromDate                 DateTime      Mandatory         Starting date
ToDate                   DateTime      Optional          Finishing date
TariffName               String        Optional          Tariff name
Status   	             Int           Optional          Status
=====================   ===========   =============    ================================================================

**Example response**:

.. sourcecode:: json

    [
        {
            "documentId": "113175fb-44e5-433a-1935-08d9db648dd8",
            "contractName": "Evergreen",
            "carrier": "EGLV",
            "type": "SeaContainer",
            "rates": [
                {
                    "pol": "ESVLC",
                    "polServiceType": null,
                    "pod": "BRPEC",
                    "podServiceType": null,
                    "startDate": "2022-01-01T00:00:00",
                    "endDate": "2023-08-31T00:00:00",
                    "timeInTransit": 24,
                    "via": null,
                    "containerType": "DRY40",
                    "costs": [
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "ERS",
                            "chargeDescription": "Equipment Repositionning Surcharge",
                            "amount": 30000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "ALF",
                            "chargeDescription": "Agency Logistic fee",
                            "amount": 1000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "VGM",
                            "chargeDescription": "Verified Gross Mass",
                            "amount": 1000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "PAL",
                            "chargeDescription": "Port additionals",
                            "amount": 5000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "DOC",
                            "chargeDescription": "Documentation Fee",
                            "amount": 5000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "THC",
                            "chargeDescription": "Terminal handling charge",
                            "amount": 23500,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "PSS",
                            "chargeDescription": "Peak Season Surcharge",
                            "amount": 60000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "CSS",
                            "chargeDescription": "Carrier security surcharge (Carrier ISPS)",
                            "amount": 900,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "BAF",
                            "chargeDescription": "Bunker ajustement factor",
                            "amount": 31600,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "FRT",
                            "chargeDescription": "Seafreight",
                            "amount": 150000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        }
                    ]
                },
                {
                    "pol": "ESVLC",
                    "polServiceType": null,
                    "pod": "BRPEC",
                    "podServiceType": null,
                    "startDate": "2022-01-01T00:00:00",
                    "endDate": "2023-08-31T00:00:00",
                    "timeInTransit": 24,
                    "via": null,
                    "containerType": "HDRY45",
                    "costs": [
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "ERS",
                            "chargeDescription": "Equipment Repositionning Surcharge",
                            "amount": 30000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "ALF",
                            "chargeDescription": "Agency Logistic fee",
                            "amount": 1000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "VGM",
                            "chargeDescription": "Verified Gross Mass",
                            "amount": 1000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "PAL",
                            "chargeDescription": "Port additionals",
                            "amount": 5000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "DOC",
                            "chargeDescription": "Documentation Fee",
                            "amount": 5000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "THC",
                            "chargeDescription": "Terminal handling charge",
                            "amount": 23500,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "PSS",
                            "chargeDescription": "Peak Season Surcharge",
                            "amount": 60000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "CSS",
                            "chargeDescription": "Carrier security surcharge (Carrier ISPS)",
                            "amount": 900,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "BAF",
                            "chargeDescription": "Bunker ajustement factor",
                            "amount": 31600,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "FRT",
                            "chargeDescription": "Seafreight",
                            "amount": 150000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        }
                    ]
                },
                {
                    "pol": "ESVLC",
                    "polServiceType": null,
                    "pod": "BRPEC",
                    "podServiceType": null,
                    "startDate": "2022-01-01T00:00:00",
                    "endDate": "2023-08-31T00:00:00",
                    "timeInTransit": 24,
                    "via": null,
                    "containerType": "DRY20",
                    "costs": [
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "PSS",
                            "chargeDescription": "Peak Season Surcharge",
                            "amount": 30000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "ALF",
                            "chargeDescription": "Agency Logistic fee",
                            "amount": 1000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "VGM",
                            "chargeDescription": "Verified Gross Mass",
                            "amount": 1000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "PAL",
                            "chargeDescription": "Port additionals",
                            "amount": 3600,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "DOC",
                            "chargeDescription": "Documentation Fee",
                            "amount": 5000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "THC",
                            "chargeDescription": "Terminal handling charge",
                            "amount": 23500,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "CSS",
                            "chargeDescription": "Carrier security surcharge (Carrier ISPS)",
                            "amount": 900,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "BAF",
                            "chargeDescription": "Bunker ajustement factor",
                            "amount": 15800,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "FRT",
                            "chargeDescription": "Seafreight",
                            "amount": 90000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "ERS",
                            "chargeDescription": "Equipment Repositionning Surcharge",
                            "amount": 15000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        }
                    ]
                },
                {
                    "pol": "ESVLC",
                    "polServiceType": null,
                    "pod": "BRVDC",
                    "podServiceType": null,
                    "startDate": "2022-01-01T00:00:00",
                    "endDate": "2023-08-31T00:00:00",
                    "timeInTransit": 26,
                    "via": null,
                    "containerType": "HDRY45",
                    "costs": [
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "PSS",
                            "chargeDescription": "Peak Season Surcharge",
                            "amount": 60000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "ALF",
                            "chargeDescription": "Agency Logistic fee",
                            "amount": 1000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "VGM",
                            "chargeDescription": "Verified Gross Mass",
                            "amount": 1000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "PAL",
                            "chargeDescription": "Port additionals",
                            "amount": 5000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "DOC",
                            "chargeDescription": "Documentation Fee",
                            "amount": 5000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "THC",
                            "chargeDescription": "Terminal handling charge",
                            "amount": 23500,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "ERS",
                            "chargeDescription": "Equipment Repositionning Surcharge",
                            "amount": 30000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "CSS",
                            "chargeDescription": "Carrier security surcharge (Carrier ISPS)",
                            "amount": 900,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "BAF",
                            "chargeDescription": "Bunker ajustement factor",
                            "amount": 31600,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "FRT",
                            "chargeDescription": "Seafreight",
                            "amount": 820000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        }
                    ]
                },
                {
                    "pol": "ESVLC",
                    "polServiceType": null,
                    "pod": "BRVDC",
                    "podServiceType": null,
                    "startDate": "2022-01-01T00:00:00",
                    "endDate": "2023-08-31T00:00:00",
                    "timeInTransit": 26,
                    "via": null,
                    "containerType": "DRY40",
                    "costs": [
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "ALF",
                            "chargeDescription": "Agency Logistic fee",
                            "amount": 1000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "VGM",
                            "chargeDescription": "Verified Gross Mass",
                            "amount": 1000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "PAL",
                            "chargeDescription": "Port additionals",
                            "amount": 5000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "DOC",
                            "chargeDescription": "Documentation Fee",
                            "amount": 5000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "THC",
                            "chargeDescription": "Terminal handling charge",
                            "amount": 23500,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "PSS",
                            "chargeDescription": "Peak Season Surcharge",
                            "amount": 60000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "ERS",
                            "chargeDescription": "Equipment Repositionning Surcharge",
                            "amount": 30000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "CSS",
                            "chargeDescription": "Carrier security surcharge (Carrier ISPS)",
                            "amount": 900,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "BAF",
                            "chargeDescription": "Bunker ajustement factor",
                            "amount": 31600,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "FRT",
                            "chargeDescription": "Seafreight",
                            "amount": 820000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        }
                    ]
                },
                {
                    "pol": "ESVLC",
                    "polServiceType": null,
                    "pod": "BRVDC",
                    "podServiceType": null,
                    "startDate": "2022-01-01T00:00:00",
                    "endDate": "2023-08-31T00:00:00",
                    "timeInTransit": 26,
                    "via": null,
                    "containerType": "DRY20",
                    "costs": [
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "ALF",
                            "chargeDescription": "Agency Logistic fee",
                            "amount": 1000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "VGM",
                            "chargeDescription": "Verified Gross Mass",
                            "amount": 1000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "DOC",
                            "chargeDescription": "Documentation Fee",
                            "amount": 5000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "THC",
                            "chargeDescription": "Terminal handling charge",
                            "amount": 23500,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "PAL",
                            "chargeDescription": "Port additionals",
                            "amount": 3600,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "PSS",
                            "chargeDescription": "Peak Season Surcharge",
                            "amount": 30000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "ERS",
                            "chargeDescription": "Equipment Repositionning Surcharge",
                            "amount": 15000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "CSS",
                            "chargeDescription": "Carrier security surcharge (Carrier ISPS)",
                            "amount": 900,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "BAF",
                            "chargeDescription": "Bunker ajustement factor",
                            "amount": 15800,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "FRT",
                            "chargeDescription": "Seafreight",
                            "amount": 460000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        }
                    ]
                },
                {
                    "pol": "ESVLC",
                    "polServiceType": null,
                    "pod": "BRMAO",
                    "podServiceType": null,
                    "startDate": "2022-01-01T00:00:00",
                    "endDate": "2023-08-31T00:00:00",
                    "timeInTransit": 17,
                    "via": null,
                    "containerType": "DRY40",
                    "costs": [
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "BAF",
                            "chargeDescription": "Bunker ajustement factor",
                            "amount": 31600,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "FRT",
                            "chargeDescription": "Seafreight",
                            "amount": 820000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "CSS",
                            "chargeDescription": "Carrier security surcharge (Carrier ISPS)",
                            "amount": 900,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "ALF",
                            "chargeDescription": "Agency Logistic fee",
                            "amount": 1000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "VGM",
                            "chargeDescription": "Verified Gross Mass",
                            "amount": 1000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "PAL",
                            "chargeDescription": "Port additionals",
                            "amount": 5000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "DOC",
                            "chargeDescription": "Documentation Fee",
                            "amount": 5000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "THC",
                            "chargeDescription": "Terminal handling charge",
                            "amount": 23500,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "PSS",
                            "chargeDescription": "Peak Season Surcharge",
                            "amount": 60000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "ERS",
                            "chargeDescription": "Equipment Repositionning Surcharge",
                            "amount": 30000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        }
                    ]
                },
                {
                    "pol": "ESVLC",
                    "polServiceType": null,
                    "pod": "BRMAO",
                    "podServiceType": null,
                    "startDate": "2022-01-01T00:00:00",
                    "endDate": "2023-08-31T00:00:00",
                    "timeInTransit": 17,
                    "via": null,
                    "containerType": "DRY20",
                    "costs": [
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "BAF",
                            "chargeDescription": "Bunker ajustement factor",
                            "amount": 15800,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "FRT",
                            "chargeDescription": "Seafreight",
                            "amount": 460000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "ERS",
                            "chargeDescription": "Equipment Repositionning Surcharge",
                            "amount": 15000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "CSS",
                            "chargeDescription": "Carrier security surcharge (Carrier ISPS)",
                            "amount": 900,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "ALF",
                            "chargeDescription": "Agency Logistic fee",
                            "amount": 1000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "VGM",
                            "chargeDescription": "Verified Gross Mass",
                            "amount": 1000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "PAL",
                            "chargeDescription": "Port additionals",
                            "amount": 3600,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "DOC",
                            "chargeDescription": "Documentation Fee",
                            "amount": 5000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "THC",
                            "chargeDescription": "Terminal handling charge",
                            "amount": 23500,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "PSS",
                            "chargeDescription": "Peak Season Surcharge",
                            "amount": 30000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        }
                    ]
                },
                {
                    "pol": "ESVLC",
                    "polServiceType": null,
                    "pod": "BRMAO",
                    "podServiceType": null,
                    "startDate": "2022-01-01T00:00:00",
                    "endDate": "2023-08-31T00:00:00",
                    "timeInTransit": 17,
                    "via": null,
                    "containerType": "HDRY45",
                    "costs": [
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "FRT",
                            "chargeDescription": "Seafreight",
                            "amount": 820000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "BAF",
                            "chargeDescription": "Bunker ajustement factor",
                            "amount": 31600,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "CSS",
                            "chargeDescription": "Carrier security surcharge (Carrier ISPS)",
                            "amount": 900,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "ALF",
                            "chargeDescription": "Agency Logistic fee",
                            "amount": 1000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "VGM",
                            "chargeDescription": "Verified Gross Mass",
                            "amount": 1000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "PAL",
                            "chargeDescription": "Port additionals",
                            "amount": 5000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "DOC",
                            "chargeDescription": "Documentation Fee",
                            "amount": 5000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "THC",
                            "chargeDescription": "Terminal handling charge",
                            "amount": 23500,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "PSS",
                            "chargeDescription": "Peak Season Surcharge",
                            "amount": 60000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "ERS",
                            "chargeDescription": "Equipment Repositionning Surcharge",
                            "amount": 30000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        }
                    ]
                },
                {
                    "pol": "ESVLC",
                    "polServiceType": null,
                    "pod": "BRIOA",
                    "podServiceType": null,
                    "startDate": "2022-01-01T00:00:00",
                    "endDate": "2023-08-31T00:00:00",
                    "timeInTransit": 15,
                    "via": null,
                    "containerType": "HDRY45",
                    "costs": [
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "BAF",
                            "chargeDescription": "Bunker ajustement factor",
                            "amount": 31600,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "CSS",
                            "chargeDescription": "Carrier security surcharge (Carrier ISPS)",
                            "amount": 900,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "FRT",
                            "chargeDescription": "Seafreight",
                            "amount": 120000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "ALF",
                            "chargeDescription": "Agency Logistic fee",
                            "amount": 1000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "VGM",
                            "chargeDescription": "Verified Gross Mass",
                            "amount": 1000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "PAL",
                            "chargeDescription": "Port additionals",
                            "amount": 5000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "DOC",
                            "chargeDescription": "Documentation Fee",
                            "amount": 5000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Origin",
                            "chargeName": "THC",
                            "chargeDescription": "Terminal handling charge",
                            "amount": 23500,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "PSS",
                            "chargeDescription": "Peak Season Surcharge",
                            "amount": 60000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        },
                        {
                            "commodity": null,
                            "chargeType": "Freight",
                            "chargeName": "ERS",
                            "chargeDescription": "Equipment Repositionning Surcharge",
                            "amount": 30000,
                            "currency": "EUR",
                            "chargeUnit": "Specific",
                            "criteria": null,
                            "extraInfo": null
                        }
                    ]
                }
            ]
        }
    ]

* Tariff model:

===========================   ====================   ===============================================
    Name                          Type                   Description
===========================   ====================   ===============================================
 Carrier                        String                 Carrier
 Name                           String                 Name 
 Type                           Int                    Tariff type (FCL/LCL)
 Rates	           	            List<Rate>             List of rates belonging to the tariff
===========================   ====================   ===============================================

* Tariff Rate model:

===========================   ====================   ===============================================
    Name                          Type                   Description
===========================   ====================   ===============================================
  POL                           String	               Origin Port
  POLServiceType                String?	               Origin service type
  POD           	            String	               Destination Port
  PODServiceType                String?	               Destination service type
  StartDate                     DateTime               Starting date
  EndDate                       DateTime?              Finishing date
  ContainerType                 String                 Container type
  Via                           DateTime               Vias
  TimeInTransit                 DateTime               Time in transit
  Costs                         List<Cost>             List of cost belonging to the rate 
===========================   ====================   ===============================================

* Tariff Cost model:

===========================   ====================   ===============================================
    Name                          Type                   Description
===========================   ====================   ===============================================
  Commodity                     String	               Commodity
  ChargeType                    String	               Charge type
  ChargeName           	        String	               Charge name
  ChargeDescription             String	               Charge description
  Amount                        Long                   Cost price
  Currency                      String                 Currency
  ChargeUnit                    String                 Finishing date
  Criteria                      List<string>           List of criteria
  ExtraInfo                     String                 Extra info
===========================   ====================   ===============================================

.. autosummary::
   :toctree: generated
