# Módulo checkout Vtex

  1. Para recuperarmos o orderForm utilizamos da vtexjs o método getOrderForm().

  Ex:
  ```javascript
vtexjs.checkout.getOrderForm()
    .then(function(orderForm){
      console.log(orderForm);
    });
  ```

Abaixo as requisições que esse método encapsula:

A primeira requisição faz um POST para o endpoint abaixo:

```javascript
  https://task23557--lojausereserva.myvtex.com/api/checkout/pub/orderForm/fa30a6d69ee447d9a4c6863f72498a3e?refreshOutdatedData=true
``````

```javascript
Body
{
  "expectedOrderFormSections": [
    "items",
    "totalizers",
    "clientProfileData",
    "shippingData",
    "paymentData",
    "sellers",
    "messages",
    "marketingData",
    "clientPreferencesData",
    "storePreferencesData",
    "giftRegistryData",
    "ratesAndBenefitsData",
    "openTextField",
    "commercialConditionData",
    "customData"
  ]
}
``````
Response:
```javascript
{
    "orderFormId": "fa30a6d69ee447d9a4c6863f72498a3e",
    "salesChannel": "1",
    "loggedIn": false,
    "isCheckedIn": false,
    "storeId": null,
    "checkedInPickupPointId": null,
    "allowManualPrice": false,
    "canEditData": true,
    "userProfileId": null,
    "userType": null,
    "ignoreProfileData": false,
    "value": 161800,
    "messages": [],
    "items": [
        {
            "uniqueId": "FCF698C291794654831212A109810B5D",
            "id": "475029",
            "productId": "43077",
            "productRefId": "0085009",
            "refId": "008500990208",
            "ean": "0085009902",
            "name": "Tenis Rsv R-brooklyn Castle Rock/Branco/Preto/Cinza Escuro - 40",
            "skuName": "Castle Rock/Branco/Preto/Cinza Escuro - 40",
            "modalType": null,
            "parentItemIndex": null,
            "parentAssemblyBinding": null,
            "assemblies": [],
            "priceValidUntil": "2024-12-24T14:04:23Z",
            "tax": 0,
            "price": 95900,
            "listPrice": 95900,
            "manualPrice": null,
            "manualPriceAppliedBy": null,
            "sellingPrice": 80900,
            "rewardValue": 0,
            "isGift": false,
            "additionalInfo": {
                "dimension": null,
                "brandName": "RESERVA GO",
                "brandId": "2000003",
                "offeringInfo": null,
                "offeringType": null,
                "offeringTypeId": null
            },
            "preSaleDate": null,
            "productCategoryIds": "/432/452/453/462/",
            "productCategories": {
                "462": "Tênis",
                "453": "Coleção",
                "452": "Masculino",
                "432": "GO Reserva",
                "442": "Tênis",
                "434": "Coleção",
                "433": "Feminino"
            },
            "quantity": 2,
            "seller": "1",
            "sellerChain": [
                "1",
                "lojausereserva773014"
            ],
            "imageUrl": "http://lojausereserva.vteximg.com.br/arquivos/ids/8440873-55-55/0085009902_01.jpg?v=638381715992830000",
            "detailUrl": "/tenis-rsv-r-brooklyn0085009/p",
            "components": [],
            "bundleItems": [],
            "attachments": [],
            "attachmentOfferings": [],
            "offerings": [
                {
                    "type": "Embalagem pra Presente",
                    "id": "461320",
                    "name": "Embalagem pra Presente",
                    "allowGiftMessage": true,
                    "attachmentOfferings": [
                        {
                            "name": "message",
                            "required": false,
                            "schema": {
                                "text": {
                                    "maximumNumberOfCharacters": 300,
                                    "domain": []
                                }
                            }
                        }
                    ],
                    "price": 0
                }
            ],
            "priceTags": [
                {
                    "name": "discount@price-f7377202-ccce-4b40-bc9e-bfc90669597a#761e7464-6fe3-4a53-92b1-42d3a060db98",
                    "value": -30000,
                    "rawValue": -300.0,
                    "isPercentual": false,
                    "identifier": "f7377202-ccce-4b40-bc9e-bfc90669597a",
                    "owner": "lojausereserva"
                }
            ],
            "availability": "available",
            "measurementUnit": "un",
            "unitMultiplier": 1.0,
            "manufacturerCode": null,
            "priceDefinition": {
                "calculatedSellingPrice": 80900,
                "total": 161800,
                "sellingPrices": [
                    {
                        "value": 80900,
                        "quantity": 2
                    }
                ]
            },
            "taxCode": "6403.99.90"
        }
    ],
    "selectableGifts": [],
    "totalizers": [
        {
            "id": "Items",
            "name": "Total dos Itens",
            "value": 191800
        },
        {
            "id": "Discounts",
            "name": "Total dos Descontos",
            "value": -30000
        }
    ],
    "shippingData": {
        "address": null,
        "logisticsInfo": [
            {
                "itemIndex": 0,
                "selectedSla": null,
                "selectedDeliveryChannel": "delivery",
                "addressId": null,
                "slas": [],
                "shipsTo": [
                    "BRA"
                ],
                "itemId": "475029",
                "deliveryChannels": [
                    {
                        "id": "delivery"
                    },
                    {
                        "id": "pickup-in-point"
                    }
                ]
            }
        ],
        "selectedAddresses": [],
        "availableAddresses": [],
        "pickupPoints": [],
        "contactInformation": []
    },
    "clientProfileData": null,
    "paymentData": {
        "updateStatus": "updated",
        "installmentOptions": [
            {
                "paymentSystem": "1",
                "bin": null,
                "paymentName": null,
                "paymentGroupName": null,
                "value": 161800,
                "installments": [
                    {
                        "count": 1,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 161800,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 1,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 161800,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 2,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 80900,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 2,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 80900,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 3,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 53933,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 3,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 53933,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 4,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 40450,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 4,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 40450,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 5,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 32360,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 5,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 32360,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 6,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 26966,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 6,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 26966,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 7,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 23114,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 7,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 23114,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 8,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 20225,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 8,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 20225,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 9,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 17977,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 9,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 17977,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 10,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 16180,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 10,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 16180,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 11,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 14709,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 11,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 14709,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 12,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 13483,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 12,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 13483,
                                "total": 161800
                            }
                        ]
                    }
                ]
            },
            {
                "paymentSystem": "2",
                "bin": null,
                "paymentName": null,
                "paymentGroupName": null,
                "value": 161800,
                "installments": [
                    {
                        "count": 1,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 161800,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 1,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 161800,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 2,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 80900,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 2,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 80900,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 3,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 53933,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 3,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 53933,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 4,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 40450,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 4,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 40450,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 5,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 32360,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 5,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 32360,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 6,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 26966,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 6,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 26966,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 7,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 23114,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 7,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 23114,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 8,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 20225,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 8,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 20225,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 9,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 17977,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 9,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 17977,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 10,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 16180,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 10,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 16180,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 11,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 14709,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 11,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 14709,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 12,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 13483,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 12,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 13483,
                                "total": 161800
                            }
                        ]
                    }
                ]
            },
            {
                "paymentSystem": "3",
                "bin": null,
                "paymentName": null,
                "paymentGroupName": null,
                "value": 161800,
                "installments": [
                    {
                        "count": 1,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 161800,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 1,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 161800,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 2,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 80900,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 2,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 80900,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 3,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 53933,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 3,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 53933,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 4,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 40450,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 4,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 40450,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 5,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 32360,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 5,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 32360,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 6,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 26966,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 6,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 26966,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 7,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 23114,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 7,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 23114,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 8,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 20225,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 8,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 20225,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 9,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 17977,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 9,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 17977,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 10,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 16180,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 10,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 16180,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 11,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 14709,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 11,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 14709,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 12,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 13483,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 12,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 13483,
                                "total": 161800
                            }
                        ]
                    }
                ]
            },
            {
                "paymentSystem": "4",
                "bin": null,
                "paymentName": null,
                "paymentGroupName": null,
                "value": 161800,
                "installments": [
                    {
                        "count": 1,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 161800,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 1,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 161800,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 2,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 80900,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 2,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 80900,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 3,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 53933,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 3,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 53933,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 4,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 40450,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 4,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 40450,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 5,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 32360,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 5,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 32360,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 6,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 26966,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 6,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 26966,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 7,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 23114,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 7,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 23114,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 8,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 20225,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 8,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 20225,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 9,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 17977,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 9,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 17977,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 10,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 16180,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 10,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 16180,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 11,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 14709,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 11,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 14709,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 12,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 13483,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 12,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 13483,
                                "total": 161800
                            }
                        ]
                    }
                ]
            },
            {
                "paymentSystem": "9",
                "bin": null,
                "paymentName": null,
                "paymentGroupName": null,
                "value": 161800,
                "installments": [
                    {
                        "count": 1,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 161800,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 1,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 161800,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 2,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 80900,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 2,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 80900,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 3,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 53933,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 3,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 53933,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 4,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 40450,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 4,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 40450,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 5,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 32360,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 5,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 32360,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 6,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 26966,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 6,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 26966,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 7,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 23114,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 7,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 23114,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 8,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 20225,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 8,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 20225,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 9,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 17977,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 9,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 17977,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 10,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 16180,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 10,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 16180,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 11,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 14709,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 11,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 14709,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 12,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 13483,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 12,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 13483,
                                "total": 161800
                            }
                        ]
                    }
                ]
            },
            {
                "paymentSystem": "16",
                "bin": null,
                "paymentName": null,
                "paymentGroupName": null,
                "value": 161800,
                "installments": [
                    {
                        "count": 1,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 161800,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 1,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 161800,
                                "total": 161800
                            }
                        ]
                    }
                ]
            },
            {
                "paymentSystem": "72",
                "bin": null,
                "paymentName": null,
                "paymentGroupName": null,
                "value": 161800,
                "installments": [
                    {
                        "count": 1,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 161800,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 1,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 161800,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 2,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 80900,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 2,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 80900,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 3,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 53933,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 3,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 53933,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 4,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 40450,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 4,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 40450,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 5,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 32360,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 5,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 32360,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 6,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 26966,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 6,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 26966,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 7,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 23114,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 7,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 23114,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 8,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 20225,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 8,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 20225,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 9,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 17977,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 9,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 17977,
                                "total": 161800
                            }
                        ]
                    },
                    {
                        "count": 10,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 16180,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 10,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 16180,
                                "total": 161800
                            }
                        ]
                    }
                ]
            },
            {
                "paymentSystem": "178",
                "bin": null,
                "paymentName": null,
                "paymentGroupName": null,
                "value": 161800,
                "installments": [
                    {
                        "count": 1,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 161800,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 1,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 161800,
                                "total": 161800
                            }
                        ]
                    }
                ]
            },
            {
                "paymentSystem": "198",
                "bin": null,
                "paymentName": null,
                "paymentGroupName": null,
                "value": 161800,
                "installments": [
                    {
                        "count": 1,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 161800,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 1,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 161800,
                                "total": 161800
                            }
                        ]
                    }
                ]
            },
            {
                "paymentSystem": "713",
                "bin": null,
                "paymentName": null,
                "paymentGroupName": null,
                "value": 161800,
                "installments": [
                    {
                        "count": 1,
                        "hasInterestRate": false,
                        "interestRate": 0,
                        "value": 161800,
                        "total": 161800,
                        "sellerMerchantInstallments": [
                            {
                                "id": "LOJAUSERESERVA",
                                "count": 1,
                                "hasInterestRate": false,
                                "interestRate": 0,
                                "value": 161800,
                                "total": 161800
                            }
                        ]
                    }
                ]
            }
        ],
        "paymentSystems": [
            {
                "id": 4,
                "name": "Mastercard",
                "groupName": "creditCardPaymentGroup",
                "validator": {
                    "regex": "^((5(([1-2]|[4-5])[0-9]{8}|0((1|6)([0-9]{7}))|3(0(4((0|[2-9])[0-9]{5})|([0-3]|[5-9])[0-9]{6})|[1-9][0-9]{7})))|((508116)\\d{4,10})|((502121)\\d{4,10})|((589916)\\d{4,10})|(2[0-9]{15})|(67[0-9]{14})|(506387)\\d{4,10})",
                    "mask": "9999 9999 9999 9999",
                    "cardCodeRegex": "^[0-9]{3}$",
                    "cardCodeMask": "999",
                    "weights": [
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2
                    ],
                    "useCvv": true,
                    "useExpirationDate": true,
                    "useCardHolderName": true,
                    "useBillingAddress": true
                },
                "stringId": "4",
                "template": "creditCardPaymentGroup-template",
                "requiresDocument": true,
                "displayDocument": true,
                "isCustom": false,
                "description": null,
                "requiresAuthentication": false,
                "dueDate": "2023-12-31T13:48:08.0012423Z",
                "availablePayments": null
            },
            {
                "id": 2,
                "name": "Visa",
                "groupName": "creditCardPaymentGroup",
                "validator": {
                    "regex": "^4[0-9]{15}$",
                    "mask": "9999 9999 9999 9999",
                    "cardCodeRegex": "^[0-9]{3}$",
                    "cardCodeMask": "999",
                    "weights": [
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2
                    ],
                    "useCvv": true,
                    "useExpirationDate": true,
                    "useCardHolderName": true,
                    "useBillingAddress": true
                },
                "stringId": "2",
                "template": "creditCardPaymentGroup-template",
                "requiresDocument": true,
                "displayDocument": true,
                "isCustom": false,
                "description": null,
                "requiresAuthentication": false,
                "dueDate": "2023-12-31T13:48:08.0012423Z",
                "availablePayments": null
            },
            {
                "id": 3,
                "name": "Diners",
                "groupName": "creditCardPaymentGroup",
                "validator": {
                    "regex": "^3(0[0-5]|[68][0-9])[0-9]{11}$",
                    "mask": "9999 999999 9999",
                    "cardCodeRegex": "^[0-9]{3}$",
                    "cardCodeMask": "999",
                    "weights": [
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2
                    ],
                    "useCvv": true,
                    "useExpirationDate": true,
                    "useCardHolderName": true,
                    "useBillingAddress": true
                },
                "stringId": "3",
                "template": "creditCardPaymentGroup-template",
                "requiresDocument": true,
                "displayDocument": true,
                "isCustom": false,
                "description": null,
                "requiresAuthentication": false,
                "dueDate": "2023-12-31T13:48:08.0012423Z",
                "availablePayments": null
            },
            {
                "id": 9,
                "name": "Elo",
                "groupName": "creditCardPaymentGroup",
                "validator": {
                    "regex": "^(50(67(0[78]|1[5789]|2[012456789]|3[01234569]|4[0-7]|53|7[4-8])|9(0(0[0-9]|1[34]|2[0-7]|3[0359]|4[01235678]|5[01235789]|6[0-9]|7[01346789]|8[01234789]|9[123479])|1(0[34568]|4[6-9]|5[1-8]|8[356789])|2(2[0-2]|5[78]|6[1-9]|7[0-9]|8[01235678]|90)|357|4(0[7-9]|1[0-9]|2[0-2]|31|5[7-9]|6[0-6]|84)|55[01]|636|7(2[2-9]|6[5-9])))|4(0117[89]|3(1274|8935)|5(1416|7(393|63[12])))|6(27780|36368|5(0(0(3[12356789]|4[0-7]|7[78])|4(0[6-9]|1[0234]|2[2-9]|3[045789]|8[5-9]|9[0-9])|5(0[012346789]|1[0-9]|2[0-9]|3[0178]|5[2-9]|6[0-6]|7[7-9]|8[0-8]|9[1-8])|72[0-7]|9(0[1-9]|1[0-9]|2[0128]|3[89]|4[6-9]|5[0145]|6[235678]|71))|16(5[2-9]|6[0-9]|7[01456789])|50(0[0-9]|1[02345678]|36|5[1267]))))\\d{0,13}$",
                    "mask": "9999 9999 9999 9999",
                    "cardCodeRegex": "^[0-9]{3}$",
                    "cardCodeMask": "999",
                    "weights": [
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2
                    ],
                    "useCvv": true,
                    "useExpirationDate": true,
                    "useCardHolderName": true,
                    "useBillingAddress": true
                },
                "stringId": "9",
                "template": "creditCardPaymentGroup-template",
                "requiresDocument": true,
                "displayDocument": true,
                "isCustom": false,
                "description": null,
                "requiresAuthentication": false,
                "dueDate": "2023-12-31T13:48:08.0012423Z",
                "availablePayments": null
            },
            {
                "id": 1,
                "name": "American Express",
                "groupName": "creditCardPaymentGroup",
                "validator": {
                    "regex": "^3[47][0-9]{13}$",
                    "mask": "9999 999999 99999",
                    "cardCodeRegex": "^[0-9]{4}$",
                    "cardCodeMask": "9999",
                    "weights": [
                        1,
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2,
                        1,
                        2,
                        1
                    ],
                    "useCvv": true,
                    "useExpirationDate": true,
                    "useCardHolderName": true,
                    "useBillingAddress": true
                },
                "stringId": "1",
                "template": "creditCardPaymentGroup-template",
                "requiresDocument": true,
                "displayDocument": true,
                "isCustom": false,
                "description": null,
                "requiresAuthentication": false,
                "dueDate": "2023-12-31T13:48:08.0012423Z",
                "availablePayments": null
            },
            {
                "id": 16,
                "name": "Vale",
                "groupName": "giftCardPaymentGroup",
                "validator": {
                    "regex": null,
                    "mask": null,
                    "cardCodeRegex": null,
                    "cardCodeMask": null,
                    "weights": null,
                    "useCvv": false,
                    "useExpirationDate": false,
                    "useCardHolderName": false,
                    "useBillingAddress": false
                },
                "stringId": "16",
                "template": "giftCardPaymentGroup-template",
                "requiresDocument": false,
                "displayDocument": false,
                "isCustom": false,
                "description": null,
                "requiresAuthentication": false,
                "dueDate": "2023-12-31T13:48:08.0012423Z",
                "availablePayments": null
            },
            {
                "id": 72,
                "name": "PicPay",
                "groupName": "picPayPaymentGroup",
                "validator": {
                    "regex": null,
                    "mask": null,
                    "cardCodeRegex": null,
                    "cardCodeMask": null,
                    "weights": null,
                    "useCvv": false,
                    "useExpirationDate": false,
                    "useCardHolderName": false,
                    "useBillingAddress": false
                },
                "stringId": "72",
                "template": "picPayPaymentGroup-template",
                "requiresDocument": false,
                "displayDocument": false,
                "isCustom": false,
                "description": null,
                "requiresAuthentication": false,
                "dueDate": "2023-12-31T13:48:08.0012423Z",
                "availablePayments": null
            },
            {
                "id": 178,
                "name": "Nubank",
                "groupName": "NubankPaymentGroup",
                "validator": {
                    "regex": null,
                    "mask": null,
                    "cardCodeRegex": null,
                    "cardCodeMask": null,
                    "weights": null,
                    "useCvv": false,
                    "useExpirationDate": false,
                    "useCardHolderName": false,
                    "useBillingAddress": false
                },
                "stringId": "178",
                "template": "NubankPaymentGroup-template",
                "requiresDocument": false,
                "displayDocument": false,
                "isCustom": false,
                "description": null,
                "requiresAuthentication": false,
                "dueDate": "2023-12-31T13:48:08.0012423Z",
                "availablePayments": null
            },
            {
                "id": 713,
                "name": "Pagaleve Pix A Vista Transparente",
                "groupName": "PagalevePixAVistaTransparentePaymentGroup",
                "validator": {
                    "regex": null,
                    "mask": null,
                    "cardCodeRegex": null,
                    "cardCodeMask": null,
                    "weights": null,
                    "useCvv": false,
                    "useExpirationDate": false,
                    "useCardHolderName": false,
                    "useBillingAddress": false
                },
                "stringId": "713",
                "template": "PagalevePixAVistaTransparentePaymentGroup-template",
                "requiresDocument": false,
                "displayDocument": false,
                "isCustom": false,
                "description": null,
                "requiresAuthentication": false,
                "dueDate": "2023-12-31T13:48:08.0012423Z",
                "availablePayments": null
            },
            {
                "id": 198,
                "name": "Pagaleve Transparente",
                "groupName": "Pagaleve TransparentePaymentGroup",
                "validator": {
                    "regex": null,
                    "mask": null,
                    "cardCodeRegex": null,
                    "cardCodeMask": null,
                    "weights": null,
                    "useCvv": false,
                    "useExpirationDate": false,
                    "useCardHolderName": false,
                    "useBillingAddress": false
                },
                "stringId": "198",
                "template": "Pagaleve TransparentePaymentGroup-template",
                "requiresDocument": false,
                "displayDocument": false,
                "isCustom": false,
                "description": null,
                "requiresAuthentication": false,
                "dueDate": "2023-12-31T13:48:08.0012423Z",
                "availablePayments": null
            }
        ],
        "payments": [
            {
                "paymentSystem": "2",
                "bin": null,
                "accountId": null,
                "tokenId": null,
                "installments": null,
                "referenceValue": 161800,
                "value": 161800,
                "merchantSellerPayments": [
                    {
                        "id": "LOJAUSERESERVA",
                        "installments": null,
                        "referenceValue": 161800,
                        "value": 161800,
                        "interestRate": null,
                        "installmentValue": 0
                    }
                ]
            }
        ],
        "giftCards": [],
        "giftCardMessages": [],
        "availableAccounts": [],
        "availableTokens": [],
        "availableAssociations": {}
    },
    "marketingData": {
        "utmSource": null,
        "utmMedium": null,
        "utmCampaign": null,
        "utmipage": null,
        "utmiPart": null,
        "utmiCampaign": null,
        "coupon": null,
        "marketingTags": [
            "GO | Todos os produtos"
        ]
    },
    "sellers": [
        {
            "id": "1",
            "name": "Reserva",
            "logo": ""
        }
    ],
    "clientPreferencesData": {
        "locale": "pt-BR",
        "optinNewsLetter": null
    },
    "commercialConditionData": null,
    "storePreferencesData": {
        "countryCode": "BRA",
        "saveUserData": true,
        "timeZone": "E. South America Standard Time",
        "currencyCode": "BRL",
        "currencyLocale": 1046,
        "currencySymbol": "R$",
        "currencyFormatInfo": {
            "currencyDecimalDigits": 2,
            "currencyDecimalSeparator": ",",
            "currencyGroupSeparator": ".",
            "currencyGroupSize": 3,
            "startsWithCurrencySymbol": true
        }
    },
    "giftRegistryData": null,
    "openTextField": null,
    "invoiceData": null,
    "customData": null,
    "itemMetadata": {
        "items": [
            {
                "id": "475029",
                "seller": "1",
                "name": "Tenis Rsv R-brooklyn Castle Rock/Branco/Preto/Cinza Escuro - 40",
                "skuName": "Castle Rock/Branco/Preto/Cinza Escuro - 40",
                "productId": "43077",
                "refId": "008500990208",
                "ean": "0085009902",
                "imageUrl": "http://lojausereserva.vteximg.com.br/arquivos/ids/8440873-55-55/0085009902_01.jpg?v=638381715992830000",
                "detailUrl": "/tenis-rsv-r-brooklyn0085009/p",
                "assemblyOptions": []
            }
        ]
    },
    "hooksData": null,
    "ratesAndBenefitsData": {
        "rateAndBenefitsIdentifiers": [
            {
                "id": "f7377202-ccce-4b40-bc9e-bfc90669597a",
                "name": "GO | Special Gift  Compre R$1299 ganhe R$300 OFF",
                "featured": false,
                "description": null,
                "matchedParameters": {
                    "Seller@CatalogSystem": "1,lojausereservago,lojausereservaondemand|inclusive",
                    "productCluster@CatalogSystem": "2806|inclusive"
                },
                "additionalInfo": null
            }
        ],
        "teaser": []
    },
    "subscriptionData": null,
    "merchantContextData": null,
    "itemsOrdination": null,
    "recaptchaKey": "6LdAUOAUAAAAAG8GfSFnEdE2t6Hwq4wnIFzJKa4e",
    "recaptchaKeyV3": "6LfnCR8mAAAAAGfsca_MuJ4oXTWJWOJ4TkPFOXzT"
}
``````

Encapsuladamente ele faz algumas outras requisições:

Get:
```javascript
https://task23557--lojausereserva.myvtex.com/api/dataentities/MS/search?_where=(sellerId=1)&_fields=texto,logo,banner,bannerMobile,sellerName&1703426772354=cache
```

Response:
```javascript
[]
```

Get:
```javascript
https://task23557--lojausereserva.myvtex.com/_v/fbe/pixel
```

Response:
```javascript
{
  "pixelId": "475696979236643",
  "enablePixelIntegration": true
}
```

Get:
```javascript
https://task23557--lojausereserva.myvtex.com/_v/rsv-prime/primepromotion?1703429213697=cache
```

Response:
```javascript
{
  "idCalculatorConfiguration": "",
  "marketingTags": [],
  "name": "Reserva I PrimeTag 20%",
  "percentualDiscountValue": 20,
  "isActive": true,
  "categories": [
      {
          "id": "198",
          "name": "Cartão Presente (198)"
      },
      {
          "id": "176",
          "name": "Mini | Crianças | Cartão presente (176)"
      },
      {
          "id": "11",
          "name": "Reserva | Masculino | cartão presente (11)"
      }
  ],
  "categoriesAreInclusive": false,
  "brands": [],
  "collections": [
      {
          "id": "239",
          "name": "MINI Destaques Máscara Infantil (239)"
      },
      {
          "id": "166",
          "name": "RESERVA Novidades Camiseta Simples Assinatura (166)"
      },
      {
          "id": "353",
          "name": "Adulto Ofertas (353)"
      },
      {
          "id": "698",
          "name": "RESERVA Não Acumular Promo (698)"
      },
      {
          "id": "684",
          "name": "Reserva - Produto Surpresa (684)"
      },
      {
          "id": "685",
          "name": "RESERVA Produto Surpresa APP (685)"
      }
  ],
  "collectionsIsInclusive": false,
  "brandsAreInclusive": false,
  "idSeller": "1,lojausereservago,lojausereservaondemand",
  "idSellerIsInclusive": true,
  "totalValueFloor": 499,
  "totalValueCeling": 0
}
```

Post:
```javascript
https://task23557--lojausereserva.myvtex.com/api/io/_v/facebook-checkout-pixel/notify
```

Body:
```javascript
{
  "events": [
    {
      "eventName": "order-form-initiate-checkout",
      "eventObject": {
        "orderFormId": "fa30a6d69ee447d9a4c6863f72498a3e",
        "payload": {
          "contents": [
            {
              "id": "475029",
              "item_price": 959,
              "quantity": 2
            }
          ],
          "content_ids": [
            "475029"
          ],
          "currency": "BRL",
          "num_items": 2,
          "value": 1618
        },
        "eventId": "2fd4549f-d402-4706-a3da-8250042e39bf",
        "eventSourceURL": "https://task23557--lojausereserva.myvtex.com/checkout#/email",
        "fbpCookie": "fb.1.1702311891162.2032843782"
      },
      "userAgent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/120.0.0.0 Safari/537.36"
    }
  ]
}
```

Response:
```javascript
OK
```

