---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 85a35fe4c6b988ce6f5320d308582fb722cc5791
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924664"
---
# New-AzVpnClientRevokedCertificate

## SYNOPSIS
Erstellt ein neues VPN-Clientsperrzertifikat.

## SYNTAX

```
New-AzVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet New-AzVpnClientRevokedCertificate** erstellt ein neues VPN(Virtual Private Network)-Clientsperrzertifikat für die Verwendung auf einem Gateway für virtuelle Netzwerke.
Clientperrzertifikate verhindern, dass Clientcomputer das angegebene Zertifikat für die Authentifizierung verwenden.
Dieses Cmdlet erstellt ein eigenständiges Zertifikat, das keinem virtuellen Gateway zugewiesen ist.
Stattdessen wird das von **New-AzVpnClientRevokedCertificate** erstellte Zertifikat in Verbindung mit dem cmdlet New-AzVirtualNetworkGateway verwendet, wenn ein neues Gateway erstellt wird.
Angenommen, Sie erstellen ein neues Zertifikat und speichern es in einer Variablen namens $Certificate.
Sie können dieses Zertifikatobjekt dann verwenden, wenn Sie ein neues virtuelles Gateway erstellen.
Zum Beispiel `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`
Weitere Informationen finden Sie in der Dokumentation zum New-AzVirtualNetworkGateway Cmdlet.

## BEISPIELE

### Beispiel 1: Erstellen eines neuen vom Client widerrufenen Zertifikats
```
PS C:\>$Certificate = New-AzVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

Mit diesem Befehl wird ein neues vom Client widerrufenes Zertifikat erstellt und das Zertifikatobjekt in einer Variablen namens $Certificate.
Diese Variable kann dann vom **Cmdlet New-AzVirtualNetworkGateway** verwendet werden, um das Zertifikat zu einem neuen Gateway für virtuelle Netzwerke hinzuzufügen.

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

### -Name
Gibt einen eindeutigen Namen für das neue Clientperrzertifikat an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Thumbprint
Gibt den eindeutigen Bezeichner des hinzugefügten Zertifikats an.
Sie können Fingerabdruckinformationen für Ihre Zertifikate mithilfe eines Befehls zurückgeben, der Windows PowerShell wie der folgenden ähnelt: `Get-ChildItem -Path Cert:\LocalMachine\Root`
Der vorhergehende Befehl gibt Informationen für alle Zertifikate des lokalen Computers zurück, die im Stammzertifikatspeicher gefunden wurden.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate

## NOTIZEN

## VERWANDTE LINKS

[Add-AzVpnClientRevokedCertificate](./Add-AzVpnClientRevokedCertificate.md)

[Get-AzVpnClientRevokedCertificate](./Get-AzVpnClientRevokedCertificate.md)

[Remove-AzVpnClientRevokedCertificate](./Remove-AzVpnClientRevokedCertificate.md)


