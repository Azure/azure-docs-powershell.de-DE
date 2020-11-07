---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
ms.openlocfilehash: aee61173ee327d0c65f4cc04451fd64f51a79522
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663060"
---
# Restore-AzureKeyVaultKey

## Synopsis
Erstellt einen Schlüssel in einem schlüsseltresor aus einem gesicherten Schlüssel.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ByVaultName (Standard)
```
Restore-AzureKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObject
```
Restore-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Restore-AzureKeyVaultKey** erstellt einen Schlüssel im angegebenen schlüsseltresor.
Dieser Schlüssel ist ein Replikat des gesicherten Schlüssels in der Eingabedatei und hat denselben Namen wie der ursprüngliche Schlüssel.
Wenn der schlüsseltresor bereits über einen Schlüssel mit demselben Namen verfügt, schlägt dieses Cmdlet fehl, anstatt den ursprünglichen Schlüssel zu überschreiben.
Wenn die Sicherung mehrere Versionen eines Schlüssels enthält, werden alle Versionen wiederhergestellt.

Der schlüsseltresor, in den Sie den Schlüssel wiederherstellen, kann sich vom schlüsseltresor unterscheiden, von dem Sie den Schlüssel gesichert haben.
Der schlüsseltresor muss jedoch dasselbe Abonnement verwenden und sich in einem Azure-Bereich in derselben geografischen Region befinden (beispielsweise in Nordamerika).
Informationen finden Sie im Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) für die Zuordnung von Azure-Regionen zu Geographien.

## Beispiele

### Beispiel 1: Wiederherstellen eines gesicherten Schlüssels
```
PS C:\>Restore-AzureKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

Mit diesem Befehl wird ein Schlüssel, einschließlich aller Versionen, aus der Sicherungsdatei mit dem Namen Backup. BLOB in den schlüsseltresor mit dem Namen MyKeyVault wiederhergestellt.

## Parameter

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

### -Eingabefeld
Gibt die Eingabedatei an, die die Sicherung des wiederherzustellenden Schlüssels enthält.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inputobject
Keyvault-Objekt

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Vaultname
Gibt den Namen des Schlüssel Tresors an, in den der Schlüssel wiederhergestellt werden soll.

```yaml
Type: String
Parameter Sets: ByVaultName
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

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKey

## Notizen

## Verwandte Links

[Add-AzureKeyVaultKey](./Add-AzureKeyVaultKey.md)

[Backup-AzureKeyVaultKey](./Backup-AzureKeyVaultKey.md)

[Get-AzureKeyVaultKey](./Get-AzureKeyVaultKey.md)

[Remove-AzureKeyVaultKey](./Remove-AzureKeyVaultKey.md)

