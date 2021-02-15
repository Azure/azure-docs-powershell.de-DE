---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: 379ba58abe2d7a697c7dca5bdb31bc222159d367
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159065"
---
# New-AzVpnClientRootCertificate

## SYNOPSIS
Erstellt ein neues VPN-Clientstammzertifikat.

## SYNTAX

```
New-AzVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "New-AzVpnClientRootCertificate"** erstellt ein neues VPN-Stammzertifikat zur Verwendung auf einem virtuellen Netzwerkgateway.
Stammzertifikate sind X.509-Zertifikate, die Ihre Stammzertifizierungsstelle identifizieren: Alle anderen vom Gateway verwendeten Zertifikate vertrauen dem Stammzertifikat.
Dieses Cmdlet erstellt ein eigenständiges Zertifikat, das keinem virtuellen Gateway zugewiesen ist.
Stattdessen wird das von **"New-AzVpnClientRootCertificate"** erstellte Zertifikat beim Erstellen eines neuen Gateways in Verbindung mit dem cmdlet New-AzVirtualNetworkGateway "New-AzVirtualNetworkGateway" verwendet.
Angenommen, Sie erstellen ein neues Zertifikat und speichern es in einer Variablen namens $Certificate.
Sie können dieses Zertifikatobjekt dann verwenden, wenn Sie ein neues virtuelles Gateway erstellen.
Zum Beispiel `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`
Weitere Informationen finden Sie in der Dokumentation zum New-AzVirtualNetworkGateway Cmdlet.

## BEISPIELE

### Beispiel 1: Erstellen eines Clientstammzertifikats
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

In diesem Beispiel wird ein Clientstammzertifikat erstellt und das Zertifikatobjekt in einer Variablen namens "$Certificate.
Diese Variable kann dann vom **Cmdlet "New-AzVirtualNetworkGateway"** verwendet werden, um einem neuen virtuellen Netzwerkgateway ein Stammzertifikat hinzuzufügen.
Der erste Befehl verwendet das **Get-Content-Cmdlet,** um eine zuvor exportierte Textdarstellung des Stammzertifikats zu erhalten. text data is stored in a variable named $Text.
Der zweite Befehl verwendet dann eine for-Schleife, um den ganzen Text mit Ausnahme der ersten und letzten Zeile zu extrahieren und den extrahierten Text in einer Variablen namens "$CertificateText.
Der dritte Befehl verwendet das **Cmdlet "New-AzVpnClientRootCertificate"** zum Erstellen des Zertifikats und speichert das erstellte Objekt in einer Variablen namens $Certificate.

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
Gibt einen Namen für das neue Clientstammzertifikat an.

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

### -PublicCertData
Gibt eine Textdarstellung des Stammzertifikats an, das hinzugefügt werden soll.
Um die Textdarstellung zu erhalten, exportieren Sie das Zertifikat im CER-Format (mit Base64-Codierung), und öffnen Sie dann die resultierende Datei in einem Text-Editor.
Die Ausgabe sollte ähnlich wie diese angezeigt werden (beachten Sie, dass die tatsächliche Ausgabe viel mehr Textzeilen enthalten wird als im hier gezeigten abgekürzten Beispiel): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- Die PublicCertData-Datei besteht aus allen Zeilen zwischen der ersten Zeile (----- BEGIN CERTIFICATE -----) und der letzten Zeile (----- END CERTIFICATE -----) in der Datei.
Sie können die PublicCertData mit Windows PowerShell-Befehlen wie dem folgenden abrufen: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text \[ $i \] }

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Add-AzVpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[Remove-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


