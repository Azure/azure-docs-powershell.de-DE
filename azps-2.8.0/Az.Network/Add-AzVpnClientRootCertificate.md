---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
ms.openlocfilehash: 1a38c55757f96b99a6801452f490f0fc4240fde1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822471"
---
# Add-AzVpnClientRootCertificate

## Synopsis
Fügt ein VPN-Client-Stammzertifikat hinzu.

## Syntax

```
Add-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Add-AzVpnClientRootCertificate** wird ein Stammzertifikat zu einem virtuellen Netzwerkgateway hinzugefügt.
Stammzertifikate sind X. 509-Zertifikate, die Ihre Stammzertifizierungsstelle identifizieren.
Im Design Vertrauen alle auf dem Gateway verwendeten Zertifikate dem Stammzertifikat.
Dieses Cmdlet weist ein vorhandenes Zertifikat als Gateway-Stammzertifikat zu.
Wenn Sie nicht über ein X. 509-Zertifikat verfügen, können Sie ein Zertifikat über Ihre Infrastruktur öffentlicher Schlüssel generieren oder einen Zertifikat Generator wie makecert.exe verwenden.
Wenn Sie ein Stammzertifikat hinzufügen möchten, müssen Sie den Zertifikatnamen angeben und eine nur-Text-Darstellung des Zertifikats bereitstellen (Weitere Informationen finden Sie *im PublicCertData* -Parameter).
Azure ermöglicht Ihnen, einem Gateway mehr als ein Stammzertifikat zuzuweisen.
Mehrere Stammzertifikate werden häufig von Organisationen bereitgestellt, die Benutzer aus mehr als einem Unternehmen einbeziehen.

## Beispiele

### Beispiel 1: Hinzufügen eines Client Stammzertifikats zu einem virtuellen Gateway
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

In diesem Beispiel wird ein Client-Stammzertifikat zu einem virtuellen Gateway mit dem Namen ContosoVirtualGateway hinzugefügt.
Der erste Befehl verwendet das Cmdlet " **Get-Content** ", um eine zuvor exportierte Textdarstellung des Stammzertifikats abzurufen, und speichert diese Textdaten als die Variable mit dem Namen "$Text".
Der zweite Befehl verwendet dann eine for-Schleife, um den gesamten Text mit Ausnahme der ersten Zeile und der letzten Zeile zu extrahieren.
Der extrahierte Text wird in einer Variablen mit dem Namen $CertificateText gespeichert.
Der dritte Befehl verwendet dann den in $CertificateText gespeicherten Text mit dem Cmdlet **Add-AzVpnClientRootCertificate** , um das Stammzertifikat zum Gateway hinzuzufügen.

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
Gibt die Textdarstellung des Stammzertifikats an, das hinzugefügt werden soll.
Um die Textdarstellung zu erhalten, exportieren Sie Ihr Zertifikat im CER-Format (mit Base64-Codierung), und öffnen Sie dann die resultierende Datei in einem Text-Editor.
Wenn Sie dies tun, wird die Ausgabe ähnlich wie in der folgenden Abbildung angezeigt (Beachten Sie, dass die tatsächliche Ausgabe viele weitere Textzeilen enthält, als das hier gezeigte verkürzte Beispiel):-----Zertifikat-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----Ende des Zertifikats-----der PublicCertData besteht aus allen Zeilen zwischen der ersten Zeile (-----BEGIN Certificate-----) und der letzten Zeile (-----End Certificate-----) in der Datei.
Sie können diese Daten mithilfe von Windows PowerShell-Befehlen abrufen, die wie folgt aussehen: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
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
Gibt den Namen des virtuellen Netzwerkgateways an, auf dem das Zertifikat hinzugefügt wird.

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
Gibt den Namen des Client-Stammzertifikats an, das von diesem Cmdlet hinzugefügt wird.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate

## Notizen

## Verwandte Links

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[Neu – AzVpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)

[Remove-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


