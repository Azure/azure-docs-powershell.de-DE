---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
ms.openlocfilehash: 38a6abb631a77d41e38026edd3bef5abe9c70c01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932443"
---
# Add-AzVpnClientRootCertificate

## SYNOPSIS
Fügt ein VPN-Clientstammzertifikat hinzu.

## SYNTAX

```
Add-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Add-AzVpnClientRootCertificate-Cmdlet** fügt einem Gateway für virtuelle Netzwerke ein Stammzertifikat hinzu.
Stammzertifikate sind X.509-Zertifikate, die Ihre Stammzertifizierungsstelle identifizieren.
Standardmäßig vertrauen alle zertifikate, die im Gateway verwendet werden, dem Stammzertifikat.
Dieses Cmdlet weist ein vorhandenes Zertifikat als Gatewaystammzertifikat zu.
Wenn kein X.509-Zertifikat verfügbar ist, können Sie ein Zertifikat über Ihre Infrastruktur für öffentliche Schlüssel generieren oder einen Zertifikatgenerator wie makecert.exe.
Zum Hinzufügen eines Stammzertifikats müssen Sie den Zertifikatnamen angeben und eine Textdarstellung des Zertifikats bereitstellen (weitere Informationen finden Sie im *Parameter PublicCertData).*
Azure ermöglicht es Ihnen, einem Gateway mehr als ein Stammzertifikat zuzuordnen.
Mehrere Stammzertifikate werden häufig von Organisationen bereitgestellt, die Benutzer aus mehreren Unternehmen umfassen.

## BEISPIELE

### Beispiel 1: Hinzufügen eines Clientstammzertifikats zu einem virtuellen Gateway
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

In diesem Beispiel wird einem virtuellen Gateway namens ContosoVirtualGateway ein Clientstammzertifikat hinzufügt.
Der erste Befehl verwendet das **Get-Content-Cmdlet,** um eine zuvor exportierte Textdarstellung des Stammzertifikats zu erhalten, und speichert diese Textdaten, die die Variable namens $Text.
Der zweite Befehl verwendet dann eine for-Schleife, um den ganzen Text mit Ausnahme der ersten und der letzten Zeile zu extrahieren.
Der extrahierte Text wird in einer Variablen mit dem Namen $CertificateText.
Der dritte Befehl verwendet dann den in $CertificateText mit dem **Add-AzVpnClientRootCertificate-Cmdlet** gespeicherten Text, um das Stammzertifikat zum Gateway hinzuzufügen.

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

### -PublicCertData
Gibt die Textdarstellung des Stammzertifikats an, das hinzugefügt werden soll.
Um die Textdarstellung zu erhalten, exportieren Sie Ihr Zertifikat im CER-Format (unter Verwendung der Base64-Codierung), und öffnen Sie dann die resultierende Datei in einem Text-Editor.
In diesem Beispiel wird eine ähnliche Ausgabe wie die folgende angezeigt (beachten Sie, dass die tatsächliche Ausgabe viel mehr Textzeilen enthält als das hier gezeigte abgekürzte Beispiel): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- Das PublicCertData besteht aus allen Zeilen zwischen der ersten Zeile (----- BEGIN CERTIFICATE -----) und der letzten Zeile (----- END CERTIFICATE -----) in der Datei.
Sie können diese Daten mithilfe der folgenden Windows PowerShell abrufen: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, der das Stammzertifikat zugewiesen ist.
Ressourcengruppen kategorisieren Elemente, um die Bestandsverwaltung und die allgemeine Azure-Verwaltung zu vereinfachen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGatewayName
Gibt den Namen des Virtuellen Netzwerkgateways an, in dem das Zertifikat hinzugefügt wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VpnClientRootCertificateName
Gibt den Namen des Clientstammzertifikats an, das von diesem Cmdlet addiert wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate

## NOTIZEN

## VERWANDTE LINKS

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[New-AzVpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)

[Remove-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


