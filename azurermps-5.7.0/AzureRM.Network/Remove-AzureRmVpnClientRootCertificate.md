---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: b86637618b0ef6a2ed337a48d5bdebf8888fad2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505785"
---
# Remove-AzureRmVpnClientRootCertificate

## Synopsis
Entfernt ein vorhandenes VPN-Client-Stammzertifikat.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Remove-AzureRmVpnClientRootCertificate -VpnClientRootCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureRmVpnClientRootCertificate** entfernt das angegebene Stammzertifikat von einem virtuellen Netzwerkgateway.
Stammzertifikate sind X. 509-Zertifikate, die Ihre Stammzertifizierungsstelle identifizieren: alle anderen auf dem Gateway verwendeten Zertifikate vertrauen dem Stammzertifikat.
Wenn Sie ein Stammzertifikat Computer entfernen, die das Zertifikat für Authentifizierungszwecke verwenden, kann keine Verbindung mehr mit dem Gateway hergestellt werden.

Wenn Sie **Remove-AzureRmVpnClientRootCertificate** verwenden, müssen Sie sowohl den Zertifikatsnamen als auch eine Textdarstellung der Zertifikatsdaten angeben.
Weitere Informationen zur Textdarstellung eines Zertifikats finden Sie in der Beschreibung des *PublicCertData* -Parameters.

## Beispiele

### Beispiel 1: Entfernen eines Client Stammzertifikats von einem virtuellen Netzwerkgateway
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway"-VpnClientRootCertificateName "ContosoRootCertificate"
```

In diesem Beispiel wird ein Client-Stammzertifikat namens ContosoRootCertificate aus dem virtuellen Netzwerkgateway ContosoVirtualGateway entfernt.

Der erste Befehl verwendet das Cmdlet " **Get-Content** ", um eine zuvor exportierte Textdarstellung des Zertifikats abzurufen. Diese Textdarstellung wird in einer Variablen mit dem Namen $Text gespeichert.

Der zweite Befehl verwendet dann eine for-Schleife, um den gesamten Text in $Text mit Ausnahme der ersten Zeile und der letzten Zeile zu extrahieren.
Dieser extrahierte Text wird in einer Variablen mit dem Namen $CertificateText gespeichert.

Der dritte Befehl verwendet die in der $CertificateText-Variablen gespeicherten Informationen zusammen mit dem Cmdlet **Remove-AzureRmVpnClientRootCertificate** , um das Zertifikat vom Gateway zu entfernen.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicCertData
Gibt die Textdarstellung des zu entfernende Stammzertifikats an.
Um die Textdarstellung zu erhalten, exportieren Sie Ihr Zertifikat im CER-Format (mit Base64-Codierung), und öffnen Sie dann die resultierende Datei in einem Text-Editor.
Die Ausgabe sollte ähnlich der folgenden angezeigt werden (Beachten Sie, dass die tatsächliche Ausgabe viele weitere Textzeilen enthält, als das hier gezeigte abgekürzte Beispiel):

-----Zertifikat-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----Abschlusszertifikat starten-----

Der PublicCertData besteht aus allen Zeilen zwischen der ersten Zeile (-----BEGIN Certificate-----) und der letzten Zeile (-----Ende des Zertifikats-----) in der Datei.
Sie können die PublicCertData mit Windows PowerShell-Befehlen abrufen, die wie folgt aussehen:

$Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = für ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }

```yaml
Type: String
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
Type: String
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
Type: String
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
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

## Notizen

## Verwandte Links

[Add-AzureRmVpnClientRootCertificate](./Add-AzureRmVpnClientRootCertificate.md)

[Get-AzureRmVpnClientRootCertificate](./Get-AzureRmVpnClientRootCertificate.md)

[Neu – AzureRmVpnClientRootCertificate](./New-AzureRmVpnClientRootCertificate.md)


