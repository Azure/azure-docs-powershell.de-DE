---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: ab126ee6bfc6a19f4a3a9997a75a01277437e42d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918872"
---
# Remove-AzKeyVaultManagedStorageAccount

## SYNOPSIS
Entfernt ein vom Schlüsseltresor verwaltetes Azure Storage-Konto und alle zugehörigen SAS-Definitionen.

## SYNTAX

### ByDefinitionName (Standard)
```
Remove-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObject
```
Remove-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-InRemovedState] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESCHREIBUNG
Die Zuordnung eines Azure Storage-Kontos vom Schlüsseltresor wird aufgehoben. Dadurch wird kein Azure Storage-Konto entfernt, sondern die Kontoschlüssel werden nicht vom Azure Key Vault verwaltet. Alle zugeordneten Key Vault managed Storage SAS-Definitionen werden ebenfalls entfernt.

## BEISPIELE

### Beispiel 1: Entfernen eines vom Schlüsseltresor verwalteten Azure Storage-Kontos und aller zugehörigen SAS-Definitionen.
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

Entfernt das "mystorageaccount" des Azure Storage-Kontos vom Schlüsseltresor "myvault" und verhindert, dass der Schlüsseltresor seine Schlüssel verwaltet. Das Konto "mystorageaccount" wird nicht entfernt. Alle mit dem Schlüsseltresor verwalteten SAS-Definitionen, die diesem Konto zugeordnet sind, werden entfernt.

### Beispiel 2: Entfernen eines verwalteten Azure Storage-Schlüsseltresorkontos und aller zugehörigen SAS-Definitionen ohne Benutzerbestätigung.
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru -Force

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

Entfernt das "mystorageaccount" des Azure Storage-Kontos vom Schlüsseltresor "myvault" und verhindert, dass der Schlüsseltresor seine Schlüssel verwaltet. Das Konto "mystorageaccount" wird nicht entfernt. Alle mit dem Schlüsseltresor verwalteten SAS-Definitionen, die diesem Konto zugeordnet sind, werden entfernt.

### Beispiel 3: Endgültiges Löschen (Löschen) eines vom Schlüsseltresor verwalteten Azure Storage-Kontos und aller zugehörigen SAS-Definitionen aus einem Mit soft-delete aktivierten Tresor.
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' 
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
```

Im Beispiel wird davon ausgegangen, dass das soft-delete für diesen Tresor aktiviert ist. Überprüfen Sie, ob dies der Fall ist, indem Sie die Tresoreigenschaften oder das RecoveryLevel-Attribut einer Entität im Tresor untersuchen.
Das erste Cmdlet entfernt das "mystorageaccount" des Azure Storage-Kontos von "myvault" des Schlüsseltresors und verhindert, dass der Schlüsseltresor seine Schlüssel verwaltet. Das Konto "mystorageaccount" wird nicht entfernt. Alle mit dem Schlüsseltresor verwalteten SAS-Definitionen, die diesem Konto zugeordnet sind, werden entfernt.
Das zweite Cmdlet überprüft, ob sich das Speicherkonto in einem gelöschten, aber wiederherstellbaren Zustand befindet. Das Erreichen dieses Zustands kann einige Zeit erfordern, lassen Sie bitte ~30s zu, bevor Sie versuchen.
Das dritte Cmdlet entfernt das Speicherkonto dauerhaft – eine Wiederherstellung ist nicht mehr möglich.

## PARAMETER

### -AccountName
Name des verwalteten Speicherkontos für den Schlüsseltresor. Das Cmdlet erstellt den FQDN eines verwalteten Speicherkontonamens aus dem Tresornamen, der aktuell ausgewählten Umgebung und dem verwalteten Speicherkontonamen.

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName, Name

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

### -Erzwingen
Bitten Sie nicht um Bestätigung.

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

### -InRemovedState
Entfernen Sie das zuvor gelöschte verwaltete Speicherkonto endgültig.

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

### -PassThru
Das Cmdlet gibt standardmäßig kein -Objekt zurück.
Wenn dieser Schalter angegeben ist, gibt das Cmdlet das gelöschte verwaltete Speicherkonto zurück.

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

### -VaultName
Name des Tresors.
Das Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
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

### Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount

## NOTIZEN

## VERWANDTE LINKS

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

