---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 90f6347346c0967e29917ffe56e7ba13f7e705de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472374"
---
# Add-AzKeyVaultManagedStorageAccount

## SYNOPSIS
Fügt dem angegebenen Schlüsseltresor ein vorhandenes Azure -Speicherkonto hinzu, dessen Schlüssel vom Schlüsseltresordienst verwaltet werden sollen.

## SYNTAX

```
Add-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-AccountResourceId] <String>
 [-ActiveKeyName] <String> [-DisableAutoRegenerateKey] [-RegenerationPeriod <TimeSpan>] [-Disable]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Richtet ein vorhandenes Azure -Speicherkonto mit Schlüsseltresor für Speicherkontoschlüssel ein, die vom Schlüsseltresor verwaltet werden sollen. Das Speicherkonto muss bereits vorhanden sein. Die Speicherschlüssel werden anrufer niemals verfügbar gemacht.
Der Schlüsseltresor generiert und wechselt den aktiven Schlüssel automatisch basierend auf dem Zeitraum. Eine Übersicht über dieses Feature finden Sie unter ["Verwaltetes Speicherkonto im Azure Key Vault – PowerShell".](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell)

## BEISPIELE

### Beispiel 1: Einrichten eines Azure -Speicherkontos mit Schlüsseltresor zum Verwalten seiner Schlüssel
```powershell
PS C:\> $storage = Get-AzStorageAccount -ResourceGroupName "mystorageResourceGroup" -StorageAccountName "mystorage"
PS C:\> $servicePrincipal = Get-AzADServicePrincipal -ServicePrincipalName cfa8b339-82a2-471a-a3c9-0fc0be7a4093
PS C:\> New-AzRoleAssignment -ObjectId $servicePrincipal.Id -RoleDefinitionName 'Storage Account Key Operator Service Role' -Scope $storage.Id
PS C:\> $userPrincipalId = $(Get-AzADUser -SearchString "developer@contoso.com").Id
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName $keyVaultName -ObjectId $userPrincipalId -PermissionsToStorage get, set
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -AccountResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key1
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

Legt ein Speicherkonto mit Schlüsseltresor für die Schlüssel fest, die vom Schlüsseltresor verwaltet werden sollen. Der aktive Schlüsselsatz ist "key1". Dieser Schlüssel wird zum Generieren von Sastokens verwendet. Der Schlüsseltresor generiert den Schlüssel "key2" nach dem Zeitraum des Diensts ab dem Zeitpunkt dieses Befehls erneut und setzt ihn als aktiven Schlüssel. Dieser automatische Vorgang wird zwischen "key1" und "key2" mit einer Lücke von 90 Tagen fortgesetzt.

### Beispiel 2: Festlegen eines klassischen Azure -Speicherkontos mit Schlüsseltresor zum Verwalten seiner Schlüssel
```powershell
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -AccountResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myvault/providers/Microsoft.Cl
                      assicStorage/storageAccounts/mystorageaccount
Active Key Name     : Primary
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

Legt ein klassisches Speicherkonto mit Schlüsseltresor für die Schlüssel fest, die vom Schlüsseltresor verwaltet werden sollen. Der Aktive Schlüsselsatz ist "Primär". Dieser Schlüssel wird zum Generieren von Sastokens verwendet. Der Schlüsseltresor generiert den sekundären Schlüssel nach dem Zeitraum des Diensts ab dem Zeitpunkt dieses Befehls erneut und setzt ihn als aktiven Schlüssel. Dieser automatische Vorgang wird zwischen "Primär" und "Sekundär" mit einer Lücke von 90 Tagen fortgesetzt.

## PARAMETERS

### -AccountName
Name des verwalteten Speicherkontos im Schlüsseltresor. Das Cmdlet erstellt den FQDN eines verwalteten Speicherkontos aus dem Namen des Tresors, der aktuell ausgewählten Umgebung und dem verwalteten Speicherkontonamen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AccountResourceId
Die Azure-Ressourcen-ID des Speicherkontos.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountResourceId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ActiveKeyName
Name des Speicherkontoschlüssels, der zum Generieren von Sastokens verwendet werden muss.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Deaktiviert die Verwendung des Schlüssels eines verwalteten Speicherkontos für die Generation von Sastokens.

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

### -DisableAutoRegenerateKey
Schlüssel automatisch neu generiert. Ist dies der Fall, wird der inaktive Schlüssel des verwalteten Speicherkontos automatisch neu generiert und nach dem Zeitraum zum neuen aktiven Schlüssel. Wenn "False", werden die Schlüssel des verwalteten Speicherkontos nicht automatisch erneut generiert.

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

### -Destimperiod
Zeitraum. Wenn die automatische neu generierte Taste aktiviert ist, gibt dieser Wert die Zeitspanne an, nach der die inaktiven Keygets des verwalteten Speicherkontos automatisch neu generiert und zum neuen aktiven Schlüssel werden.

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Name des Tresors.
Das Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
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

### System.String

### System.Nullable'1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Collections.Hashtable

## AUSGABEN

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Az.KeyVault](/powershell/module/az.keyvault)
