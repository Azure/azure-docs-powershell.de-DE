---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: ba9715b6f29cd45ba25f8b2d2ab85ba0d7ef7979
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378942"
---
# New-AzVpnClientRevokedCertificate

## SYNOPSIS
Erstellt ein neues ZERTIFIKAT für die Clientsperrung von VPN.

## SYNTAX

```
New-AzVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "New-AzVpnClientRevokedCertificate"** erstellt ein neues VPN (Virtual Private Network)-Clientsperrzertifikat zur Verwendung auf einem virtuellen Netzwerkgateway.
Clientsperrzertifikate verhindern, dass Clientcomputer das angegebene Zertifikat für die Authentifizierung verwenden.
Dieses Cmdlet erstellt ein eigenständiges Zertifikat, das keinem virtuellen Gateway zugewiesen ist.
Stattdessen wird das mit **"New-AzVpnClientRevokedCertificate"** erstellte Zertifikat beim Erstellen eines neuen Gateways in Verbindung mit dem Cmdlet New-AzVirtualNetworkGateway verwendet.
Angenommen, Sie erstellen ein neues Zertifikat und speichern es in einer Variablen namens $Certificate.
Sie können dieses Zertifikatobjekt dann verwenden, wenn Sie ein neues virtuelles Gateway erstellen.
Zum Beispiel `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`
Weitere Informationen finden Sie in der Dokumentation zum New-AzVirtualNetworkGateway Cmdlet.

## BEISPIELE

### Beispiel 1: Erstellen eines neuen Zertifikats mit Client widerrufen
```
PS C:\>$Certificate = New-AzVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

Dieser Befehl erstellt ein neues Zertifikat mit Client widerrufen und speichert das Zertifikatobjekt in einer Variablen namens $Certificate.
Diese Variable kann dann vom **Cmdlet "New-AzVirtualNetworkGateway"** verwendet werden, um das Zertifikat einem neuen virtuellen Netzwerkgateway hinzuzufügen.

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

### -Name
Gibt einen eindeutigen Namen für das neue Zertifikat für die Clientsperrung an.

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
Sie können Fingerabdrückinformationen für Ihre Zertifikate mithilfe eines Windows PowerShell ähnlich dem folgenden zurückgeben: `Get-ChildItem -Path Cert:\LocalMachine\Root`
Der vorherige Befehl gibt Informationen für alle Zertifikate des lokalen Computers zurück, die im Stammzertifikatspeicher gefunden wurden.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Add-AzVpnClientRevokedCertificate](./Add-AzVpnClientRevokedCertificate.md)

[Get-AzVpnClientRevokedCertificate](./Get-AzVpnClientRevokedCertificate.md)

[Remove-AzVpnClientRevokedCertificate](./Remove-AzVpnClientRevokedCertificate.md)


