---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
ms.openlocfilehash: 64945cf503248fc0561dc894090c73d2d7151e4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663282"
---
# Get-AzureRmWebApp

## Synopsis
Ruft Azure Web Apps in der angegebenen Ressourcengruppe ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### S1
```
Get-AzureRmWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### S2
```
Get-AzureRmWebApp [-AppServicePlan] <ServerFarmWithRichSku> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### S3
```
Get-AzureRmWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmWebApp** " Ruft Informationen zu einer Azure Web App ab.

## Beispiele

### Beispiel 1: Abrufen einer Web-App aus einer Ressourcengruppe
```
PS C:\>Get-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -SlotName "Slot001"
```

Dieser Befehl ruft die Web-App mit dem Namen ContosoSite ab, die der Ressourcengruppe Default-Web-westus angehört.

## Parameter

### -AppServicePlan
App-Service Plan Objekt

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Standort
Lage

```yaml
Type: System.String
Parameter Sets: S3
Aliases: 

Required: True
Position: 0
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

Required: False
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

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Neu – AzureRmWebApp](./New-AzureRmWebApp.md)

[Remove-AzureRmWebApp](./Remove-AzureRmWebApp.md)

[Neustart-AzureRmWebApp](./Restart-AzureRmWebApp.md)

[Anfang-AzureRmWebApp](./Start-AzureRmWebApp.md)

[Stopp-AzureRmWebApp](./Stop-AzureRmWebApp.md)


