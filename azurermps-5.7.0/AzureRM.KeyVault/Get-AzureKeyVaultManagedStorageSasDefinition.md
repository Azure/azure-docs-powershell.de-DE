---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 7606293338e6467247e257f34e6850f52b67a1c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663480"
---
# Get-AzureKeyVaultManagedStorageSasDefinition

## Synopsis
Ruft Schlüsselspeicher-SAS-Definitionen für verwalteten Speicher ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ByAccountName (Standard)
```
Get-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByDefinitionName
```
Get-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Ruft eine Key Vault-Definition für verwaltete Speicher SAS ab, wenn der Name der Definition angegeben wird. Wenn der Definitionsname nicht angegeben ist, werden alle SAS-Definitionen aufgelistet, die dem angegebenen Schlüsseldepot-verwalteten Speicherkonto im Tresor zugeordnet sind.

## Beispiele

### Beispiel 1: Auflisten aller Key Vault-Definitionen für verwaltete Speicher-SAS
```
PS C:\> Get-AzureKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount'
```

Listet alle SAS-Definitionen auf, die mit dem von Vault "myvault" verwalteten Speicherkonto "mystorageaccount" des Schlüsseldepots verknüpft sind

### Beispiel 2: Abrufen eines verwalteten speicherkontos für Schlüsseldepots
```
PS C:\> Get-AzureKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasDef'
```

Ruft die Details der SAS-Definition "mysasDef" ab, die mit dem von Vault "myvault" verwalteten Schlüsseldepot-verwalteten Speicherkonto "mystorageaccount" verknüpft ist.

## Parameter

### -Kontoname
Vault-Name.
Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -Name
Name der Speicher-SAS-Definition
Cmdlet erstellt den FQDN einer Speicher SAS-Definition aus Vault-Name, aktuell ausgewählter Umgebung, Speicherkonto Name und SAS-Definitionsname.

```yaml
Type: String
Parameter Sets: ByDefinitionName
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Vaultname
Vault-Name.
Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. keyvault. Models. ManagedStorageSasDefinitionListItem, Microsoft. Azure. Commands. keyvault, Version = 2.5.0.0, Culture = neutral, PublicKeyToken = null]]
Microsoft. Azure. Commands. keyvault. Models. ManagedStorageSasDefinition

## Notizen

## Verwandte Links

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

