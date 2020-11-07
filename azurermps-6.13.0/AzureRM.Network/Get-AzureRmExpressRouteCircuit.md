---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 969d7c5f55d210cdff74066d08af50bbcc47181e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663133"
---
# Get-AzureRmExpressRouteCircuit

## Synopsis
Ruft eine Azure Express Route-Schaltkreis aus Azure ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmExpressRouteCircuit** " wird verwendet, um ein Express Route-Schaltkreis Objekt aus Ihrem Abonnement abzurufen. Das zurückgegebene Circuit-Objekt kann als Eingabe für andere Cmdlets verwendet werden, die auf Express Route-Schaltkreisen ausgeführt werden.

## Beispiele

### Beispiel 1: Abrufen des zu löschenden Express Route-Schaltkreises
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## Parameter

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

### -Name
Der Name des Express Route-Schaltkreises.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe, die den Express Route-Schaltkreis enthält.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit

## Notizen

## Verwandte Links

[Verschieben-AzureRmExpressRouteCircuit](Move-AzureRmExpressRouteCircuit.md)

[Neu – AzureRmExpressRouteCircuit](New-AzureRmExpressRouteCircuit.md)

[Remove-AzureRmExpressRouteCircuit](Remove-AzureRmExpressRouteCircuit.md)

[Satz-AzureRmExpressRouteCircuit](Set-AzureRmExpressRouteCircuit.md)
