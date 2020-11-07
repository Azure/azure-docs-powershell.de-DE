---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortsLocation.md
ms.openlocfilehash: 5d077991e42da0709019df1dccdd83f03659ca49
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664828"
---
# Get-AzureRmExpressRoutePortsLocation

## Synopsis
Ruft die Speicherorte ab, an denen ExpressRoutePort-Ressourcen verfügbar sind.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmExpressRoutePortsLocation** " wird verwendet, um die Speicherorte abzurufen, an denen ExpressRoutePort-Ressourcen verfügbar sind. Bei Angabe einer bestimmten Position als Eingabe zeigt das Cmdlet die Details dieses Speicherorts an, also eine Liste der verfügbaren Bandbreiten an diesem Speicherort.


## Beispiele

### Beispiel 1
```powershell
PS C:\> Get-AzureRmExpressRoutePortsLocation
```

Listet die Speicherorte auf, an denen ExpressRoutePort-Ressourcen verfügbar sind.

### Beispiel 2
```powershell
PS C:\> Get-AzureRmExpressRoutePortsLocation -LocationName $loc
```

Listet die ExpressRoutePort-Bandbreiten auf, die an Standort $Loc verfügbar sind.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### -Standortname
Der Name des Standorts.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSExpressRoutePortsLocation

## Notizen

## Verwandte Links
