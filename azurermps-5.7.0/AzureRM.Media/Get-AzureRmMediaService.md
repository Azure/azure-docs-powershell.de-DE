---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/get-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaService.md
ms.openlocfilehash: 8b1f4a10ab974f50a01ba0725285ccd7a3b7dffc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663249"
---
# Get-AzureRmMediaService

## Synopsis
Ruft Informationen zu einem Mediendienst ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ResourceGroupParameterSet
```
Get-AzureRmMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### AccountNameParameterSet
```
Get-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmMediaService** " Ruft Informationen zu einem Mediendienst ab.

## Beispiele

### Beispiel 1: Abrufen aller Mediendienste in einer Ressourcengruppe
```
PS C:\>Get-AzureRmMediaService -ResourceGroupName "ResourceGroup001"
```

Dieser Befehl ruft Eigenschaften für alle Mediendienste in der Ressourcengruppe mit dem Namen ResourceGroup001 ab.

### Beispiel 2: Abrufen von Mediendienst Eigenschaften
```
PS C:\>Get-AzureRmMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

Dieser Befehl ruft die Eigenschaften des Medien Diensts mit dem Namen MediaService1 ab, der zur Ressourcengruppe mit dem Namen ResourceGroup002 gehört.

## Parameter

### -Kontoname
Gibt den Namen des Medien Diensts an, den dieses Cmdlet erhält.

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, die den Mediendienst enthält.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Microsoft. Azure. Commands. Media. Models. PSMediaService

## Notizen

## Verwandte Links

[Neu – AzureRmMediaService](./New-AzureRmMediaService.md)

[Remove-AzureRmMediaService](./Remove-AzureRmMediaService.md)

[Satz-AzureRmMediaService](./Set-AzureRmMediaService.md)


