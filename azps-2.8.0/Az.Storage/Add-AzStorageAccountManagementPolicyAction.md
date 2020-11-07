---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/add-Azstorageaccountmanagementpolicyaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
ms.openlocfilehash: 73384827b5af2b3370eca1eee5a90066a89b8e55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826372"
---
# Add-AzStorageAccountManagementPolicyAction

## Synopsis
Fügt dem Eingabe ManagementPolicy-Aktionsgruppen Objekt eine Aktion hinzu oder erstellt ein ManagementPolicy-Aktionsgruppen Objekt mit der Aktion. Das Objekt kann in New-AzStorageAccountManagementPolicyRule verwendet werden.

## Syntax

### BaseBlob (Standard)
```
Add-AzStorageAccountManagementPolicyAction -BaseBlobAction <String> -DaysAfterModificationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Snapshot
```
Add-AzStorageAccountManagementPolicyAction -SnapshotAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das **Add-AzStorageAccountManagementPolicyAction-** Cmdlet fügt dem Eingabe ManagementPolicy-Aktionsgruppen Objekt eine Aktion hinzu oder erstellt ein ManagementPolicy-Aktionsgruppen Objekt mit der Aktion.

## Beispiele

### Beispiel 1: erstellt ein ManagementPolicy-Aktionsgruppen Objekt mit 4 Aktionen, fügt es dann einer Verwaltungsrichtlinien Regel hinzu und legt es auf ein Speicherkonto.
```
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50  -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30 -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100 -InputObject $action
PS C:\>$action 

BaseBlob.TierToCool.DaysAfterModificationGreaterThan    : 30
BaseBlob.TierToArchive.DaysAfterModificationGreaterThan : 50
BaseBlob.Delete.DaysAfterModificationGreaterThan        : 100
Snapshot.Delete.DaysAfterCreationGreaterThan            : 100

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

Mit dem ersten Befehl wird ein ManagementPolicy-Aktionsgruppen Objekt erstellt, mit den folgenden 3 Befehlen werden dem Objekt 3 Aktionen hinzugefügt. Fügen Sie es dann einer Verwaltungsrichtlinien Regel hinzu, und legen Sie es auf ein Speicherkonto.

## Parameter

### -BaseBlobAction
Die Verwaltungsrichtlinien Aktion für baseblob.

```yaml
Type: System.String
Parameter Sets: BaseBlob
Aliases:
Accepted values: Delete, TierToArchive, TierToCool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DaysAfterCreationGreaterThan
Ganzzahliger Wert, der das Alter in Tagen nach der Erstellung angibt.

```yaml
Type: System.Int32
Parameter Sets: Snapshot
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DaysAfterModificationGreaterThan
Ganzzahliger Wert, der das Alter in Tagen nach der letzten Änderung angibt.

```yaml
Type: System.Int32
Parameter Sets: BaseBlob
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inputobject
Wenn das ManagementPolicy-Aktionsobjekt eingegeben wird, wird die Aktion auf das Eingabe Aktionsobjekt gesetzt.
Wenn nicht eingegeben, wird ein neues Aktionsobjekt erstellt.

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Schnappschuss
Die Verwaltungsrichtlinien Aktion für Snapshot.

```yaml
Type: System.String
Parameter Sets: Snapshot
Aliases:
Accepted values: Delete

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. Management. Storage. Models. PSManagementPolicyActionGroup

## Ausgaben

### Microsoft. Azure. Commands. Management. Storage. Models. PSManagementPolicyActionGroup

## Notizen

## Verwandte Links
