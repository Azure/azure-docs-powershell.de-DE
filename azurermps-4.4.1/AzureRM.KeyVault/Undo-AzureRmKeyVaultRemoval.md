---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
ms.openlocfilehash: 57fdddfea449bbde18762afaed0c576c2b4d1db3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663927"
---
# Undo-AzureRmKeyVaultRemoval

## Synopsis
Stellt einen gelöschten schlüsseltresor in einen aktiven Zustand.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Undo-AzureRmKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **"Undo-AzureRmKeyVaultRemoval"** wird ein zuvor gelöschter schlüsseltresor wiederhergestellt. Der wiederhergestellte Tresor wird nach der Wiederherstellung aktiviert.

## Beispiele

### Beispiel 1
```
PS C:\> Undo-AzureRmKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}
```

Mit diesem Befehl wird der schlüsseltresor "MyKeyVault" wiederhergestellt, der zuvor aus der eastus2-Region und der Ressourcengruppe "myresourcegroup" gelöscht wurde, in einen aktiven und nutzbaren Zustand. Außerdem werden die Tags durch eine neue Kategorie ersetzt.

## Parameter

### -Standort
Gibt den ursprünglichen Azure-Bereich für gelöschte Vaults an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer vorhandenen Ressourcengruppe an, in der der schlüsseltresor erstellt werden soll.

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

### -Tag
Schlüssel-Wert-Paare in Form einer Hashtabelle Zum Beispiel:

@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

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
Type: System.String
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
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

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

### System. String
System. Collections. Hashtable

## Ausgaben

### Microsoft. Azure. Commands. keyvault. Models. PSVault

## Notizen

## Verwandte Links

[Remove-AzureRmKeyVault](./Remove-AzureRmKeyVault.md)

[Neu – AzureRmKeyVault](./New-AzureRmKeyVault.md)

[Get-AzureRmKeyVault](./Get-AzureRmKeyVault.md)
