---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
ms.openlocfilehash: 11b18f0a0f12a82e88694fd91ce89956951a4eb6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156865"
---
# New-AzVpnClientConfiguration

## SYNOPSIS
Dieser Befehl ermöglicht es den Benutzern, zusätzlich zu einigen zusätzlichen Einstellungen, die Benutzer möglicherweise konfigurieren müssen, z. B. einige Stammzertifikate, das Vpn-Profilpaket basierend auf vorkonfigurierten Vpneinstellungen auf dem VPN-Gateway zu erstellen.

## SYNTAX

```
New-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String> [-ProcessorArchitecture <String>]
 [-AuthenticationMethod <String>] [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESCHREIBUNG
dadurch können die Benutzer zusätzlich zu einigen zusätzlichen Einstellungen, die Benutzer möglicherweise konfigurieren müssen, z. B. einige Stammzertifikate, das Vpn-Profilpaket basierend auf vorkonfigurierten Vpneinstellungen auf dem VPN-Gateway erstellen.

## BEISPIELE

### Beispiel 1
```
PS C:\> New-AzVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

Dieses Cmdlet wird verwendet, um eine ZIP-Datei für das VPN-Clientprofil für "ContosoVirtualNetworkGateway" in der Ressourcengruppe "ContosoResourceGroup" zu erstellen. Das Profil wird für einen vorkonfigurierten Radiusserver generiert, der für die Verwendung der "EAPTLS"-Authentifizierungsmethode mit der Zertifikatdatei "VpnProfileRadiusCert" konfiguriert ist.

## PARAMETERS

### -AuthenticationMethod
Bei der Authentifizierungsmethode können Werte wie EAPMSCHAPv2 oder EAPTLS verwendet werden. Wenn EAPMSCHAPv2 angegeben wird, generiert das Cmdlet ein Clientkonfigurationsprogramm für die Authentifizierung mit Benutzername/Kennwort, das EAP-MSCHAPv2 verwendet. Wenn EAPTLS angegeben wird, generiert das Cmdlet ein Clientkonfigurationsprogramm für die Zertifikatauthentifizierung, das das EAP-TLS-Protokoll verwendet. Die Option "EapTls" kann sowohl für DIE RADIUS-basierte Zertifikatauthentifizierung als auch für die Zertifizierungsauthentifizierung verwendet werden, die vom virtuellen Netzwerkgateway durch Hochladen des vertrauenswürdigen Stamms ausgeführt wird. Das Cmdlet erkennt automatisch, was konfiguriert ist.

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
Eine Liste der Pfade für Clientstammzertifikate

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
Radius des Serverstammzertifikatpfads. Dies ist ein obligatorischer Parameter, der angegeben werden muss, wenn EAP-TLS mit RADIUS-Authentifizierung verwendet wird. Dies ist der vollständige Pfadname der CER-Datei, die das RADIUS-Stammzertifikat enthält, das der Client zum Überprüfen des RADIUS-Servers während der Authentifizierung verwendet.

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

### -Confirm
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

### -Waswenn
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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

### System.String[]

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSVpnProfile

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzVpnClientConfiguration](./Get-AzVpnClientConfiguration.md)
