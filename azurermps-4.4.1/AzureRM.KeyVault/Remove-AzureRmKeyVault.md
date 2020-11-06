---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://go.microsoft.com/fwlink/?LinkId=690162
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
ms.openlocfilehash: 2a30a190fbf257142e1c1e4fb4329fd6c4f41e3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502697"
---
# Remove-AzureRmKeyVault

## Synopsis
Löscht einen schlüsseltresor.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ByAvailableVault
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDeletedVault
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-Force] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureRmKeyVault** löscht den angegebenen schlüsseltresor.
Außerdem werden alle Schlüssel und Geheimnisse gelöscht, die in dieser Instanz enthalten sind.

Beachten Sie, dass Sie eine bessere Leistung erzielen sollten, wenn Sie die Ressourcengruppe für dieses Cmdlet optional angeben.

## Beispiele

### Beispiel 1: Entfernen eines Schlüsseldepots
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault"
```

Mit diesem Befehl wird der schlüsseltresor mit dem Namen Contoso03Vault aus Ihrem aktuellen Abonnement entfernt.

### Beispiel 2: Entfernen eines Schlüsseldepots aus einer angegebenen Ressourcengruppe
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

Mit diesem Befehl wird der schlüsseltresor mit dem Namen Contoso03Vault aus der benannten Ressourcengruppe entfernt.
Wenn Sie den Namen der Ressourcengruppe nicht angeben, sucht das Cmdlet nach dem benannten schlüsseltresor, der in Ihrem aktuellen Abonnement gelöscht werden soll.

## Parameter

### -Force
Gibt an, dass das Cmdlet Sie nicht zur Bestätigung auffordert.
Standardmäßig werden Sie von diesem Cmdlet aufgefordert, zu bestätigen, dass Sie den schlüsseltresor löschen möchten.

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

### -InRemovedState
Entfernen Sie den zuvor gelöschten Tresor endgültig.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Standort
Der Speicherort des gelöschten Tresors.

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an.

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Vaultname
Gibt den Namen des zu entfernenden Schlüsseldepots an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureRmKeyVault](./Get-AzureRmKeyVault.md)

[Neu – AzureRmKeyVault](./New-AzureRmKeyVault.md)
