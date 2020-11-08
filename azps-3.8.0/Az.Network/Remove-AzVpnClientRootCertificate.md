---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
ms.openlocfilehash: 3288573719edac1f04b40ed624820397b4beebcd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004156"
---
# Remove-AzVpnClientRootCertificate

## Synopsis
Entfernt ein vorhandenes VPN-Client-Stammzertifikat.

## Syntax

```
Remove-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzVpnClientRootCertificate** entfernt das angegebene Stammzertifikat von einem virtuellen Netzwerkgateway.
Stammzertifikate sind X. 509-Zertifikate, die Ihre Stammzertifizierungsstelle identifizieren: alle anderen auf dem Gateway verwendeten Zertifikate vertrauen dem Stammzertifikat.
Wenn Sie ein Stammzertifikat Computer entfernen, die das Zertifikat für Authentifizierungszwecke verwenden, kann keine Verbindung mehr mit dem Gateway hergestellt werden.
Wenn Sie **Remove-AzVpnClientRootCertificate** verwenden, müssen Sie sowohl den Zertifikatsnamen als auch eine Textdarstellung der Zertifikatsdaten angeben.
Weitere Informationen zur Textdarstellung eines Zertifikats finden Sie in der Beschreibung des *PublicCertData* -Parameters.

## Beispiele

### Beispiel 1: Entfernen eines Client Stammzertifikats von einem virtuellen Netzwerkgateway
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway"-VpnClientRootCertificateName "ContosoRootCertificate"
```

In diesem Beispiel wird ein Client-Stammzertifikat namens ContosoRootCertificate aus dem virtuellen Netzwerkgateway ContosoVirtualGateway entfernt.
Der erste Befehl verwendet das Cmdlet " **Get-Content** ", um eine zuvor exportierte Textdarstellung des Zertifikats abzurufen. Diese Textdarstellung wird in einer Variablen mit dem Namen $Text gespeichert.
Der zweite Befehl verwendet dann eine for-Schleife, um den gesamten Text in $Text mit Ausnahme der ersten Zeile und der letzten Zeile zu extrahieren.
Dieser extrahierte Text wird in einer Variablen mit dem Namen $CertificateText gespeichert.
Der dritte Befehl verwendet die in der $CertificateText-Variablen gespeicherten Informationen zusammen mit dem Cmdlet **Remove-AzVpnClientRootCertificate** , um das Zertifikat vom Gateway zu entfernen.

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

### -PublicCertData
Gibt die Textdarstellung des zu entfernende Stammzertifikats an.
Um die Textdarstellung zu erhalten, exportieren Sie Ihr Zertifikat im CER-Format (mit Base64-Codierung), und öffnen Sie dann die resultierende Datei in einem Text-Editor.
Es sollte eine Ausgabe ähnlich der folgenden angezeigt werden (Beachten Sie, dass die tatsächliche Ausgabe viele weitere Textzeilen enthält, als das hier gezeigte verkürzte Beispiel):-----Zertifikat-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----Ende des Zertifikats-----der PublicCertData besteht aus allen Zeilen zwischen der ersten Zeile (-----BEGIN Certificate-----) und der letzten Zeile (-----Ende des Zertifikats-----) in der Datei.
Sie können die PublicCertData mit Windows PowerShell-Befehlen abrufen, die wie folgt aussehen: $Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = für ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }

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
Gibt den Namen der Ressourcengruppe an, der das virtuelle Netzwerkgateway zugewiesen ist.
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
Gibt den Namen des virtuellen Netzwerkgateways an, aus dem das Zertifikat entfernt wurde.

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
Gibt den Namen des Client Stammzertifikats an, das vom Cmdlet entfernt wird.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### System. Boolean

## Notizen

## Verwandte Links

[Add-AzVpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[Neu – AzVpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)


