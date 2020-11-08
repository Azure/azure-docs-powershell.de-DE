---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
ms.openlocfilehash: 11b18f0a0f12a82e88694fd91ce89956951a4eb6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165200"
---
# New-AzVpnClientConfiguration

## Synopsis
Dieser Befehl ermöglicht es den Benutzern, das VPN-Profil Paket basierend auf vorkonfigurierten VPN-Einstellungen auf dem VPN-Gateway sowie einige zusätzliche Einstellungen zu erstellen, die Benutzer möglicherweise konfigurieren müssen, beispielsweise für einige Stammzertifikate.

## Syntax

```
New-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String> [-ProcessorArchitecture <String>]
 [-AuthenticationMethod <String>] [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
auf diese Weise können die Benutzer das VPN-Profil Paket basierend auf vorkonfigurierten VPN-Einstellungen auf dem VPN-Gateway sowie einige zusätzliche Einstellungen erstellen, die Benutzer möglicherweise konfigurieren müssen, beispielsweise für einige Stammzertifikate.

## Beispiele

### Beispiel 1
```
PS C:\> New-AzVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

Dieses Cmdlet wird verwendet, um eine ZIP-Datei für ein VPN-Clientprofil für "ContosoVirtualNetworkGateway" in der "ContosoResourceGroup" von "ResourceGroup" zu erstellen. Das Profil wird für einen vorkonfigurierten RADIUS-Server generiert, der für die Verwendung der Authentifizierungsmethode "eaptls" mit der VpnProfileRadiusCert-Zertifikatsdatei konfiguriert ist.

## Parameter

### -AuthenticationMethod
Die Authentifizierungsmethode kann Werte EAPMSCHAPv2 oder eaptls. Wenn EAPMSCHAPv2 angegeben wird, generiert das Cmdlet ein Client Konfigurations Installationsprogramm für die Benutzernamen-und Kennwortauthentifizierung, die EAP-MSCHAPv2 Authentifizierungsprotokoll verwendet. Wenn eaptls angegeben wird, generiert das Cmdlet ein Clientkonfigurations-Installationsprogramm für die Zertifikatauthentifizierung, die das EAP-TLS-Protokoll verwendet. Die Option "eaptls" kann sowohl für die RADIUS-basierte Zertifikatauthentifizierung als auch für die Zertifizierungs Authentifizierung verwendet werden, die vom virtuellen Netzwerk Gateway durch Hochladen des vertrauenswürdigen Stamms durchgeführt wird. Das Cmdlet erkennt automatisch, was konfiguriert ist.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ClientRootCertificateFileList
Eine Liste der Client-Stammzertifikat Pfade

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Name
Der Ressourcenname.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProcessorArchitecture
ProcessorArchitecture

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RadiusRootCertificateFile
RADIUS-Server-Stammzertifikatpfad. Hierbei handelt es sich um einen obligatorischen Parameter, der angegeben werden muss, wenn EAP-TLS mit RADIUS-Authentifizierung verwendet wird. Dies ist der vollständige Pfadname der CER-Datei, die das RADIUS-Stammzertifikat enthält, das der Client verwendet, um den RADIUS-Server während der Authentifizierung zu überprüfen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe.

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

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

### System. String []

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSVpnProfile

## Notizen

## Verwandte Links

[Get-AzVpnClientConfiguration](./Get-AzVpnClientConfiguration.md)
