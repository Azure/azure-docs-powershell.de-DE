---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 8A638FB1-F530-4E28-BAAE-5382671092C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupItem.md
ms.openlocfilehash: 892e9385a34f9c02ddcf41d57578bb320d645e0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505550"
---
# Get-AzureRmBackupItem

## Synopsis
Ruft die Elemente unter einem Container in Backup ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmBackupItem [-ProtectionStatus <String>] [-Status <String>] [-Type <String>]
 [-Container] <AzureRMBackupContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Get-AzureRmBackupItem werden** die Elemente in einem Container in Azure Backup und der Schutzstatus der Elemente abgerufen.
Aktivieren Sie Elemente für den Schutz mithilfe des Enable-AzureRmBackupProtection-Cmdlets.

Ein Container, der für einen sicherungstresor registriert ist, kann ein oder mehrere Elemente enthalten, die geschützt werden können.
Für Azure Virtual Machines kann nur ein Element im Container für virtuelle Maschinen vorhanden sein.

## Beispiele

### Beispiel 1: Abrufen der Elemente in einem Container
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container
Name                    ProtectionStatus       DataSourceStatus       RecoveryPointsCount    ProtectionPolicyName
----                    ----------------       ----------------       -------------------    --------------------
co03-vm                 NotProtected                                  0
```

Der erste Befehl ruft den Tresor mit dem Namen Vault03 mithilfe des Get-AzureRmBackupVault-Cmdlets ab.
Der Befehl speichert das Objekt in der $Vault Variablen.

Der zweite Befehl ruft mit dem Cmdlet **Get-AzureRmBackupContainer** einen Container mit dem angegebenen Namen im Tresor in $Vault ab.
Der Befehl speichert das Objekt in der $Container Variablen.

Der endgültige Befehl ruft das Sicherungselement im Container in $Container ab.

### Beispiel 2: Anzeigen aller Eigenschaften für ein Element
```
PS C:\>Get-AzureRmBackupItem -Container $Container | Select-Object -Property *
Name                 : co03-vm
DataSourceStatus     : 
ProtectionStatus     : NotProtected
Type                 : AzureVM
ProtectionPolicyName : 
ProtectionPolicyId   : 
RecoveryPointsCount  : 0
ItemName             : iaasvmcontainer;co03-vm;co03-vm
ContainerType        : AzureVM
ContainerUniqueName  : iaasvmcontainer;co03-vm;co03-vm
ResourceGroupName    : resourcegroup02
ResourceName         : vault03
Location             : southeastasia
```

Dieser Befehl ruft das Sicherungselement im Container in $Container ab und übergibt es dann an das Cmdlet Select-Object.
Dieses Cmdlet gibt alle Eigenschaften des sicherungselements zurück.
Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Select-Object` .

## Parameter

### -Container
Gibt ein Containerobjekt an, für das dieses Cmdlet Sicherungselemente erhält.
Verwenden Sie zum Abrufen eines **AzureRmBackupContainer** das Get-AzureRmBackupContainer-Cmdlet.

```yaml
Type: AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

### -ProtectionStatus
Gibt den allgemeinen Schutzstatus eines Elements im Container an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Geschützten 
- Schutz  
- NotProtected

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Protected, Protecting, NotProtected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status
Gibt den Sicherungsstatus für ein Element an.
Die zulässigen Werte für diesen Parameter sind: IRPending, protected, ProtectionError und ProtectionStopped.
Wenn der Wert des *ProtectionStatus* -Parameters geschützt ist, können Sie den *Status* -Parameterwert verwenden, um Elemente zu filtern.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IRPending, ProtectionStopped, ProtectionError, Protected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Typ
Gibt den Typ des Elements an, das dieses Cmdlet erhält.
Derzeit ist der einzige unterstützte Wert AzureVM.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### AzureRmBackupContainer

## Ausgaben

### AzureRmBackupItem

## Notizen

## Verwandte Links

[Backup-AzureRmBackupItem](./Backup-AzureRmBackupItem.md)

[Deaktivieren-AzureRmBackupProtection](./Disable-AzureRmBackupProtection.md)

[Enable-AzureRmBackupProtection](./Enable-AzureRmBackupProtection.md)

[Get-AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Wiederherstellen – AzureRmBackupItem](./Restore-AzureRmBackupItem.md)


