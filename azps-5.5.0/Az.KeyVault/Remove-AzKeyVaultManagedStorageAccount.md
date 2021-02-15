---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c415a7b80609a9e8794df183b2ae1cea73a7f1cd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159593"
---
# Remove-AzKeyVaultManagedStorageAccount

## SYNOPSIS
Entfernt ein schlüsseltresor verwaltetes Azure Storage-Konto und alle zugehörigen SAS-Definitionen.

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
Entfernt ein Azure -Speicherkonto vom Schlüsseltresor. Dadurch wird kein Azure -Speicherkonto entfernt, sondern die Kontoschlüssel werden von Azure Key Vault verwaltet. Alle zugeordneten SAS-Definitionen für den schlüsseltresor verwalteten Speicher werden ebenfalls entfernt.

## BEISPIELE

### Beispiel 1: Entfernen eines schlüsseltresor verwalteten Azure -Speicherkontos und aller zugehörigen SAS-Definitionen.
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

Entfernt die Zuordnung des Azure -Speicherkontos "mystorageaccount" vom Schlüsseltresor "myvault" und verhindert, dass der Schlüsseltresor seine Schlüssel verwaltet. Das Konto "mystorageaccount" wird nicht entfernt. Alle diesem Konto zugeordneten SAS-Definitionen für verwalteten Speicher im Schlüsseltresor werden entfernt.

### Beispiel 2: Entfernen eines schlüsseltresor verwalteten Azure -Speicherkontos und aller zugehörigen SAS-Definitionen ohne Benutzerbestätigung.
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

Entfernt die Zuordnung des Azure -Speicherkontos "mystorageaccount" vom Schlüsseltresor "myvault" und verhindert, dass der Schlüsseltresor seine Schlüssel verwaltet. Das Konto "mystorageaccount" wird nicht entfernt. Alle diesem Konto zugeordneten SAS-Definitionen für verwalteten Speicher im Schlüsseltresor werden entfernt.

### Beispiel 3: Endgültiges Löschen eines Schlüsseltresor, das vom Schlüsseltresor verwaltet wurde, und aller zugehörigen SAS-Definitionen aus einem für die weiche Löschung aktivierten Tresor.
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' 
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
```

Im Beispiel wird davon ausgegangen, dass das weiche Löschen für diesen Tresor aktiviert ist. Überprüfen Sie, ob dies der Fall ist, indem Sie die Eigenschaften des Tresors oder das Attribut "RecoveryLevel" einer Entität im Tresor überprüfen.
Das erste Cmdlet entfernt "mystorageaccount" des Azure-Speicherkontos vom Schlüsseltresor "myvault" und verhindert, dass der Schlüsseltresor seine Schlüssel verwaltet. Das Konto "mystorageaccount" wird nicht entfernt. Alle diesem Konto zugeordneten SAS-Definitionen für verwalteten Speicher im Schlüsseltresor werden entfernt.
Mit dem zweiten Cmdlet wird überprüft, ob sich das Speicherkonto in einem gelöschten, aber beh wiederherstellbaren Zustand befindet. Das Erreichen dieses Status kann einige Zeit erfordern. Lassen Sie bitte ca. 30 s zu, bevor Sie versuchen.
Das dritte Cmdlet entfernt das Speicherkonto dauerhaft – eine Wiederherstellung ist nicht mehr möglich.

## PARAMETERS

### -AccountName
Name des verwalteten Speicherkontos im Schlüsseltresor. Das Cmdlet erstellt den FQDN eines verwalteten Speicherkontos aus dem Namen des Tresors, der aktuell ausgewählten Umgebung und dem verwalteten Speicherkontonamen.

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

### -Force
Fordern Sie keine Bestätigung an.

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
Endgültiges Entfernen des zuvor gelöschten verwalteten Speicherkontos.

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
Das Cmdlet gibt standardmäßig kein Objekt zurück.
Wenn dieser Schalter angegeben ist, gibt das Cmdlet das konto für verwalteten Speicher zurück, das gelöscht wurde.

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
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem

## AUSGABEN

### Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

