---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/get-azurermmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
ms.openlocfilehash: ed91cc0c6558797ee1b46070978fe2a41dfb94e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499825"
---
# Get-AzureRmMediaServiceNameAvailability

## Synopsis
Überprüft, ob ein Mediendienst Name verfügbar ist.
Mediendienst Namen sind global eindeutig.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmMediaServiceNameAvailability** " überprüft, ob ein Mediendienst Name verfügbar ist.
Mediendienst Namen sind global eindeutig.

## Beispiele

### Beispiel 1: überprüfen, ob ein Mediendienst Name verfügbar ist
```
PS C:\>Get-AzureRmMediaServiceNameAvailability -AccountName "MediaService1"
```

Dieser Befehl überprüft, ob der Name MediaService1 verfügbar ist.

## Parameter

### -Kontoname
Gibt den Namen des Medien Diensts an, den dieses Cmdlet erhält.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Microsoft. Azure. Commands. Media. Models. PSCheckNameAvailabilityOutput

## Notizen

## Verwandte Links

[Get-AzureRmMediaService](./Get-AzureRmMediaService.md)

[Neu – AzureRmMediaService](./New-AzureRmMediaService.md)

[Remove-AzureRmMediaService](./Remove-AzureRmMediaService.md)

[Satz-AzureRmMediaService](./Set-AzureRmMediaService.md)


