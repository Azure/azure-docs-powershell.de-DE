---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
ms.openlocfilehash: 5cb4a57994ad8b15048bfc22dadefbbee031aaf7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293039"
---
# Remove-AzVpnClientRootCertificate

## SYNOPSIS
Entfernt ein vorhandenes VPN-Client-Stammzertifikat.

## SYNTAX

```
Remove-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Remove-AzVpnClientRootCertificate"** entfernt das angegebene Stammzertifikat aus einem virtuellen Netzwerkgateway.
Stammzertifikate sind X.509-Zertifikate, die Ihre Stammzertifizierungsstelle identifizieren: Alle anderen auf dem Gateway verwendeten Zertifikate vertrauen dem Stammzertifikat.
Wenn Sie einen Stammzertifikatcomputer entfernen, der das Zertifikat für Authentifizierungszwecke verwendet, kann keine Verbindung mehr mit dem Gateway hergestellt werden.
Wenn Sie **Remove-AzVpnClientRootCertificate** verwenden, müssen Sie sowohl den Zertifikatnamen als auch eine Textdarstellung der Zertifikatdaten eingeben.
Weitere Informationen zur Textdarstellung eines Zertifikats finden Sie in der *Beschreibung des PublicCertData-Parameters.*

## BEISPIELE

### Beispiel 1: Entfernen eines Clientstammzertifikats von einem virtuellen Netzwerkgateway
```powershell
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoRootCertificate"
```

In diesem Beispiel wird ein Clientstammzertifikat namens "ContosoRootCertificate" aus dem virtuellen Netzwerkgateway "ContosoVirtualGateway" entfernt.
Der erste Befehl verwendet das **Get-Content-Cmdlet,** um eine zuvor exportierte Textdarstellung des Zertifikats zu erhalten. diese Textdarstellung wird in einer Variablen mit dem Namen $Text.
Der zweite Befehl verwendet dann eine "for"-Schleife, um den $Text mit Ausnahme der ersten und der letzten Zeile, zu extrahieren.
Dieser extrahierte Text wird in einer Variablen mit dem Namen $CertificateText.
Der dritte Befehl verwendet die in der Variablen "$CertificateText" gespeicherten Informationen zusammen mit dem **Cmdlet "Remove-AzVpnClientRootCertificate",** um das Zertifikat aus dem Gateway zu entfernen.

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
Gibt die Textdarstellung des Stammzertifikats an, das entfernt werden soll.
Um die Textdarstellung zu erhalten, exportieren Sie das Zertifikat im CER-Format (mit Base64)-Codierung, und öffnen Sie dann die resultierende Datei in einem Text-Editor.
Die Ausgabe sollte ähnlich wie die folgende angezeigt werden (beachten Sie, dass die tatsächliche Ausgabe viel mehr Textzeilen enthalten wird als im hier gezeigten abgekürzten Beispiel): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- Die PublicCertData-Datei besteht aus allen Zeilen zwischen der ersten Zeile (----- BEGIN CERTIFICATE -----) und der letzten Zeile (----- END CERTIFICATE -----) in der Datei.
Sie können publicCertData mit Windows PowerShell-Befehlen wie dem folgenden abrufen: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text \[ $i \] }

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
Gibt den Namen des virtuellen Netzwerkgateways an, von dem das Zertifikat entfernt wird.

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
Gibt den Namen des Clientstammzertifikats an, das von diesem Cmdlet entfernt wird.

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

### System.Boolean

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Add-AzVpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[New-AzVpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)


