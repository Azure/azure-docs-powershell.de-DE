---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 9595E785-6DBF-433C-83B3-8506A3B49B13
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 621e5ac05c5f975ff3878781bcb8c5a1b40c04bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664177"
---
# Get-AzureRmSiteRecoveryVaultSettingsFile

## Synopsis
Ruft die Datei für die Vault-Einstellungen der Websitewiederherstellung ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ByParam (Standard)
```
Get-AzureRmSiteRecoveryVaultSettingsFile [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Standard
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ForSite
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> -SiteIdentifier <String> -SiteFriendlyName <String>
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmSiteRecoveryVaultSettingsFile** " Ruft die Einstellungsdatei für ein Azure Site Recovery Vault ab.

## Beispiele

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

### -Path
Gibt den Pfad zur Website Recovery Vault Settings-Datei an.
Wenn Sie diese Datei lokal speichern möchten, laden Sie Sie nach Abschluss des Befehls aus dem Vault-Portal der Website wieder her.

```yaml
Type: String
Parameter Sets: Default, ForSite
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteFriendlyName
Gibt den Website Anzeigenamen für den Tresor an, wenn es sich um eine Hyper-V-Website handelt.

```yaml
Type: String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteIdentifier
Gibt die Website-ID für den Tresor an, wenn es sich um eine Hyper-V-Website handelt.

```yaml
Type: String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vault
Gibt das Vault-Objekt für die Website an.

```yaml
Type: ASRVault
Parameter Sets: Default, ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### ASRVault
Der Parameter "Vault" akzeptiert den Wert vom Typ "ASRVault" aus der Pipeline.

## Ausgaben

### Microsoft. Azure. Commands. SiteRecovery. VaultSettingsFilePath

## Notizen

## Verwandte Links

[Importieren-AzureRmSiteRecoveryVaultSettingsFile](./Import-AzureRmSiteRecoveryVaultSettingsFile.md)

[Satz-AzureRmSiteRecoveryVaultSettings](./Set-AzureRmSiteRecoveryVaultSettings.md)
