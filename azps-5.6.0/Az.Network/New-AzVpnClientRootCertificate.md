---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: 866a3b9ac28de57a71fce5fb84b2fa1144d0ff8e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924659"
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
Das **Cmdlet New-AzVpnClientRootCertificate** erstellt ein neues VPN-Stammzertifikat für die Verwendung auf einem Gateway für virtuelle Netzwerke.
Stammzertifikate sind X.509-Zertifikate, die Ihre Stammzertifizierungsstelle identifizieren: Alle anderen zertifikate, die im Gateway verwendet werden, vertrauen dem Stammzertifikat.
Dieses Cmdlet erstellt ein eigenständiges Zertifikat, das keinem virtuellen Gateway zugewiesen ist.
Stattdessen wird das von **New-AzVpnClientRootCertificate** erstellte Zertifikat beim Erstellen eines neuen Gateways in Verbindung mit dem cmdlet New-AzVirtualNetworkGateway verwendet.
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

In diesem Beispiel wird ein Clientstammzertifikat erstellt und das Zertifikatobjekt in einer Variablen namens $Certificate.
Diese Variable kann dann vom **Cmdlet New-AzVirtualNetworkGateway** verwendet werden, um einem neuen virtuellen Netzwerkgateway ein Stammzertifikat hinzuzufügen.
Der erste Befehl verwendet das **Cmdlet Get-Content,** um eine zuvor exportierte Textdarstellung des Stammzertifikats zu erhalten. diese Textdaten in einer Variablen mit dem Namen $Text.
Der zweite Befehl verwendet dann eine for-Schleife, um den ganzen Text mit Ausnahme der ersten und der letzten Zeile zu extrahieren und den extrahierten Text in einer Variablen namens $CertificateText.
Der dritte Befehl verwendet das **Cmdlet New-AzVpnClientRootCertificate** zum Erstellen des Zertifikats und speichert das erstellte Objekt in einer Variablen namens $Certificate.

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
Um die Textdarstellung zu erhalten, exportieren Sie Ihr Zertifikat im CER-Format (unter Verwendung der Base64-Codierung), und öffnen Sie dann die resultierende Datei in einem Text-Editor.
Eine ähnliche Ausgabe sollte angezeigt werden (beachten Sie, dass die tatsächliche Ausgabe viel mehr Textzeilen enthält als das hier gezeigte abgekürzte Beispiel): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo 09982CVVFAw8w ----- END CERTIFICATE ----- Das PublicCertData besteht aus allen Zeilen zwischen der ersten Zeile (----- BEGIN CERTIFICATE -----) und der letzten Zeile (----- END CERTIFICATE -----) in der Datei.
Sie können die PublicCertData mithilfe von Windows PowerShell-Befehlen wie diesem abrufen: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = für ($i=1; $i -lt $Text.Length -1 ; $i++){$Text \[ $i \] }

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate

## NOTIZEN

## VERWANDTE LINKS

[Add-AzVpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[Remove-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


