---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: 918ef18717cb09bad28ee10b91f635181dd5b3cb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003560"
---
# Get-AzExpressRoutePortsLocation

## Synopsis
Ruft die Speicherorte ab, an denen ExpressRoutePort-Ressourcen verfügbar sind.

## Syntax

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzExpressRoutePortsLocation** " wird verwendet, um die Speicherorte abzurufen, an denen ExpressRoutePort-Ressourcen verfügbar sind. Bei Angabe einer bestimmten Position als Eingabe zeigt das Cmdlet die Details dieses Speicherorts an, also eine Liste der verfügbaren Bandbreiten an diesem Speicherort.

## Beispiele

### Beispiel 1
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

Listet die Speicherorte auf, an denen ExpressRoutePort-Ressourcen verfügbar sind.

### Beispiel 2
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

Listet die ExpressRoutePort-Bandbreiten auf, die an Standort $Loc verfügbar sind.

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

### -Standortname
Der Name des Standorts.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSExpressRoutePortsLocation

## Notizen

## Verwandte Links
