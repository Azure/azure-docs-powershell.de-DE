---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 95FF3F7A-5CC6-4AA6-A393-5EBB5579D9A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
ms.openlocfilehash: ef4d8ca2e1fb21165281375b3d325f5fc8b6ceed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479938"
---
# Get-AzureRmBackupVault

## Synopsis
Ruft Sicherungs Depots ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmBackupVault [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmBackupVault** " ruft Azure Backup Vaults ab.
Dieses Cmdlet gibt **AzureRmBackupVault** -Objekte zur Verwendung mit anderen Cmdlets zurück.

## Beispiele

### Beispiel 1: Anzeigen aller Sicherungs Depots
```
PS C:\>Get-AzureRmBackupVault
```

Dieser Befehl ruft alle Azure Backup Vaults ab.

### Beispiel 2: Anzeigen aller in West-US erstellten Tresore
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Region -eq "westus" }
```

Dieser Befehl ruft alle Sicherungs Depots ab.
Der Befehl übergibt Sie mithilfe des Pipelineoperators an das Where-Object-Cmdlet.
Dieses Cmdlet filtert die Ergebnisse basierend auf der **Region** -Eigenschaft.
Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Where-Object` .

### Beispiel 3: Abrufen eines bestimmten Tresors
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup011/providers/Microsoft.Backup
                    /BackupVault/Vault
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

Dieser Befehl ruft den Tresor mit dem Namen Vault03 ab.

### Beispiel 4: zählen der Anzahl von Tresoren, die über lokal redundanten Speicher verfügen
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Storage -match "LocallyRedundant" } | Measure-Object
Count    : 4
Average  : 
Sum      : 
Maximum  : 
Minimum  : 
Property :
```

Dieser Befehl ruft alle Azure Backup Vaults ab.
Der Befehl übergibt sie an **Where-Object** , wodurch die Ergebnisse basierend auf der **Speicher** Eigenschaft gefiltert werden.
Der Befehl übergibt diejenigen, die einen Wert von LocallyRedundant haben, an das Measure-Object-Cmdlet, in dem die Ergebnisse gezählt werden.
Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Measure-Object` .

## Parameter

### -Name
Gibt den Namen des Sicherungsspeichers an, den dieses Cmdlet erhält.
Wenn mehr als ein Backup Vault denselben Namen hat, gibt dieses Cmdlet alle zurück.
Geben Sie den *ResourceGroupName* -Parameter an, um einen eindeutigen Tresor abzurufen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Azure-Ressourcengruppe an, in der dieses Cmdlet einen Sicherungsspeicher erhält.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
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

## Ausgaben

### AzureRmBackupVault

## Notizen
* Keine

## Verwandte Links

[Get-AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[Neu – AzureRmBackupVault](./New-AzureRmBackupVault.md)

[Remove-AzureRmBackupVault](./Remove-AzureRmBackupVault.md)

[Satz-AzureRmBackupVault](./Set-AzureRmBackupVault.md)


