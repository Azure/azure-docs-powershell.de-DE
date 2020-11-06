---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/new-azurermstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
ms.openlocfilehash: 2ceb395805607809593054880415dccac7e1e28c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498161"
---
# New-AzureRmStorageAccount

## Synopsis
Erstellt ein Speicherkonto.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Location] <String> [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>]
 [-UseSubDomain <Boolean>] [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmStorageAccount** erstellt ein Azure Storage-Konto.

## Beispiele

### Beispiel 1: Erstellen eines speicherkontos
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

Mit diesem Befehl wird ein Speicherkonto für den Ressourcengruppennamen myresourcegroup erstellt.

### Beispiel 2: Erstellen eines BLOB-speicherkontos mit BlobStorage-freundlicher und heißer AccessTier
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

Mit diesem Befehl wird ein BLOB-Speicherkonto erstellt, das mit BlobStorage-freundlicher und heißer AccessTier

### Beispiel 3: Erstellen eines speicherkontos mit der Art StorageV2 und generieren und Zuweisen einer Identität für Azure keyvault
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

Dieser Befehl erstellt ein Speicherkonto mit der Art StorageV2.  Darüber hinaus wird eine Identität generiert und zugewiesen, die zum Verwalten von Konto Schlüsseln über Azure keyvault verwendet werden kann.

### Beispiel 4: Erstellen eines speicherkontos mit NetworkRuleSet aus JSON
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

Mit diesem Befehl wird ein Speicherkonto erstellt, das über die NetworkRuleSet-Eigenschaft von JSON verfügt

## Parameter

### -AccessTier
Gibt die Zugriffsebene des vom Cmdlet erstellten speicherkontos an.
Die akzeptablen Werte für diesen Parameter sind: heiß und cool.
Wenn Sie einen Wert von BlobStorage für den Parameter *Kind* angeben, müssen Sie einen Wert für den *AccessTier* -Parameter angeben. Wenn Sie einen Wert für Storage für diesen *Art* -Parameter angeben, geben Sie den *AccessTier* -Parameter nicht an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
Ausführen eines Cmdlets im Hintergrund

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

### -AssignIdentity
Generieren und Zuweisen einer neuen Speicherkonto Identität für dieses Speicherkonto für die Verwendung mit Schlüssel Verwaltungsdiensten wie Azure keyvault

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

### -CustomDomainName
Gibt den Namen der benutzerdefinierten Domäne des speicherkontos an.
Der Standardwert ist Storage.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

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

### -EnableHttpsTrafficOnly
Gibt an, ob das Speicherkonto nur HTTPS-Datenverkehr aktiviert.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Art
Gibt die Art des vom Cmdlet erstellten speicherkontos an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- Speicher. Speicherkonto für allgemeine Zwecke, das die Speicherung von BLOBs, Tabellen, Warteschlangen, Dateien und Datenträgern unterstützt.
- StorageV2. GPv2-Speicherkonto (General Purpose Version 2), das BLOBs, Tabellen, Warteschlangen, Dateien und Datenträger mit erweiterten Features wie Datenebenen unterstützt.
- BlobStorage. BLOB-Speicherkonto, das nur BLOB-Speicher unterstützt.
Der Standardwert ist Storage.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Standort
Gibt den Speicherort des zu erstellende speicherkontos an.

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

### -Name
Gibt den Namen des zu erstellende speicherkontos an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NetworkRuleSet
NetworkRuleSet wird verwendet, um eine Reihe von Konfigurationsregeln für Firewalls und virtuelle Netzwerke zu definieren sowie Werte für Netzwerkeigenschaften festzulegen, beispielsweise Dienste, die die Regeln umgehen dürfen, und die Behandlung von Anforderungen, die keiner der definierten Regeln entsprechen.

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, in der das Speicherkonto hinzugefügt werden soll.

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

### -SkuName
Gibt den SKU-Namen des speicherkontos an, das von diesem Cmdlet erstellt wird.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- Standard_LRS. Lokal redundanter Speicherplatz.
- Standard_ZRS. Zone – redundanter Speicher.
- Standard_GRS. Geo-redundanter Speicher.
- Standard_RAGRS. Lesezugriff Geo-redundanter Speicher.
- Premium_LRS. Premium-lokal redundanter Speicherplatz.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags auf dem Server definiert ist. Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseSubDomain
Gibt an, ob die indirekte CNAME-Validierung aktiviert werden soll.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

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

### System. Boolean

## Ausgaben

### Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount

## Notizen

## Verwandte Links

[Get-AzureRmStorageAccount](./Get-AzureRmStorageAccount.md)

[Remove-AzureRmStorageAccount](./Remove-AzureRmStorageAccount.md)

[Satz-AzureRmStorageAccount](./Set-AzureRmStorageAccount.md)
