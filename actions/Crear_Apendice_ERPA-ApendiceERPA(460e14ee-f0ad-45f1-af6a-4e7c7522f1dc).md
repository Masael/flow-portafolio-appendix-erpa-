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

## Crear\_Apendice\_ERPA

| Property   | Value                                                                                                               |
| ---------- | ------------------------------------------------------------------------------------------------------------------- |
| Name       | Crear\_Apendice\_ERPA                                                                                               |
| Type       | OpenApiConnection                                                                                                   |
| Connection | [![sharepointonline](../sharepointonline32.png) SharePoint](https://docs.microsoft.com/connectors/sharepointonline) |

### Inputs

| Property             | Value                                                                                                                                                                                                                                                                                                                                            |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| metadata             | <table><tr><td>operationMetadataId</td><td>183c413b-f005-4124-a347-0ba6b2a07e15</td></tr></table>                                                                                                                                                                                                                                                |
| host                 | <table><tr><td>apiId</td><td>/providers/Microsoft.PowerApps/apis/shared_sharepointonline</td></tr><tr><td>connectionName</td><td>shared_sharepointonline</td></tr><tr><td>operationId</td><td>CreateFile</td></tr></table>                                                                                                                       |
| parameters           | <table><tr><td>dataset</td><td>https://canopiacarbon918.sharepoint.com/sites/intranet</td></tr><tr><td>folderPath</td><td>/Apndices ERPA</td></tr><tr><td>name</td><td>@{outputs('Obtener_Registro_Apendice_ERPA')?['body/Title']} @{utcNow()}.docx</td></tr><tr><td>body</td><td>@body('Obtener_Contenido_de_Plantilla_ERPA')</td></tr></table> |
| authentication       | <table><tr><td>value</td><td>@json(decodeBase64(triggerOutputs().headers['X-MS-APIM-Tokens']))['$ConnectionKey']</td></tr><tr><td>type</td><td>Raw</td></tr></table>                                                                                                                                                                             |
| runtimeConfiguration | <table><tr><td>contentTransfer</td><td><table><tr><td>transferMode</td><td>Chunked</td></tr></table></td></tr></table>                                                                                                                                                                                                                           |

### Next Action(s) Conditions

| Next Action                                                                                                                |
| -------------------------------------------------------------------------------------------------------------------------- |
| [Actualizar\_Apendice\_ERPA \[Succeeded\]](Actualizar_Apendice_ERPA-ApendiceERPA(460e14ee-f0ad-45f1-af6a-4e7c7522f1dc).md) |
