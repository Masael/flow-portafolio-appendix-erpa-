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

## Limpiar\_Caché

| Property   | Value                                                                                                               |
| ---------- | ------------------------------------------------------------------------------------------------------------------- |
| Name       | Limpiar\_Caché                                                                                                      |
| Type       | OpenApiConnection                                                                                                   |
| Connection | [![sharepointonline](../sharepointonline32.png) SharePoint](https://docs.microsoft.com/connectors/sharepointonline) |

### Inputs

| Property       | Value                                                                                                                                                                                                                      |
| -------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| metadata       | <table><tr><td>operationMetadataId</td><td>98c08f87-1ddf-4c08-823f-d5ef0e2b76f6</td></tr></table>                                                                                                                          |
| host           | <table><tr><td>apiId</td><td>/providers/Microsoft.PowerApps/apis/shared_sharepointonline</td></tr><tr><td>connectionName</td><td>shared_sharepointonline</td></tr><tr><td>operationId</td><td>DeleteFile</td></tr></table> |
| parameters     | <table><tr><td>dataset</td><td>https://canopiacarbon918.sharepoint.com/sites/intranet</td></tr><tr><td>id</td><td>@outputs('Actualizar_Apendice_ERPA')?['body/{Identifier}']</td></tr></table>                             |
| authentication | <table><tr><td>value</td><td>@json(decodeBase64(triggerOutputs().headers['X-MS-APIM-Tokens']))['$ConnectionKey']</td></tr><tr><td>type</td><td>Raw</td></tr></table>                                                       |
