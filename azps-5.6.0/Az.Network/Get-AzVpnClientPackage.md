---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
ms.openlocfilehash: 69fcd4ee3cdcd2692c242a366c7d88545f9641b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945929"
---
# Get-AzVpnClientPackage

## SYNOPSIS
Ruft Informationen zu einem VPN-Clientpaket ab.

## SYNTAX

```
Get-AzVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzVpnClientPackage-Cmdlet** ruft Informationen zu den VPN-Clientpaketen ab, die über ein Gateway für virtuelle Netzwerke verfügbar sind.
Clientpakete enthalten Konfigurationsdaten, die es einem Clientcomputer ermöglichen, eine #A0 mit einem virtuellen Azure-Netzwerk herzustellen. Auf Clientcomputern muss das richtige Konfigurationspaket installiert sein, um eine VPN-Verbindung herstellen zu können.
Unterschiedliche Konfigurationspakete sind basierend auf der Windows-Version des Clientcomputers (z. B. Windows 7 oder Windows 10) und der Prozessorarchitektur des Clientcomputers (AMD64 oder x86) verfügbar.
Sie müssen den Architekturtyp angeben, wenn **Sie Get-AzVpnClientPackage ausführen.**

## BEISPIELE

### Beispiel 1: Informationen zu einem VPN-Clientpaket der Prozessorarchitektur
```
PS C:\>Get-AzVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

Dieser Befehl ruft Informationen zu den AMD64-VPN-Clientpaketen ab, die auf dem Virtuellen Netzwerkgateway namens ContosoVirtualNetworkGateway gespeichert sind.
Um Informationen zu den x86-Clientpaketen zu erhalten, legen Sie den Wert des *Parameters ProcessorArchitecture* auf x86.

## PARAMETER

### -DefaultProfile
Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -ProcessorArchitecture
Gibt den Typ der CPU-Architektur an, für den das Clientpaket entwickelt wurde.
Gültige Werte sind Amd64 und X86.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, der das Virtuelle Netzwerkgateway zugewiesen ist.
Ressourcengruppen kategorisieren Elemente, um die Bestandsverwaltung und die allgemeine Azure-Verwaltung zu vereinfachen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkGatewayName
Gibt den Namen des Virtuellen Netzwerkgateways an, in dem die Clientpaketinformationen gespeichert sind.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### System.String

## AUSGABEN

### System.String

## NOTIZEN

## VERWANDTE LINKS

[Resize-AzVirtualNetworkGateway](./Resize-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGatewayVpnClientConfig](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)


