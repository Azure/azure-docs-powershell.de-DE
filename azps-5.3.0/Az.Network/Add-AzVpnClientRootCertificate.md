---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
ms.openlocfilehash: efb8640f765468432a2927f865ce9f67c7b9164f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467404"
---
# Add-AzVpnClientRootCertificate

## SYNOPSIS
Fügt ein Stammzertifikat für den VPN-Client hinzu.

## SYNTAX

```
Add-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Add-AzVpnClientRootCertificate"** fügt einem virtuellen Netzwerkgateway ein Stammzertifikat hinzu.
Stammzertifikate sind X.509-Zertifikate, die Ihre Stammzertifizierungsstelle identifizieren.
Standardmäßig vertrauen alle auf dem Gateway verwendeten Zertifikate dem Stammzertifikat.
Dieses Cmdlet weist ein vorhandenes Zertifikat als Gatewaystammzertifikat zu.
Wenn kein X.509-Zertifikat verfügbar ist, können Sie über Ihre Public Key-Infrastruktur ein Zertifikat generieren oder einen Zertifikatgenerator wie makecert.exe.
Zum Hinzufügen eines Stammzertifikats müssen Sie den Zertifikatnamen angeben und eine Nur-Text-Darstellung des Zertifikats bereitstellen (weitere Informationen finden Sie im *Parameter "PublicCertData").*
Mit Azure können Sie einem Gateway mehrere Stammzertifikate zuweisen.
Mehrere Stammzertifikate werden häufig von Organisationen bereitgestellt, die Benutzer aus mehreren Unternehmen umfassen.

## BEISPIELE

### Beispiel 1: Hinzufügen eines Clientstammzertifikats zu einem virtuellen Gateway
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

In diesem Beispiel wird einem virtuellen Gateway namens "ContosoVirtualGateway" ein Clientstammzertifikat hinzufügt.
Der erste Befehl verwendet das **Get-Content-Cmdlet,** um eine zuvor exportierte Textdarstellung des Stammzertifikats zu erhalten, und speichert diese Textdaten, die die Variable namens "$Text.
Der zweite Befehl verwendet dann eine for-Schleife, um den ganzen Text mit Ausnahme der ersten und letzten Zeile zu extrahieren.
Der extrahierte Text wird in einer Variablen mit dem Namen $CertificateText.
Der dritte Befehl verwendet dann den Text, der in $CertificateText mit dem **Cmdlet "Add-AzVpnClientRootCertificate"** gespeichert ist, um das Stammzertifikat zum Gateway hinzuzufügen.

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

### -PublicCertData
Gibt die Textdarstellung des Stammzertifikats an, das hinzugefügt werden soll.
Um die Textdarstellung zu erhalten, exportieren Sie das Zertifikat im CER-Format (mit Base64-Codierung), und öffnen Sie dann die resultierende Datei in einem Text-Editor.
Dabei wird eine Ausgabe ähnlich der folgenden angezeigt (beachten Sie, dass die tatsächliche Ausgabe viel mehr Textzeilen enthält als im hier gezeigten abgekürzten Beispiel): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- Die PublicCertData-Datei besteht aus allen Zeilen zwischen der ersten Zeile (----- BEGIN CERTIFICATE -----) und der letzten Zeile (----- END CERTIFICATE -----) in der Datei.
Sie können diese Daten mithilfe von Windows PowerShell wie dem folgenden abrufen: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
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
Ressourcengruppen kategorisieren Elemente, um die Bestandsverwaltung und die allgemeine Verwaltung von Azure zu vereinfachen.

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
Gibt den Namen des virtuellen Netzwerkgateways an, dem das Zertifikat hinzugefügt wird.

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
Gibt den Namen des Clientstammzertifikats an, das von diesem Cmdlet hinzufügt wird.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[New-AzVpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)

[Remove-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


