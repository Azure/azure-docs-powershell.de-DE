---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
ms.openlocfilehash: 064ccbcfa94137f5221a5d08e0a06e09328e0b1f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658579"
---
# Get-AzAppServicePlan

## Synopsis
Ruft einen Azure-App-Dienstplan in der angegebenen Ressourcengruppe ab.

## Syntax

### S1
```
Get-AzAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
Get-AzAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzAppServicePlan** " Ruft einen Azure App-Dienstplan in der angegebenen Ressourcengruppe ab.

## Beispiele

### Beispiel 1: Abrufen eines App-Service Plans aus einer Ressourcengruppe
```
PS C:\>Get-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

Dieser Befehl ruft den App-Dienstplan mit dem Namen ContosoASP ab, der zur Ressourcengruppe Default-Web-westus gehört.

### Beispiel 2: Abrufen aller App-Service Pläne an einem Speicherort
```
PS C:\>Get-AzAppServicePlan -Location "West US"
```

Dieser Befehl ruft alle App-Service Pläne ab, die sich in der Region "West USA" befinden.

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

### -Standort
Lage 

```yaml
Type: System.String
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Name des App-Service Plans

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
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

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### Microsoft. Azure. Commands. webapps. Models. PSAppServicePlan.

## Notizen

## Verwandte Links

[Neu – AzAppServicePlan](./New-AzAppServicePlan.md)

[Remove-AzAppServicePlan](./Remove-AzAppServicePlan.md)

[Satz-AzAppServicePlan](./Set-AzAppServicePlan.md)


