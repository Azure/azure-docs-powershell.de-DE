---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: d0bca8fadf9179990eb5901e67ee07a3532a39cb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658499"
---
# Set-AzWebAppSlot

## Synopsis
Ändert einen Azure Web App-Steckplatz.

## Syntax

### S1
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ContainerImageName <String>]
 [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-AsJob] [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>]
 [-AzureStoragePath <WebAppAzureStoragePath[]>] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Set-AzWebApp** " legt einen Azure Web App-Steckplatz fest.

## Beispiele

### Beispiel 1
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

Mit diesem Befehl wird der Appservice-Plan geändert, der dem Slot001 zugeordnet ist, und zwar auf dem ContosoWebApp, das der Ressourcengruppe Default-Web-westus zugeordnet ist. Verwenden Sie den Link zu learm, um mehr über das Ändern des Appservice-Plans und die damit verbundenen Einschränkungen zu erfahren.
https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan

### Beispiel 2
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

Mit diesem Befehl wird HttpLoggingEnabled auf "true" festgelegt, wenn der Slot Slot001 in Bezug auf Web-App-ContosoWebApp, die mit der Ressourcengruppe Standard verknüpft sind-Web-westus

## Parameter

### -AppServicePlan
Name des App-Service Plans

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AppSettings
Hashtable für App-Einstellungen

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
Ausführen eines Cmdlets im Hintergrund

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AssignIdentity
Aktivieren/Deaktivieren von MSI für einen vorhandenen Steckplatz [Preview]

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AutoSwapSlotName
Name des Ziel Steckplatzes für den automatischen Austausch

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureStoragePath
Azure-Speicher, der in einer Web-App für Container bereitgestellt werden soll. Verwenden von New-AzureRmWebAppAzureStoragePath zum Erstellen

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath[]
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionStrings
Hashtable für Verbindungszeichenfolgen

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContainerImageName
Name des Container Bilds

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContainerRegistryPassword
Registrierungskennwort für private Container

```yaml
Type: System.Security.SecureString
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContainerRegistryUrl
URL des Registrierungsservers für private Container

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContainerRegistryUser
Benutzername für private Container-Registrierung

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultDocuments
Standard-Zeichenfolgen Array für Dokumente

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DetailedErrorLoggingEnabled
Detaillierte Fehlerprotokollierung aktiviert boolescher Wert

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableContainerContinuousDeployment
Aktiviert/deaktiviert die Container-fortlaufende Bereitstellung webhook

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HandlerMappings
Handler-Zuordnungen, IList

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HttpLoggingEnabled
HttpLoggingEnabled-boolescher Wert

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HttpsOnly
Aktivieren/Deaktivieren der Umleitung des gesamten Datenverkehrs an HTTPS auf einem vorhandenen Steckplatz

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedPipelineMode
Name des verwalteten Pipeline Modus

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Classic, Integrated

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Name des Webhosts

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NetFrameworkVersion
NET Framework-Version

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NumberOfWorkers
Die Anzahl der Arbeitskräfte, die zugewiesen werden sollen

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PhpVersion
PHP-Version

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequestTracingEnabled
Anforderungs Ablaufverfolgung aktiviert boolescher Wert

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Ressourcengruppen Name

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
Name des webslots

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Use32BitWorkerProcess
Verwenden des 32-Bit-Workerprozess-booleschen Werts

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Webbasierte
Webobjekt

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebSocketsEnabled
Web Sockets enabled Boolescher Wert

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. Int32

### System. String

### Microsoft. Azure. Commands. webapps. Models. PSSite

## Ausgaben

### Microsoft. Azure. Commands. webapps. Models. PSSite

## Notizen

## Verwandte Links

[Get-AzWebAppSlot](./Get-AzWebAppSlot.md)

[Neu – AzWebAppSlot](./New-AzWebAppSlot.md)

[Remove-AzWebAppSlot](./Remove-AzWebAppSlot.md)

[Neustart-AzWebAppSlot](./Restart-AzWebAppSlot.md)

[Anfang-AzWebAppSlot](./Start-AzWebAppSlot.md)

[Stopp-AzWebAppSlot](./Stop-AzWebAppSlot.md)

[Get-AzAppServicePlan](./Get-AzAppServicePlan.md)
