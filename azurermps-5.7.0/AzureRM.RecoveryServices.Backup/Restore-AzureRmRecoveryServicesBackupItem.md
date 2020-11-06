---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/restore-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: 6013531367f5996924da1776c0062ebb5ad02b90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478337"
---
# <span data-ttu-id="5c714-101">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="5c714-101">Restore-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="5c714-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5c714-102">SYNOPSIS</span></span>
<span data-ttu-id="5c714-103">Wiederherstellen der Daten und der Konfiguration für ein Sicherungselement an einem Wiederherstellungspunkt</span><span class="sxs-lookup"><span data-stu-id="5c714-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c714-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c714-104">SYNTAX</span></span>

```
Restore-AzureRmRecoveryServicesBackupItem [-RecoveryPoint] <RecoveryPointBase> [-StorageAccountName] <String>
 [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c714-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c714-105">DESCRIPTION</span></span>
<span data-ttu-id="5c714-106">Das Cmdlet **Restore-AzureRmRecoveryServicesBackupItem** stellt die Daten und die Konfiguration für ein Azure Backup-Element an einem angegebenen Wiederherstellungspunkt wieder her.</span><span class="sxs-lookup"><span data-stu-id="5c714-106">The **Restore-AzureRmRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="5c714-107">Mit diesem Cmdlet wird die Wiederherstellung aus dem Vault für Wiederherstellungsdienste auf dem Speicherkonto des Kunden gestartet.</span><span class="sxs-lookup"><span data-stu-id="5c714-107">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>

<span data-ttu-id="5c714-108">Beim Wiederherstellungsvorgang wird der vollständige virtuelle Computer nicht wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="5c714-108">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="5c714-109">Die Datenträgerdaten und Konfigurationsinformationen werden wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="5c714-109">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="5c714-110">Nach Abschluss des Wiederherstellungsvorgangs müssen Sie den virtuellen Computer erstellen und starten.</span><span class="sxs-lookup"><span data-stu-id="5c714-110">After the restore operation is finished, you must create the virtual machine and start it.</span></span>

<span data-ttu-id="5c714-111">Setzen Sie den Vault-Kontext mithilfe des Set-AzureRmRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="5c714-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="5c714-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5c714-112">EXAMPLES</span></span>

### <span data-ttu-id="5c714-113">Beispiel 1: Wiederherstellen eines Elements in einem Wiederherstellungspunkt</span><span class="sxs-lookup"><span data-stu-id="5c714-113">Example 1: Restore an item to a recovery point</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() 
PS C:\> $RestoreJob = Restore-AzureRmRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG"
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="5c714-114">Der erste Befehl ruft den Sicherungs Container des Typs AzureVM ab und speichert ihn dann in der $Container Variablen.</span><span class="sxs-lookup"><span data-stu-id="5c714-114">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="5c714-115">Der zweite Befehl ruft das Sicherungselement mit dem Namen V2VM aus $Container ab und speichert es dann in der $BackupItem-Variablen.</span><span class="sxs-lookup"><span data-stu-id="5c714-115">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>

<span data-ttu-id="5c714-116">Der dritte Befehl ruft das Datum ab sieben Tage zuvor ab und speichert es dann in der $StartDate Variablen.</span><span class="sxs-lookup"><span data-stu-id="5c714-116">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>

<span data-ttu-id="5c714-117">Der vierte Befehl ruft das aktuelle Datum ab und speichert es dann in der $EndDate Variablen.</span><span class="sxs-lookup"><span data-stu-id="5c714-117">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>

<span data-ttu-id="5c714-118">Der fünfte Befehl ruft eine Liste der Wiederherstellungspunkte für das jeweilige Sicherungselement ab, das nach $StartDate und $EndDate gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="5c714-118">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="5c714-119">Der angegebene Datumsbereich ist die letzten 7 Tage.</span><span class="sxs-lookup"><span data-stu-id="5c714-119">The date range specified is the last 7 days.</span></span>

<span data-ttu-id="5c714-120">Mit dem letzten Befehl werden die Datenträger auf dem Zielspeicher Konto DestAccount in der DestRG-Ressourcengruppe wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="5c714-120">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="5c714-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c714-121">PARAMETERS</span></span>

### <span data-ttu-id="5c714-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c714-122">-DefaultProfile</span></span>
<span data-ttu-id="5c714-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5c714-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c714-124">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="5c714-124">-RecoveryPoint</span></span>
<span data-ttu-id="5c714-125">Gibt den Wiederherstellungspunkt an, auf den der virtuelle Computer wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5c714-125">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="5c714-126">Verwenden Sie das Get-AzureRmRecoveryServicesBackupRecoveryPoint-Cmdlet, um ein **AzureRmRecoveryServicesBackupRecoveryPoint** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5c714-126">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the Get-AzureRmRecoveryServicesBackupRecoveryPoint cmdlet.</span></span>

```yaml
Type: RecoveryPointBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c714-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5c714-127">-StorageAccountName</span></span>
<span data-ttu-id="5c714-128">Gibt den Namen des Zielspeicher Kontos in Ihrem Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="5c714-128">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="5c714-129">Im Rahmen des Wiederherstellungsvorgangs speichert dieses Cmdlet die Datenträger und die Konfigurationsinformationen in diesem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="5c714-129">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="5c714-130">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c714-130">-StorageAccountResourceGroupName</span></span>
<span data-ttu-id="5c714-131">Gibt den Namen der Ressourcengruppe an, die das Zielspeicher Konto in Ihrem Abonnement enthält.</span><span class="sxs-lookup"><span data-stu-id="5c714-131">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="5c714-132">Im Rahmen des Wiederherstellungsvorgangs speichert dieses Cmdlet die Datenträger und die Konfigurationsinformationen in diesem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="5c714-132">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="5c714-133">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5c714-133">-UseOriginalStorageAccount</span></span>
<span data-ttu-id="5c714-134">Verwenden Sie diese Option, wenn die Datenträger des Wiederherstellungspunkts auf ihren ursprünglichen Speicherkonten wiederhergestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5c714-134">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c714-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5c714-135">-Confirm</span></span>
<span data-ttu-id="5c714-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5c714-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c714-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c714-137">-WhatIf</span></span>
<span data-ttu-id="5c714-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5c714-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5c714-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5c714-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c714-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c714-140">CommonParameters</span></span>
<span data-ttu-id="5c714-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c714-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c714-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c714-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c714-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5c714-143">INPUTS</span></span>

### <span data-ttu-id="5c714-144">RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="5c714-144">RecoveryPointBase</span></span>
<span data-ttu-id="5c714-145">Der Parameter "RecoveryPoint" akzeptiert den Wert vom Typ "RecoveryPointBase" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5c714-145">Parameter 'RecoveryPoint' accepts value of type 'RecoveryPointBase' from the pipeline</span></span>

## <span data-ttu-id="5c714-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5c714-146">OUTPUTS</span></span>

### <span data-ttu-id="5c714-147">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="5c714-147">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="5c714-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="5c714-148">NOTES</span></span>

## <span data-ttu-id="5c714-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5c714-149">RELATED LINKS</span></span>

[<span data-ttu-id="5c714-150">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="5c714-150">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="5c714-151">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="5c714-151">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="5c714-152">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="5c714-152">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)


