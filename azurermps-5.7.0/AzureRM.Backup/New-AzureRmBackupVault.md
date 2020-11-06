---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 015E3BC9-C535-4EA2-8A30-C728385DBFF8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
ms.openlocfilehash: 77c2df1ec61b42aaded458bea564cf6c953c90ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501509"
---
# New-AzureRmBackupVault

## Synopsis
Erstellt einen Sicherungsspeicher.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureRmBackupVault [-ResourceGroupName] <String> [-Name] <String> [-Region] <String>
 [[-Storage] <AzureBackupVaultStorageType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **New-AzureRmBackupVault** wird ein Azure Backup Vault erstellt.
Dieses Cmdlet gibt ein **AzureRmBackupVault** -Objekt zurück, das als Verweis auf die Vault-Entität fungiert.

## Beispiele

### Beispiel 1: Erstellen eines Sicherungsspeichers
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup01" -Name "Vault03" -Region "westus"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup01/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

Mit diesem Befehl wird ein Azure Backup Vault mit dem Namen "Vault03" erstellt.
Der Tresor befindet sich in der Ressourcengruppe namens ResourceGroup01 in der Region West USA.
Im Tresor wird der standardmäßige georedundante Speichertyp verwendet.

### Beispiel 2: Erstellen eines Sicherungs Depots, in dem lokal redundanter Speicher verwendet wird
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup02" -Name "Vault03" -Region "westus" -Storage LocallyRedundant
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup02/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup02
Region            : westus
Storage           : LocallyRedundant
```

Mit diesem Befehl wird ein Azure Backup Vault mit dem Namen "Vault03" erstellt.
Der Tresor befindet sich in der Ressourcengruppe namens ResourceGroup02 in der Region West USA.
Im Tresor wird der LocallyRedundant-Speichertyp verwendet.

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

### -Name
Gibt einen Namen für den Azure Backup Vault an.
Der Name muss in einer Ressourcengruppe eindeutig sein.

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

### -Region
Gibt einen Azure-Bereich an, in dem der sicherungstresor vorhanden ist.
Für Szenarien mit Hybrid-Backup empfehlen wir, dass Sie einen Tresor in einer Region in der Nähe des lokalen Servers erstellen, um die Latenz zu verringern.
Für Backups von Azure Infrastructure as a Service (IaaS) Virtual Machines wird der Tresor zum Ermittlungspunkt für lokale virtuelle Maschinen.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer vorhandenen Azure-Ressourcengruppe an, in der mit diesem Cmdlet ein Sicherungsspeicher erstellt wird.
Verwenden Sie das New-AzureRMResourceGroup-Cmdlet, um eine Ressourcengruppe zu erstellen.
Die Ressourcengruppe und der Azure Backup Vault müssen sich nicht in der gleichen Region befinden.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Speicher
Gibt den Speichertyp für die Sicherungsdaten an.
Die zulässigen Werte für diesen Parameter sind: LocallyRedundant und georedundant.
Der Standardwert ist georedundant.

```yaml
Type: AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases: 
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### AzureRmBackupVault

## Notizen
* Keine

## Verwandte Links

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Remove-AzureRmBackupVault](./Remove-AzureRmBackupVault.md)

[Satz-AzureRmBackupVault](./Set-AzureRmBackupVault.md)


