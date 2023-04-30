# Flow Documentation \- ApendiceERPA

| Flow Name                  | ApendiceERPA                             |
| -------------------------- | ---------------------------------------- |
| Flow Name                  | ApendiceERPA                             |
| Flow ID                    | 460e14ee\-f0ad\-45f1\-af6a\-4e7c7522f1dc |
| Documentation generated at | domingo, 30 de abril de 2023 02:46 p. m. |
| Number of Variables        | 0                                        |
| Number of Actions          | 8                                        |

- [Overview](../index-ApendiceERPA(460e14ee-f0ad-45f1-af6a-4e7c7522f1dc).md)
- [Connection References](../connections-ApendiceERPA(460e14ee-f0ad-45f1-af6a-4e7c7522f1dc).md)
- [Variables](../variables-ApendiceERPA(460e14ee-f0ad-45f1-af6a-4e7c7522f1dc).md)
- [Triggers & Actions](../triggersactions-ApendiceERPA(460e14ee-f0ad-45f1-af6a-4e7c7522f1dc).md)

## Obtener\_Contenido\_de\_Plantilla\_ERPA

| Property   | Value                                                                                                               |
| ---------- | ------------------------------------------------------------------------------------------------------------------- |
| Name       | Obtener\_Contenido\_de\_Plantilla\_ERPA                                                                             |
| Type       | OpenApiConnection                                                                                                   |
| Connection | [![sharepointonline](../sharepointonline32.png) SharePoint](https://docs.microsoft.com/connectors/sharepointonline) |

### Inputs

| Property       | Value                                                                                                                                                                                                                                                      |
| -------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| metadata       | <table><tr><td>%252fApndices%2bERPA%252f001%2bAp%25c3%25a9ndice%2bERPA%2bTemplate.docx</td><td>/Apndices ERPA/001 Apéndice ERPA Template.docx</td></tr><tr><td>operationMetadataId</td><td>ffdd1040-02dd-4221-9af2-7d18b2c51e29</td></tr></table>          |
| host           | <table><tr><td>apiId</td><td>/providers/Microsoft.PowerApps/apis/shared_sharepointonline</td></tr><tr><td>connectionName</td><td>shared_sharepointonline</td></tr><tr><td>operationId</td><td>GetFileContent</td></tr></table>                             |
| parameters     | <table><tr><td>dataset</td><td>https://canopiacarbon918.sharepoint.com/sites/intranet</td></tr><tr><td>id</td><td>%252fApndices%2bERPA%252f001%2bAp%25c3%25a9ndice%2bERPA%2bTemplate.docx</td></tr><tr><td>inferContentType</td><td>True</td></tr></table> |
| authentication | <table><tr><td>value</td><td>@json(decodeBase64(triggerOutputs().headers['X-MS-APIM-Tokens']))['$ConnectionKey']</td></tr><tr><td>type</td><td>Raw</td></tr></table>                                                                                       |

### Next Action(s) Conditions

| Next Action                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------- |
| [Crear\_Apendice\_ERPA \[Succeeded\]](Crear_Apendice_ERPA-ApendiceERPA(460e14ee-f0ad-45f1-af6a-4e7c7522f1dc).md) |
