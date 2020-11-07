---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: 5455babba58e050397066e5439b3e046315b4101
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824296"
---
# Get-AzRecoveryServicesVaultSettingsFile

## Synopsis
Ruft die Azure Site Recovery Vault Settings-Datei ab.

## Syntax

### ForSiteWithCertificate
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -SiteIdentifier <String>
 -Certificate <String> -SiteFriendlyName <String> [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByDefaultWithCertificate
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String>
 [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ForBackupVaultTypeWithCertificate
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String> [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzRecoveryServicesVaultSettingsFile** " Ruft die Einstellungsdatei für ein Azure Site Recovery Vault ab.

## Beispiele

### Beispiel 1: Registrieren eines Windows-Servers oder DPM-Computers für Azure-Sicherung
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

Der erste Befehl ruft den Tresor mit dem Namen TestVault ab und speichert ihn dann in der Variablen $Vault 01.
Mit dem zweiten Befehl wird die $CredsPath-Variable auf C:\Downloads. festgelegt.
Der letzte Befehl ruft die Vault-Anmeldeinformationsdatei für $Vault 01 unter Verwendung der Anmeldeinformationen in $CredsPath für Azure-Sicherung ab.

### Beispiel 2:
```
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

Der Befehl ruft die Vault-Anmeldeinformationsdatei für $Vault 01 des Vault-Typs siteRecovery ab.

### Beispiel 3: Registrieren eines Windows-Servers oder DPM-Computers für Azure-Sicherung
```
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

Der Befehl ruft die Vault-Anmeldeinformationsdatei für $Vault 01 ab.

## Parameter

### -Backup
Gibt an, dass die Vault-Anmeldeinformationsdatei auf Azure Backup anwendbar ist.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultTypeWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Zertifikat
{{Fill Certificate Description}}

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

### -Path
Gibt den Pfad zur Azure Site Recovery Vault Settings-Datei an.
Sie können diese Datei vom Azure Site Recovery Vault-Portal herunterladen und lokal speichern.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteFriendlyName
Gibt den Anzeigenamen der Website an.
Verwenden Sie diesen Parameter, wenn Sie die Vault-Anmeldeinformationen für eine Hyper-V-Website herunterladen.

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteIdentifier
Gibt die Website-ID an.
Verwenden Sie diesen Parameter, wenn Sie die Vault-Anmeldeinformationen für eine Hyper-V-Website herunterladen.

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteRecovery
Gibt an, dass die Vault-Anmeldeinformationsdatei auf Azure Site Recovery anwendbar ist.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSiteWithCertificate, ByDefaultWithCertificate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vault
Gibt das Azure Site Recovery Vault-Objekt an.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. RecoveryServices. ARSVault

## Ausgaben

### Microsoft. Azure. Commands. RecoveryServices. VaultSettingsFilePath

## Notizen

## Verwandte Links

[Get-AzRecoveryServicesVault](./Get-AzRecoveryServicesVault.md)

[Neu – AzRecoveryServicesVault](./New-AzRecoveryServicesVault.md)

[Remove-AzRecoveryServicesVault](./Remove-AzRecoveryServicesVault.md)


