---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/set-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: b95f47de7fbdcf6b5ed7892cb8deb8656559da27
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938651"
---
# Set-AzKeyVaultManagedStorageSasDefinition

## SYNOPSIS
Legt eine SAS-Definition (Shared Access Signature) mit dem Schlüsseltresor für ein bestimmtes vom Schlüsseltresor verwaltetes Azure Storage-Konto fest.

## SYNTAX

### Standard (Standard)
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>] -ValidityPeriod <TimeSpan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObject
```
Set-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-Name] <String> [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>]
 -ValidityPeriod <TimeSpan> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESCHREIBUNG
Legt eine Sas-Definition (Shared Access Signature) mit einem verwalteten Azure -Speicherkonto (Key Vault) fest. Dadurch wird auch ein Geheimtipp definiert, der verwendet werden kann, um das SAS-Token nach dieser SAS-Definition abzurufen.
SAS-Token wird mit diesen Parametern und dem aktiven Schlüssel des verwalteten Azure Storage-Kontos für den Schlüsseltresor generiert.

## BEISPIELE

### Beispiel 1: Festlegen einer SAS-Definition vom Kontotyp und Abrufen eines aktuellen SAS-Tokens, das darauf basiert
```powershell
PS C:\> $sa = Get-AzStorageAccount -Name mysa -ResourceGroupName myrg
PS C:\> $kv = Get-AzKeyVault -VaultName mykv
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName $kv.VaultName -AccountName $sa.StorageAccountName -AccountResourceId $sa.Id -ActiveKeyName key1 -RegenerationPeriod ([System.Timespan]::FromDays(180))
PS C:\> $sctx = New-AzStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
PS C:\> $start = [System.DateTime]::Now.AddDays(-1)
PS C:\> $end = [System.DateTime]::Now.AddMonths(1)
PS C:\> $at = New-AzStorageAccountSasToken -Service blob,file,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
PS C:\> $sas = Set-AzKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
PS C:\> Get-AzKeyVaultSecret -VaultName $kv.VaultName -Name $sas.Sid.Substring($sas.Sid.LastIndexOf('/')+1)
```

Legt die SAS-Kontodefinition "Accountsas" für ein keyVault-verwaltetes Speicherkonto "mysa" im Tresor "mykv" fest. Insbesondere führt die vorstehende Sequenz die folgenden Schritte aus:
  - ruft ein (bereits vorhandenes) Speicherkonto ab.
  - ruft einen (bereits vorhandenen) Schlüsseltresor ab.
  - fügt dem Tresor ein von KeyVault verwaltetes Speicherkonto hinzu, indem Schlüssel1 als aktiver Schlüssel und mit einem Erneuerungszeitraum von 180 Tagen
  - legt einen Speicherkontext für das angegebene Speicherkonto fest, mit Key1
  - erstellt ein Konto-SAS-Token für Dienste Blob, Datei, Tabelle und Warteschlange, für die Ressourcentypen Dienst, Container und Objekt, mit allen Berechtigungen, über https und mit den angegebenen Start- und Enddatumsangaben.
  - legt eine VON KeyVault verwaltete SAS-Definition im Tresor fest, bei der der Vorlagen-URI als oben erstelltes SAS-Token vom SAS-Typ "Konto" für 30 Tage gültig ist.
  - ruft das tatsächliche Zugriffstoken aus dem KeyVault-Geheimschlüssel ab, der der SAS-Definition entspricht.

## PARAMETER

### -AccountName
Name des verwalteten Speicherkontos für den Schlüsseltresor. Das Cmdlet erstellt den FQDN eines verwalteten Speicherkontonamens aus dem Tresornamen, der aktuell ausgewählten Umgebung und dem verwalteten Speicherkontonamen.

```yaml
Type: System.String
Parameter Sets: Default
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden

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

### -Disable
Deaktiviert die Verwendung der sas-Definition für die Generierung von sas-Token.

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

### -InputObject
ManagedStorageAccount-Objekt.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Name der Speicher-SAS-Definition. Das Cmdlet erstellt den FQDN einer Speicher-SAS-Definition aus dem Tresornamen, der aktuell ausgewählten Umgebung, dem Namen des Speicherkontos und dem Sas-Definitionsnamen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SasType
Speicher-SAS-Typ.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Schlüssel-Wert-Paare in Form einer Hashtabelle. Beispiel: @{key0="value0";key1=$null;key2="value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TemplateUri
Storage SAS definition template uri.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ValidityPeriod
Gültigkeitszeitraum, der verwendet wird, um die Ablaufzeit des Sas-Tokens ab dem Zeitpunkt des Generierens zu festlegen.

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
Name des Tresors.
Das Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
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
Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem

## AUSGABEN

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition

## NOTIZEN

## VERWANDTE LINKS

[Azureâ€‹RM.â€‹Keyâ€‹Vault](/powershell/module/az.keyvault/)
