---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-Azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
ms.openlocfilehash: aaace602cd50f9464021b1dcbefe39272e1621bb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842163"
---
# Get-AzKeyVault

## Synopsis
Ruft Schlüsseldepots ab.

## Syntax

### GetVaultByName
```
Get-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByDeletedVault
```
Get-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListVaultsByResourceGroup
```
Get-AzKeyVault [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ListAllDeletedVaultsInSubscription
```
Get-AzKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListAllVaultsInSubscription
```
Get-AzKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzKeyVault** " Ruft Informationen zu den Schlüsseldepots in einem Abonnement ab. Sie können alle wichtigen Vaults-Instanzen in einem Abonnement anzeigen oder Ihre Ergebnisse nach einer Ressourcengruppe oder einem bestimmten schlüsseltresor filtern.

Beachten Sie, dass die Angabe der Ressourcengruppe zwar für dieses Cmdlet optional ist, wenn Sie einen einzelnen schlüsseltresor erhalten, Sie dies jedoch für eine bessere Leistung tun sollten.

## Beispiele

### Beispiel 1: Abrufen aller Schlüsseldepots in Ihrem aktuellen Abonnement
```
PS C:\>Get-AzKeyVault
```

Dieser Befehl ruft alle Schlüsseldepots Ihres aktuellen Abonnements ab.

### Beispiel 2: Abrufen eines bestimmten Schlüsseldepots
```
PS C:\>$MyVault = Get-AzKeyVault -VaultName 'Contoso03Vault'
```

Dieser Befehl ruft den schlüsseltresor mit dem Namen Contoso03Vault in Ihrem aktuellen Abonnement ab und speichert ihn dann in der $MyVault-Variablen. Sie können die Eigenschaften von $MyVault überprüfen, um Details zum schlüsseltresor abzurufen.

### Beispiel 3: Abrufen von Schlüsseldepots in einer Ressourcengruppe
```
PS C:\>Get-AzKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

Dieser Befehl ruft alle Schlüsseldepots in der Ressourcengruppe mit dem Namen ContosoPayRollResourceGroup ab.

### Beispiel 4: Abrufen aller gelöschten Schlüsseldepots in Ihrem aktuellen Abonnement
```
PS C:\>Get-AzKeyVault -InRemovedState
```

Dieser Befehl ruft alle gelöschten Schlüsseldepots in Ihrem aktuellen Abonnement ab.

### Beispiel 5: Abrufen eines gelöschten Schlüsseldepots
```
PS C:\>Get-AzKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

Dieser Befehl ruft die gelöschten Schlüssel Vault-Informationen mit dem Namen Contoso03Vault in Ihrem aktuellen Abonnement und in der eastus2-Region ab.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InRemovedState
Gibt an, ob die zuvor gelöschten Tresore in der Ausgabe angezeigt werden sollen.

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Standort
Der Speicherort des gelöschten Tresors.

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, die dem schlüsseltresor oder den Schlüsseldepots zugeordnet ist, die abgefragt werden.

```yaml
Type: String
Parameter Sets: GetVaultByName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ListVaultsByResourceGroup
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
Type: Hashtable
Parameter Sets: ListAllVaultsInSubscription
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Vaultname
Gibt den Namen des Schlüsseldepots an.

```yaml
Type: String
Parameter Sets: GetVaultByName, ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Microsoft. Azure. Commands. keyvault. Models. PSVault

### System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. keyvault. Models. PSVaultIdentityItem]

### Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault

### System. Collections. Generic. List ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]

## Notizen

## Verwandte Links

[Neu – AzKeyVault](./New-AzKeyVault.md)

[Remove-AzKeyVault](./Remove-AzKeyVault.md)
