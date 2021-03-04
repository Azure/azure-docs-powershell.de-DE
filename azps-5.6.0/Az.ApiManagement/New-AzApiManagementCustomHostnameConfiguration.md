---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementcustomhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
ms.openlocfilehash: e2f7ca5ac27faa3730742f77495b6b21ac084553
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919088"
---
# New-AzApiManagementCustomHostnameConfiguration

## SYNOPSIS
Erstellt eine Instanz von `PsApiManagementCustomHostNameConfiguration` .

## SYNTAX

### NoChangeCertificate (Standard)
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -HostNameCertificateInformation <PsApiManagementCertificateInformation> [-DefaultSslBinding]
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SslCertificateFromFile
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -PfxPath <String> [-PfxPassword <SecureString>] [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SslCertificateFromKeyVault
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -KeyVaultId <String> [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet New-AzApiManagementCustomHostnameConfiguration** ist ein Hilfsbefehl, der eine Instanz von **PsApiManagementCustomHostNameConfiguration erstellt.**
Dieser Befehl wird zusammen mit dem cmdlet New-AzApiManagement und Set-AzApiManagement verwendet.

## BEISPIELE

### Beispiel 1: Erstellen und Initialisieren einer Instanz von PsApiManagementCustomHostNameConfiguration mit einem Ssl-Zertifikat aus datei
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -PfxPath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111" -DefaultSslBinding
PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig
```

Mit diesem Befehl wird eine Instanz von **PsApiManagementCustomHostNameConfiguration** für Portal erstellt und initialisiert. Anschließend wird ein neuer ApiManagement-Dienst mit benutzerdefinierter Hostnamenkonfiguration erstellt.

### Beispiel 2: Erstellen und Initialisieren einer Instanz von PsApiManagementCustomHostNameConfiguration mit einem Secret from KeyVault Resource
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"

PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig -SystemAssignedIdentity
```

Mit diesem Befehl wird eine Instanz von **PsApiManagementCustomHostNameConfiguration erstellt und initialisiert.**

## PARAMETER

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

### -DefaultSslBinding
Bestimmt, ob es sich bei dem Wert um einen geheimen Wert handelt, der verschlüsselt werden soll oder nicht.
Dieser Parameter ist optional.
Standardwert ist false.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hostname
Benutzerdefinierter Hostname

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

### -HostNameCertificateInformation
Vorhandene Zertifikatkonfiguration.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation
Parameter Sets: NoChangeCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -HostnameType
Hostnametyp

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameType
Parameter Sets: (All)
Aliases:
Accepted values: Proxy, Portal, Management, Scm, DeveloperPortal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVaultId
KeyVaultId zum geheimen Speichern des benutzerdefinierten SSL-Zertifikats.

```yaml
Type: System.String
Parameter Sets: SslCertificateFromKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NegotiateClientCertificate
Bestimmt, ob es sich bei dem Wert um einen geheimen Wert handelt, der verschlüsselt werden soll oder nicht.
Dieser Parameter ist optional.
Standardwert ist false.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PfxPassword
Kennwort für die PFX-Zertifikatdatei.

```yaml
Type: System.Security.SecureString
Parameter Sets: SslCertificateFromFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PfxPath
Pfad zu einer PFX-Zertifikatdatei.

```yaml
Type: System.String
Parameter Sets: SslCertificateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation

## AUSGABEN

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration

## NOTIZEN

## VERWANDTE LINKS

[New-AzApiManagement](./New-AzApiManagement.md)

[Set-AzApiManagement](./Set-AzApiManagement.md)