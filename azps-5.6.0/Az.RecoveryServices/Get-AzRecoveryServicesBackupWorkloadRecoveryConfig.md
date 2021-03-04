---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: d608b4265435041a918ba71cdd68ae00892bcc20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922355"
---
# <span data-ttu-id="99f05-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="99f05-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="99f05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99f05-102">SYNOPSIS</span></span>
<span data-ttu-id="99f05-103">Dieser Befehl erstellt die Wiederherstellungskonfiguration eines gesicherten Elements wie SQL DB.</span><span class="sxs-lookup"><span data-stu-id="99f05-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="99f05-104">Das Konfigurationsobjekt speichert alle Details wie den Wiederherstellungsmodus, Zielziele für die Wiederherstellung und anwendungsspezifische Parameter wie physische Zielpfade für SQL.</span><span class="sxs-lookup"><span data-stu-id="99f05-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="99f05-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99f05-105">SYNTAX</span></span>

### <span data-ttu-id="99f05-106">RpParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="99f05-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99f05-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="99f05-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99f05-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="99f05-108">DESCRIPTION</span></span>
<span data-ttu-id="99f05-109">Der Befehl gibt eine Wiederherstellungskonfiguration für AzureWorkload-Elemente zurück, die an das Cmdlet für die Wiederherstellung übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="99f05-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="99f05-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="99f05-110">EXAMPLES</span></span>

### <span data-ttu-id="99f05-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="99f05-111">Example 1</span></span>
```powershell
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="99f05-112">Das erste Cmdlet wird verwendet, um das Wiederherstellungspunktobjekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="99f05-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="99f05-113">Das zweite Cmdlet erstellt einen Wiederherstellungsplan für eine ursprüngliche Speicherortwiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="99f05-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="99f05-114">Das dritte Cmdlet erstellt einen Wiederherstellungsplan für eine alternative Standortwiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="99f05-114">THe third cmdlet creates a recovery plan for a alternate location restore.</span></span>

### <span data-ttu-id="99f05-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="99f05-115">Example 2</span></span>

<span data-ttu-id="99f05-116">Dieser Befehl erstellt die Wiederherstellungskonfiguration eines gesicherten Elements wie SQL DB.</span><span class="sxs-lookup"><span data-stu-id="99f05-116">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="99f05-117">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="99f05-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -AlternateWorkloadRestore -RecoveryPoint $rp[0] -TargetItem <ProtectableItemBase> -VaultId $vault.ID
```

## <span data-ttu-id="99f05-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="99f05-118">PARAMETERS</span></span>

### <span data-ttu-id="99f05-119">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="99f05-119">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="99f05-120">Gibt an, dass der gesicherte DB auf einem anderen ausgewählten Server wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="99f05-120">Specifies that the backed up DB should be restored onto another selected server.</span></span>

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

### <span data-ttu-id="99f05-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99f05-121">-DefaultProfile</span></span>
<span data-ttu-id="99f05-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="99f05-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99f05-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="99f05-123">-FilePath</span></span>
<span data-ttu-id="99f05-124">Gibt den Filepath an, der für den Wiederherstellungsvorgang verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="99f05-124">Specifies the filepath which is used for restore operation.</span></span>

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

### <span data-ttu-id="99f05-125">-FromFull</span><span class="sxs-lookup"><span data-stu-id="99f05-125">-FromFull</span></span>
<span data-ttu-id="99f05-126">Gibt den Vollständigen Wiederherstellungspoint an, auf den Protokollsicherungen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="99f05-126">Specifies the Full RecoveryPoint to which Log backups will be applied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99f05-127">-Item</span><span class="sxs-lookup"><span data-stu-id="99f05-127">-Item</span></span>
<span data-ttu-id="99f05-128">Gibt das Sicherungselement an, für das der Wiederherstellungsvorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="99f05-128">Specifies the backup item on which the restore operation is being performed.</span></span>

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

### <span data-ttu-id="99f05-129">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="99f05-129">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="99f05-130">Gibt an, dass der gesicherte DB mit den DB-Informationen überschrieben werden soll, die im Wiederherstellungspunkt vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="99f05-130">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="99f05-131">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="99f05-131">-PointInTime</span></span>
<span data-ttu-id="99f05-132">Endzeit des Zeitbereichs, für den der Wiederherstellungspunkt abgerufen werden muss</span><span class="sxs-lookup"><span data-stu-id="99f05-132">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="99f05-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="99f05-133">-RecoveryPoint</span></span>
<span data-ttu-id="99f05-134">Wiederherstellungspunktobjekt, das wiederhergestellt werden soll</span><span class="sxs-lookup"><span data-stu-id="99f05-134">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="99f05-135">-RestoreAsFiles</span><span class="sxs-lookup"><span data-stu-id="99f05-135">-RestoreAsFiles</span></span>
<span data-ttu-id="99f05-136">Gibt an, dass Datenbank als Dateien auf einem Computer wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="99f05-136">Specifies to restore Database as files in a machine.</span></span>

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

### <span data-ttu-id="99f05-137">-TargetContainer</span><span class="sxs-lookup"><span data-stu-id="99f05-137">-TargetContainer</span></span>
<span data-ttu-id="99f05-138">Gibt den Zielcomputer an, auf dem DB-Dateien wiederhergestellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="99f05-138">Specifies the target machine on which DB Files need to be restored.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99f05-139">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="99f05-139">-TargetItem</span></span>
<span data-ttu-id="99f05-140">Gibt das Ziel an, für das die DB wiederhergestellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="99f05-140">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="99f05-141">Für SQL wiederherzustellen, muss es nur vom beschützbaren Elementtyp SQLInstance sein.</span><span class="sxs-lookup"><span data-stu-id="99f05-141">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

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

### <span data-ttu-id="99f05-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="99f05-142">-VaultId</span></span>
<span data-ttu-id="99f05-143">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="99f05-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="99f05-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99f05-144">CommonParameters</span></span>
<span data-ttu-id="99f05-145">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99f05-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99f05-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99f05-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99f05-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="99f05-147">INPUTS</span></span>

### <span data-ttu-id="99f05-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="99f05-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="99f05-149">System.String</span><span class="sxs-lookup"><span data-stu-id="99f05-149">System.String</span></span>

## <span data-ttu-id="99f05-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="99f05-150">OUTPUTS</span></span>

### <span data-ttu-id="99f05-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="99f05-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="99f05-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="99f05-152">NOTES</span></span>

## <span data-ttu-id="99f05-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="99f05-153">RELATED LINKS</span></span>
