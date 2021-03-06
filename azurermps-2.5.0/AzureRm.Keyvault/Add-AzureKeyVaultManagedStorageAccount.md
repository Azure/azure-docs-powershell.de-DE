---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
ms.openlocfilehash: 4bd6db0cf8dce4270e14337ee1168002618e3dc3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848252"
---
# Add-AzureKeyVaultManagedStorageAccount

## Synopsis
Fügt dem angegebenen schlüsseltresor ein vorhandenes Azure Storage-Konto hinzu, dessen Schlüssel vom Schlüssel-Vault-Dienst verwaltet werden.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Add-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-AccountResourceId] <String> [-ActiveKeyName] <String> [-DisableAutoRegenerateKey]
 [-RegenerationPeriod <TimeSpan>] [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Richtet ein vorhandenes Azure Storage-Konto mit dem schlüsseltresor für speicherkontoschlüssel ein, die von Key Vault verwaltet werden sollen. Das Speicherkonto muss bereits vorhanden sein. Die Speichertasten werden dem Anrufer nie angezeigt.
Key Vault wird automatisch neu generiert und wechselt basierend auf dem Erneuerungszeitraum den aktiven Schlüssel.

## Beispiele

### Beispiel 1: Einrichten eines Azure Storage-Kontos mit Key Vault zum Verwalten der Schlüssel
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod
```

Legt ein Speicherkonto mit Key Vault fest, dessen Schlüssel von Key Vault verwaltet werden sollen. Der aktive Schlüsselsatz ist "key1". Dieser Schlüssel wird verwendet, um SAS-Token zu generieren. Key Vault generiert den Schlüssel "key2" nach dem Regenerations Zeitraum ab dem Zeitpunkt des Befehls erneut und legt ihn als aktiven Schlüssel ab. Dieser automatische Regenerierungs Prozess wird zwischen "key1" und "key2" mit einem Abstand von 90 Tagen fortgesetzt.

### Beispiel 2: Einrichten eines klassischen Azure-speicherkontos mit Key Vault zum Verwalten der Schlüssel
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod
```

Legt ein klassisches Speicherkonto mit Key Vault fest, dessen Schlüssel von Key Vault verwaltet werden sollen. Der aktive Schlüsselsatz ist "Primär". Dieser Schlüssel wird verwendet, um SAS-Token zu generieren. Key Vault generiert nach dem Regenerations Zeitraum ab dem Zeitpunkt des Befehls den "sekundären" Schlüssel und legt ihn als aktiven Schlüssel ab. Dieser automatische Regenerierungs Prozess wird zwischen "Primär" und "Sekundär" mit einem Abstand von 90 Tagen fortgesetzt.

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

### -AccountResourceId
Azure-Ressourcen-ID des speicherkontos.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountResourceId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ActiveKeyName
Der Name des Speicherkonto Schlüssels, der zum Generieren von SAS-Token verwendet werden muss.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
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

### -Deaktivieren Sie
Deaktiviert die Verwendung des Schlüssels des verwalteten speicherkontos für die Generierung von SAS-Token.

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

### -DisableAutoRegenerateKey
Schlüssel zur automatischen Neugenerierung Ist der Wert "true", wird der inaktive Schlüssel des verwalteten speicherkontos automatisch neu generiert und nach dem Erneuerungszeitraum zum neuen aktiven Schlüssel. Ist der Wert false, werden die Schlüssel des verwalteten speicherkontos nicht automatisch neu generiert.

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

### -RegenerationPeriod
Erneuerungszeitraum. Wenn der Schlüssel für die automatische Regenerierung aktiviert ist, gibt dieser Wert die Zeitspanne an, nach der der inaktive keydes verwalteten speicherkontos automatisch neu generiert wird und zum neuen aktiven Schlüssel wird.

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Schlüssel-Wert-Paare in Form einer Hashtabelle Zum Beispiel:

@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
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

## Ausgaben

### Microsoft. Azure. Commands. keyvault. Models. ManagedStorageAccount

## Notizen

## Verwandte Links

[AzureRM. keyvault](/powershell/module/azurerm.keyvault)
