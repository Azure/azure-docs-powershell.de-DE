---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: e37236e4e5fbced90a6dbd5f33d22d02947b20d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664051"
---
# Get-AzureKeyVaultManagedStorageSasDefinition

## Synopsis
Ruft Schlüsselspeicher-SAS-Definitionen für verwalteten Speicher ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ByDefinitionName (Standard)
```
Get-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [[-Name] <String>]
 [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByInputObject
```
Get-AzureKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-Name] <String>] [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Ruft eine Key Vault-Definition für verwaltete Speicher SAS ab, wenn der Name der Definition angegeben wird. Wenn der Definitionsname nicht angegeben ist, werden alle SAS-Definitionen aufgelistet, die dem angegebenen Schlüsseldepot-verwalteten Speicherkonto im Tresor zugeordnet sind.

## Beispiele

### Beispiel 1: Auflisten aller Key Vault-Definitionen für verwaltete Speicher-SAS
```powershell
PS C:\> Get-AzureKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount'

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

Listet alle SAS-Definitionen auf, die mit dem von Vault "myvault" verwalteten Speicherkonto "mystorageaccount" des Schlüsseldepots verknüpft sind

### Beispiel 2: Abrufen eines verwalteten speicherkontos für Schlüsseldepots
```powershell
PS C:\> Get-AzureKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'accountsas'

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas
Secret Id   : https://myvault.vault.azure.net/secrets/mystorageaccount-accountsas
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas
Parameter   :
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

Ruft die Details der SAS-Definition "Konten" ab, die mit dem von Vault "myvault" verwalteten Speicherkonto "mystorageaccount" des Schlüsseldepots verknüpft sind.

## Parameter

### -Kontoname
Vault-Name.
Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inputobject
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
Gibt an, ob die zuvor gelöschten Speicher-SAS-Definitionen in der Ausgabe angezeigt werden sollen.

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

### -Name
Name der Speicher-SAS-Definition
Cmdlet erstellt den FQDN einer Speicher SAS-Definition aus Vault-Name, aktuell ausgewählter Umgebung, Speicherkonto Name und SAS-Definitionsname.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vaultname
Vault-Name.
Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccountIdentityItem
Parameter: Inputobject (ByValue)

## Ausgaben

### Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageSasDefinitionIdentityItem

### Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageSasDefinition

### Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition

### Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem

## Notizen

## Verwandte Links

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

