---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 6b0f2e2c5b2e9579a92b2cee7387a19fda498fda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659889"
---
# <span data-ttu-id="c4333-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="c4333-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="c4333-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c4333-102">SYNOPSIS</span></span>
<span data-ttu-id="c4333-103">Dieser Befehl erstellt die Wiederherstellungskonfiguration eines gesicherten Elements wie SQL DB.</span><span class="sxs-lookup"><span data-stu-id="c4333-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="c4333-104">Das Configuration-Objekt speichert alle Details wie den Wiederherstellungsmodus, Ziel Ziele für die Wiederherstellungs-und anwendungsspezifischen Parameter wie physische Ziel Pfade für SQL.</span><span class="sxs-lookup"><span data-stu-id="c4333-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="c4333-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4333-105">SYNTAX</span></span>

### <span data-ttu-id="c4333-106">RpParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c4333-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4333-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4333-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4333-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4333-108">DESCRIPTION</span></span>
<span data-ttu-id="c4333-109">Der Befehl gibt eine Wiederherstellungskonfiguration für AzureWorkload-Elemente zurück, die an das Restore-Cmdlet übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="c4333-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="c4333-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4333-110">EXAMPLES</span></span>

### <span data-ttu-id="c4333-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c4333-111">Example 1</span></span>
```
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="c4333-112">Das erste Cmdlet wird verwendet, um das Wiederherstellungspunkt Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c4333-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="c4333-113">Das zweite Cmdlet erstellt einen Wiederherstellungsplan für eine ursprüngliche Standortwiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="c4333-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="c4333-114">Das dritte Cmdlet crreats einen Wiederherstellungsplan für eine Alternative Standortwiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="c4333-114">THe third cmdlet crreats a recovery plan for a alternate location restore.</span></span>

## <span data-ttu-id="c4333-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4333-115">PARAMETERS</span></span>

### <span data-ttu-id="c4333-116">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="c4333-116">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="c4333-117">Gibt an, dass die gesicherte DB mit den im Wiederherstellungspunkt vorhandenen DB-Informationen überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="c4333-117">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="c4333-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4333-118">-DefaultProfile</span></span>
<span data-ttu-id="c4333-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c4333-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4333-120">-Item</span><span class="sxs-lookup"><span data-stu-id="c4333-120">-Item</span></span>
<span data-ttu-id="c4333-121">Gibt das Sicherungselement an, für das der Wiederherstellungsvorgang durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c4333-121">Specifies the backup item on which the restore operation is being performed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4333-122">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="c4333-122">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="c4333-123">Gibt an, dass die gesicherte DB mit den im Wiederherstellungspunkt vorhandenen DB-Informationen überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="c4333-123">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="c4333-124">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="c4333-124">-PointInTime</span></span>
<span data-ttu-id="c4333-125">Endzeit des Zeitbereichs, für den der Wiederherstellungspunkt abgerufen werden muss</span><span class="sxs-lookup"><span data-stu-id="c4333-125">End time of Time range for which recovery point need to be fetched</span></span>

```yaml
Type: System.DateTime
Parameter Sets: LogChainParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4333-126">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="c4333-126">-RecoveryPoint</span></span>
<span data-ttu-id="c4333-127">Wiederherstellungspunkt Objekt, das wiederhergestellt werden soll</span><span class="sxs-lookup"><span data-stu-id="c4333-127">Recovery point object to be restored</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: RpParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4333-128">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="c4333-128">-TargetItem</span></span>
<span data-ttu-id="c4333-129">Gibt das Ziel an, auf dem die DB wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c4333-129">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="c4333-130">Bei SQL-Wiederherstellungen muss es sich um einen geschützten Elementtyp SQLInstance handeln.</span><span class="sxs-lookup"><span data-stu-id="c4333-130">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4333-131">-Tresor</span><span class="sxs-lookup"><span data-stu-id="c4333-131">-VaultId</span></span>
<span data-ttu-id="c4333-132">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="c4333-132">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="c4333-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c4333-133">-Confirm</span></span>
<span data-ttu-id="c4333-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c4333-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4333-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4333-135">-WhatIf</span></span>
<span data-ttu-id="c4333-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c4333-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4333-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4333-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4333-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4333-138">CommonParameters</span></span>
<span data-ttu-id="c4333-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4333-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4333-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4333-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4333-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c4333-141">INPUTS</span></span>

### <span data-ttu-id="c4333-142">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="c4333-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="c4333-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c4333-143">System.String</span></span>

## <span data-ttu-id="c4333-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c4333-144">OUTPUTS</span></span>

### <span data-ttu-id="c4333-145">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="c4333-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="c4333-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="c4333-146">NOTES</span></span>

## <span data-ttu-id="c4333-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c4333-147">RELATED LINKS</span></span>