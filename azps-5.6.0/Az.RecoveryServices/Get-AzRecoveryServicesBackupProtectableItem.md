---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 1d14a1559d62f00b4a513c6a25dad28b7816e2d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938512"
---
# Get-AzRecoveryServicesBackupProtectableItem

## SYNOPSIS
Mit diesem Befehl werden alle schützensbaren Elemente in einem bestimmten Container oder in allen registrierten Containern abgerufen. Sie besteht aus allen Elementen der Hierarchie der Anwendung. Gibt DBs und deren Entitäten der oberen Ebene zurück, z. B. Instanz, AvailabilityGroup usw.

## SYNTAX

### NoFilterParamSet (Standard)
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FilterParamSet
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [[-ItemType] <ProtectableItemType>] [-Name <String>] [-ServerName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### IdParamSet
```
Get-AzRecoveryServicesBackupProtectableItem [-ParentID] <String> [[-ItemType] <ProtectableItemType>]
 [-Name <String>] [-ServerName <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzRecoveryServicesBackupProtectableItem-Cmdlet** ruft die Liste der schützenbaren Elemente in einem Container und den Schutzstatus der Elemente ab.
Ein Container, der bei einem Azure Recovery Services-Tresor registriert ist, kann ein oder mehrere Elemente enthalten, die geschützt werden können.

## BEISPIELE

### Beispiel 1
```
PS C:\> $Vault = Get-AzRecoveryServicesVault -Name "MyRecoveryVault"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer -Status Registered -VaultId $Vault.Id
PS C:\> $Item = Get-AzRecoveryServicesBackupProtectableItem -Container $Container -ItemType "SQLInstance" -WorkloadType "MSSQL" -VaultId $Vault.ID
```

Der erste Befehl ruft den Container vom Typ MSSQL ab und speichert ihn dann in der $Container Variablen.
Der zweite Befehl ruft das sicherungsschutzbare Element in $Container ab und speichert es dann in der $Item Variablen.

## PARAMETER

### -Container
Container, in dem sich das Element befindet

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: NoFilterParamSet, FilterParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -ItemType
Gibt den Typ des beschützbaren Elements an. Anwendbare Werte: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemType
Parameter Sets: FilterParamSet, IdParamSet
Aliases:
Accepted values: SQLDataBase, SQLInstance, SQLAvailabilityGroup

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen der Datenbank, Instanz oder Verfügbarkeitsgruppe an.

```yaml
Type: System.String
Parameter Sets: FilterParamSet, IdParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParentID
Gibt die ARM-ID einer Instanz oder AG an.

```yaml
Type: System.String
Parameter Sets: IdParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Servername
Gibt den Namen des Servers an, zu dem das Element gehört.

```yaml
Type: System.String
Parameter Sets: FilterParamSet, IdParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultId
ARM-ID des Wiederherstellungsdienste-Tresors.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WorkloadType
Arbeitsauslastungstyp der Ressource. Die aktuellen unterstützten Werte sind AzureVM, WindowsServer, AzureFiles, MSSQL.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: NoFilterParamSet, FilterParamSet
Aliases:
Accepted values: AzureVM, WindowsServer, AzureFiles, MSSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
System.String

## AUSGABEN

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase

## NOTIZEN

## VERWANDTE LINKS
