<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
Entity: MaterialAddition  
========================<!-- /10-Header -->  
<!-- 15-License -->  
[Open License](https://github.com/smart-data-models//dataModel.IndustrialProcess/blob/master/MaterialAddition/LICENSE.md)  
[document generated automatically](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## List of properties  

<sup><sub>[*] If there is not a type in an attribute is because it could have several types or different formats/patterns</sub></sup>  
<!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
Required properties  
- No required properties  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
This data model delivers data related to material additions performed in a process plant. The data model has been developed from the needs of steelmaking, but similar data structures are expected appropriate in other application areas as well. The process can be a batch process or continuous.  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## Data Model description of properties  
Sorted alphabetically (click for details)  
<!-- /50-DataModelHeader -->  
<!-- 60-ModelYaml -->  
<!-- /60-ModelYaml -->  
<!-- 70-MiddleNotes -->  
<!-- /70-MiddleNotes -->  
<!-- 80-Examples -->  
## Example payloads    
#### MaterialAddition NGSI-v2 key-values Example    
Here is an example of a MaterialAddition in JSON-LD format as key-values. This is compatible with NGSI-v2 when  using `options=keyValues` and returns the context data of an individual entity.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
  "id": "urn:ngsi-ld:MaterialAddition:PlantZ:UnitProcessX:75545",  
  "type": "MaterialAddition",  
  "dateObserved": "2025-07-17T14:07:00Z",  
  "processName": "unit_process_x",  
  "heatNumber": 10001,  
  "addedMaterials":  
  [  
    {  
      "code": "scrap_type_3",  
      "mass": 40000,  
      "category": "scrap",  
      "chemicalConcentration":  
      [  
        {  
          "substance": "Fe",  
          "percentage": 0.9973  
        },  
        {  
          "substance": "Cu",  
          "percentage": 0.0005  
        }  
      ],  
      "specificEnergy": 1.3,  
      "source": "my-id-1",  
      "origin": "my-id-2",  
      "supplier": "ACME",  
      "materialPrice": 0.02,  
      "storageAvailability": 250000  
    }  
  ]  
}  
```  
</details>  
#### MaterialAddition NGSI-v2 normalized Example    
Here is an example of a MaterialAddition in JSON-LD format as normalized. This is compatible with NGSI-v2 when not using options and returns the context data of an individual entity.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
  "id": "urn:ngsi-ld:MaterialAddition:PlantZ:UnitProcessX:75545",  
  "type": "MaterialAddition",  
  "dateObserved": {  
    "type": "DateTime",  
    "value": "2025-07-17T14:07:00Z"  
  },  
  "processName": {  
    "type": "Text",  
    "value": "unit_process_x"  
  },  
  "heatNumber": {  
    "type": "Number",  
    "value": 10001  
  },  
  "addedMaterials": {  
    "type": "StructuredValue",  
    "value": [  
      {  
        "type": "StructuredValue",  
        "value": {  
          "code": {  
            "type": "Text",  
            "value": "scrap_type_3"  
          },  
          "mass": {  
            "type": "Number",  
            "value": 40000  
          },  
          "category": {  
            "type": "Text",  
            "value": "scrap"  
          },  
          "chemicalConcentration": {  
            "type": "StructuredValue",  
            "value": [  
              {  
                "type": "StructuredValue",  
                "value": {  
                  "substance": {  
                    "type": "Text",  
                    "value": "Fe"  
                  },  
                  "percentage": {  
                    "type": "Number",  
                    "value": 0.9973  
                  }  
                }  
              },  
              {  
                "type": "StructuredValue",  
                "value": {  
                  "substance": {  
                    "type": "Text",  
                    "value": "Cu"  
                  },  
                  "percentage": {  
                    "type": "Number",  
                    "value": 0.0005  
                  }  
                }  
              }  
            ]  
          },  
          "specificEnergy": {  
            "type": "Number",  
            "value": 1.3  
          },  
          "source": {  
            "type": "Text",  
            "value": "my-id-1"  
          },  
          "origin": {  
            "type": "Text",  
            "value": "my-id-2"  
          },  
          "supplier": {  
            "type": "Text",  
            "value": "ACME"  
          },  
          "materialPrice": {  
            "type": "Number",  
            "value": 0.02  
          },  
          "storageAvailability": {  
            "type": "Number",  
            "value": 250000  
          }  
        }  
      }  
    ]  
  }  
}  
```  
</details>  
#### MaterialAddition NGSI-LD key-values Example    
Here is an example of a MaterialAddition in JSON-LD format as key-values. This is compatible with NGSI-LD when  using `options=keyValues` and returns the context data of an individual entity.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
  "@context": [  
    "https://raw.githubusercontent.com/smart-data-models/incubated/refs/heads/smartmanufacturing-processindustry/SMARTMANUFACTURING/ProcessIndustry/context.jsonld"  
  ],  
  "id": "urn:ngsi-ld:MaterialAddition:PlantZ:UnitProcessX:75545",  
  "type": "MaterialAddition",  
  "dateObserved": "2025-07-17T14:07:00Z",  
  "processName": "unit_process_x",  
  "heatNumber": 10001,  
  "addedMaterials":  
  [  
    {  
      "code": "scrap_type_3",  
      "mass": 40000,  
      "category": "scrap",  
      "chemicalConcentration":  
      [  
        {  
          "substance": "Fe",  
          "percentage": 0.9973  
        },  
        {  
          "substance": "Cu",  
          "percentage": 0.0005  
        }  
      ],  
      "specificEnergy": 1.3,  
      "source": "my-id-1",  
      "origin": "my-id-2",  
      "supplier": "ACME",  
      "materialPrice": 0.02,  
      "storageAvailability": 250000  
    }  
  ]  
}  
```  
</details>  
#### MaterialAddition NGSI-LD normalized Example    
Here is an example of a MaterialAddition in JSON-LD format as normalized. This is compatible with NGSI-LD when not using options and returns the context data of an individual entity.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
  "@context": [  
    "https://raw.githubusercontent.com/smart-data-models/incubated/refs/heads/smartmanufacturing-processindustry/SMARTMANUFACTURING/ProcessIndustry/context.jsonld"  
  ],  
  "id": "urn:ngsi-ld:MaterialAddition:PlantZ:UnitProcessX:75545",  
  "type": "MaterialAddition",  
  "dateObserved": {  
    "type": "Property",  
    "value": {  
      "@type": "DateTime",  
      "@value": "2025-07-17T14:07:00Z"  
    }  
  },  
  "processName": {  
    "type": "Property",  
    "value": "unit_process_x"  
  },  
  "heatNumber": {  
    "type": "Property",  
    "value": 10001  
  },  
  "addedMaterials": {  
    "type": "Property",  
    "value": [  
      {  
        "type": "Property",  
        "value": {  
          "code": {  
            "type": "Property",  
            "value": "scrap_type_3"  
          },  
          "mass": {  
            "type": "Property",  
            "value": 40000  
          },  
          "category": {  
            "type": "Property",  
            "value": "scrap"  
          },  
          "chemicalConcentration": {  
            "type": "Property",  
            "value": [  
              {  
                "type": "Property",  
                "value": {  
                  "substance": {  
                    "type": "Property",  
                    "value": "Fe"  
                  },  
                  "percentage": {  
                    "type": "Property",  
                    "value": 0.9973  
                  }  
                }  
              },  
              {  
                "type": "Property",  
                "value": {  
                  "substance": {  
                    "type": "Property",  
                    "value": "Cu"  
                  },  
                  "percentage": {  
                    "type": "Property",  
                    "value": 0.0005  
                  }  
                }  
              }  
            ]  
          },  
          "specificEnergy": {  
            "type": "Property",  
            "value": 1.3  
          },  
          "source": {  
            "type": "Property",  
            "value": "my-id-1"  
          },  
          "origin": {  
            "type": "Property",  
            "value": "my-id-2"  
          },  
          "supplier": {  
            "type": "Property",  
            "value": "ACME"  
          },  
          "materialPrice": {  
            "type": "Property",  
            "value": 0.02  
          },  
          "storageAvailability": {  
            "type": "Property",  
            "value": 250000  
          }  
        }  
      }  
    ]  
  }  
}  
```  
</details><!-- /80-Examples -->  
<!-- 90-FooterNotes -->  
These data models were developed in the project ALCHIMIA - Data and decentralized Artificial intelligence for a competitive and green European metallurgy industry. This project has received funding from the European Union’s Horizon 2020 research and innovation program under grant agreement No 101070046. See https://alchimia-project.eu/  
<!-- /90-FooterNotes -->  
<!-- 95-Units -->  
See [FAQ 10](https://smartdatamodels.org/index.php/faqs/) to get an answer on how to deal with magnitude units  
<!-- /95-Units -->  
<!-- 97-LastFooter -->  
---  
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->  
