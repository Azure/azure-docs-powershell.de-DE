---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
ms.openlocfilehash: 09c618e617775e0c2bfffab1794f2427f97d811c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658493"
---
# Start-AzWebApp

## Synopsis
Startet eine Azure Web App.

## Syntax

### S1
```
Start-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### S2
```
Start-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Start-AzWebApp** startet eine Azure Web App.

## Beispiele

### Beispiel 1: Starten einer Web-App
```
PS C:\>Start-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

Mit diesem Befehl wird die Web-App mit dem Namen ContosoWebApp gestartet, die zu der Ressourcengruppe Default-Web-westus gehört.

## Parameter

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

### Microsoft. Azure. Commands. webapps. Models. PSSite

## Ausgaben

### Microsoft. Azure. Commands. webapps. Models. PSSite

## Notizen

## Verwandte Links

[Get-AzWebApp](./Get-AzWebApp.md)

[Neu – AzWebApp](./New-AzWebApp.md)

[Remove-AzWebApp](./Remove-AzWebApp.md)

[Neustart-AzWebApp](./Restart-AzWebApp.md)

[Stopp-AzWebApp](./Stop-AzWebApp.md)


