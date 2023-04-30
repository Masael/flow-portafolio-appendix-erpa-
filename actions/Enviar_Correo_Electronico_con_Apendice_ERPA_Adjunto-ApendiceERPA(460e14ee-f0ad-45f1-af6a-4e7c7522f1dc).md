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

## Enviar\_Correo\_Electronico\_con\_Apendice\_ERPA\_Adjunto

| Property   | Value                                                                                                  |
| ---------- | ------------------------------------------------------------------------------------------------------ |
| Name       | Enviar\_Correo\_Electronico\_con\_Apendice\_ERPA\_Adjunto                                              |
| Type       | OpenApiConnection                                                                                      |
| Connection | [![office365](../office36532.png) Office 365 Outlook](https://docs.microsoft.com/connectors/office365) |

### Inputs

| Property       | Value                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| -------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| metadata       | <table><tr><td>operationMetadataId</td><td>a85867ba-0448-4b19-b068-29b6881e4182</td></tr></table>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| host           | <table><tr><td>apiId</td><td>/providers/Microsoft.PowerApps/apis/shared_office365</td></tr><tr><td>connectionName</td><td>shared_office365</td></tr><tr><td>operationId</td><td>SendEmailV2</td></tr></table>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| parameters     | <table><tr><td>emailMessage/To</td><td>lizette@canopiacarbon.com</td></tr><tr><td>emailMessage/Subject</td><td>Apendice ERPA proyecto @{outputs('Actualizar_Apendice_ERPA')?['body/ProjectName']}</td></tr><tr><td>emailMessage/Body</td><td><p>Apendice ERPA @{outputs('Crear_Apendice_ERPA')?['body/Name']} adjunto.&nbsp;</p></td></tr><tr><td>emailMessage/Cc</td><td>jose@canopiacarbon.com;adolfo@CanopiaCarbon918.onmicrosoft.com</td></tr><tr><td>emailMessage/Attachments</td><td><table><tr><td>Name</td><td>@outputs('Crear_Apendice_ERPA')?['body/Name']</td></tr></table><table><tr><td>ContentBytes</td><td>@body('Obtener_Contenido_de_Apendice_ERPA')</td></tr></table></td></tr><tr><td>emailMessage/Importance</td><td>Normal</td></tr></table> |
| authentication | <table><tr><td>value</td><td>@json(decodeBase64(triggerOutputs().headers['X-MS-APIM-Tokens']))['$ConnectionKey']</td></tr><tr><td>type</td><td>Raw</td></tr></table>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |

### Next Action(s) Conditions

| Next Action                                                                                         |
| --------------------------------------------------------------------------------------------------- |
| [Limpiar\_Caché \[Succeeded\]](Limpiar_Cache-ApendiceERPA(460e14ee-f0ad-45f1-af6a-4e7c7522f1dc).md) |
