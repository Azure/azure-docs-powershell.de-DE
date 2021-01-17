---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
ms.openlocfilehash: 8eba8d26bcac5de16be3e2cda5e8ca80356aea11
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372544"
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
Das **Cmdlet "Get-AzVpnClientPackage"** ruft Informationen zu den VPN-Clientpaketen ab, die über ein virtuelles Netzwerkgateway zur Verfügung stehen.
Clientpakete enthalten Konfigurationsdaten, die einem Clientcomputer das Herstellen einer #A0 mit einem virtuellen #A1 ermöglichen. client computers must have the correct configuration package installed to make a VPN connection.
Basierend auf der Version des Clientcomputers von Windows (z. B. Windows 7 oder Windows 10) und der Prozessorarchitektur des Clientcomputers (AMD64 oder x86) stehen verschiedene Konfigurationspakete zur Verfügung.
Sie müssen den Architekturtyp angeben, wenn **Sie "Get-AzVpnClientPackage" ausführen.**

## BEISPIELE

### Beispiel 1: Informationen zu einem CLIENTpaket für die Prozessorarchitektur von VPN
```
PS C:\>Get-AzVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

Dieser Befehl ruft Informationen zu den AMD64-VPN-Clientpaketen ab, die auf dem virtuellen Netzwerkgateway namens "ContosoVirtualNetworkGateway" gespeichert sind.
Um Informationen zu den x86-Clientpaketen zu erhalten, legen Sie den Wert des Parameters *"ProcessorArchitecture"* auf "x86" festgelegt.

## PARAMETERS

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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
Gibt den Typ der CPU-Architektur an, auf den das Clientpaket ausgelegt ist.
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
Gibt den Namen der Ressourcengruppe an, der das virtuelle Netzwerkgateway zugewiesen ist.
Ressourcengruppen kategorisieren Elemente, um die Bestandsverwaltung und die allgemeine Verwaltung von Azure zu vereinfachen.

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
Gibt den Namen des virtuellen Netzwerkgateways an, in dem die Clientpaketinformationen gespeichert sind.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

## AUSGABEN

### System.String

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Resize-AzVirtualNetworkGateway](./Resize-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGatewayVpnClientConfig](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)


