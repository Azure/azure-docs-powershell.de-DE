---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
ms.openlocfilehash: e5dd9da25bfa2c27bd605dc80b04f8e47fb7f95b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924675"
---
# New-AzVpnClientConfiguration

## SYNOPSIS
Dieser Befehl ermöglicht benutzern das Erstellen des Vpn-Profilpakets basierend auf vorkonfigurierten Vpn-Einstellungen auf dem VPN-Gateway, zusätzlich zu einigen zusätzlichen Einstellungen, die Benutzer möglicherweise konfigurieren müssen, z. B. für einige Stammzertifikate.

## SYNTAX

```
New-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String> [-ProcessorArchitecture <String>]
 [-AuthenticationMethod <String>] [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESCHREIBUNG
Auf diese Weise können die Benutzer das Vpn-Profilpaket basierend auf vorkonfigurierten Vpn-Einstellungen auf dem VPN-Gateway erstellen, zusätzlich zu einigen zusätzlichen Einstellungen, die Benutzer möglicherweise konfigurieren müssen, z. B. für einige Stammzertifikate.

## BEISPIELE

### Beispiel 1
```
PS C:\> New-AzVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

Dieses Cmdlet wird verwendet, um eine ZIP-Datei für ein VPN-Clientprofil für "ContosoVirtualNetworkGateway" in der Ressourcengruppe "ContosoResourceGroup" zu erstellen. Das Profil wird für einen vorkonfigurierten Radiusserver generiert, der für die Verwendung der Authentifizierungsmethode "EAPTLS" mit der VpnProfileRadiusCert-Zertifikatdatei konfiguriert ist.

## PARAMETER

### -AuthenticationMethod
Die Authentifizierungsmethode kann werte EAPMSCHAPv2 oder EAPTLS übernehmen. Wenn EAPMSCHAPv2 angegeben wird, generiert das Cmdlet ein Clientkonfigurationsinstallationsprogramm für die Benutzername-/Kennwortauthentifizierung, das EAP-MSCHAPv2 Authentifizierungsprotokoll verwendet. Wenn EAPTLS angegeben ist, generiert das Cmdlet ein Clientkonfigurationsinstallationsprogramm für die Zertifikatauthentifizierung, das das EAP-TLS-Protokoll verwendet. Die Option "EapTls" kann sowohl für die RADIUS-basierte Zertifikatauthentifizierung als auch für die Zertifizierungsauthentifizierung verwendet werden, die vom Virtual Network Gateway durch Hochladen des vertrauenswürdigen Stamms ausgeführt wird. Das Cmdlet erkennt automatisch, was konfiguriert ist.

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
Eine Liste der Clientstammzertifikatpfade

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
Radiusserverstammzertifikatpfad. Dies ist ein obligatorischer Parameter, der angegeben werden muss, wenn EAP-TLS mit RADIUS-Authentifizierung verwendet wird. Dies ist der vollständige Pfadname der CER-Datei, die das RADIUS-Stammzertifikat enthält, das vom Client zum Überprüfen des RADIUS-Servers während der Authentifizierung verwendet wird.

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
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

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
Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

### System.String[]

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSVpnProfile

## NOTIZEN

## VERWANDTE LINKS

[Get-AzVpnClientConfiguration](./Get-AzVpnClientConfiguration.md)
