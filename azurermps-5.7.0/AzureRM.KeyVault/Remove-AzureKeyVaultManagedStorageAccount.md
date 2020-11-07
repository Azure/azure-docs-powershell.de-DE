---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c422975af622fe54602224b0c311ea8e738f838f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662727"
---
# Remove-AzureKeyVaultManagedStorageAccount

## Synopsis
Entfernt ein zentrales Vault Managed Azure-Speicherkonto und alle zugehörigen SAS-Definitionen.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Remove-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Trennt ein Azure Storage-Konto von Key Vault. Dadurch wird kein Azure-Speicherkonto entfernt, aber die Kontoschlüssel werden vom Azure Key Vault verwaltet. Alle zugehörigen Schlüsselspeicher-SAS-Definitionen für den Speicher werden ebenfalls entfernt.

## Beispiele

### Beispiel 1: Entfernen eines zentralen Vault Managed Azure-speicherkontos und aller zugehörigen SAS-Definitionen.
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount'
```

Trennt das Azure-Speicherkonto "mystorageaccount" vom schlüsseltresor "myvault" ab und verhindert, dass die Schlüssel von Key Vault verwaltet werden. Das Konto "mystorageaccount" wird nicht entfernt. Alle mit diesem Konto verknüpften Schlüsselspeicher-SAS-Definitionen für verwalteten Speicher werden entfernt.

### Beispiel 2: Entfernen eines zentralen Vault Managed Azure-speicherkontos und aller zugehörigen SAS-Definitionen ohne Bestätigung des Benutzers.
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Force -Confirm:$False
```

Trennt das Azure-Speicherkonto "mystorageaccount" vom schlüsseltresor "myvault" ab und verhindert, dass die Schlüssel von Key Vault verwaltet werden. Das Konto "mystorageaccount" wird nicht entfernt. Alle mit diesem Konto verknüpften Schlüsselspeicher-SAS-Definitionen für verwalteten Speicher werden entfernt.

## Parameter

### -Kontoname
Name des verwalteten speicherkontos in Key Vault Cmdlet erstellt den FQDN eines verwalteten Speicherkonto namens aus Vault Name, aktuell ausgewählter Umgebung und verwaltetem Speicherkonto Namen.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

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

### -Force
Keine Bestätigung anfordern.

```yaml
Type: SwitchParameter
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
Wenn dieser Schalter angegeben wird, gibt das Cmdlet das gelöschte verwaltete Speicherkonto zurück.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. keyvault. Models. ManagedStorageAccount

## Notizen

## Verwandte Links

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

