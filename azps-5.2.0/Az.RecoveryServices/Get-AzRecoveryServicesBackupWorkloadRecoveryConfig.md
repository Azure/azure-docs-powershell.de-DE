---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 4209755de3475b21405fafd7f1e769bbbe3f7718
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294406"
---
# <span data-ttu-id="c2314-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="c2314-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="c2314-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2314-102">SYNOPSIS</span></span>
<span data-ttu-id="c2314-103">Dieser Befehl erstellt die Wiederherstellungskonfiguration eines gesicherten Elements wie SQL DB.</span><span class="sxs-lookup"><span data-stu-id="c2314-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="c2314-104">Das Konfigurationsobjekt speichert alle Details wie den Wiederherstellungsmodus, Zielziele für die Wiederherstellung und anwendungsspezifische Parameter wie physische Zielpfade für SQL.</span><span class="sxs-lookup"><span data-stu-id="c2314-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="c2314-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2314-105">SYNTAX</span></span>

### <span data-ttu-id="c2314-106">RpParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c2314-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2314-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2314-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2314-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c2314-108">DESCRIPTION</span></span>
<span data-ttu-id="c2314-109">Der Befehl gibt eine Wiederherstellungskonfiguration für AzureWorkload-Elemente zurück, die an das Cmdlet "Wiederherstellen" übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="c2314-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="c2314-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c2314-110">EXAMPLES</span></span>

### <span data-ttu-id="c2314-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c2314-111">Example 1</span></span>
```powershell
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="c2314-112">Das erste Cmdlet wird verwendet, um das Wiederherstellungspunktobjekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c2314-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="c2314-113">Das zweite Cmdlet erstellt einen Wiederherstellungsplan für eine Wiederherstellung des ursprünglichen Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="c2314-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="c2314-114">Das dritte Cmdlet erstellt einen Wiederherstellungsplan für die Wiederherstellung eines alternativen Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="c2314-114">THe third cmdlet creates a recovery plan for a alternate location restore.</span></span>

### <span data-ttu-id="c2314-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c2314-115">Example 2</span></span>

<span data-ttu-id="c2314-116">Dieser Befehl erstellt die Wiederherstellungskonfiguration eines gesicherten Elements wie SQL DB.</span><span class="sxs-lookup"><span data-stu-id="c2314-116">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="c2314-117">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="c2314-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -AlternateWorkloadRestore -RecoveryPoint $rp[0] -TargetItem <ProtectableItemBase> -VaultId $vault.ID
```

## <span data-ttu-id="c2314-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2314-118">PARAMETERS</span></span>

### <span data-ttu-id="c2314-119">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="c2314-119">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="c2314-120">Gibt an, dass die gesicherte DB auf einem anderen ausgewählten Server wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2314-120">Specifies that the backed up DB should be restored onto another selected server.</span></span>

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

### <span data-ttu-id="c2314-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2314-121">-DefaultProfile</span></span>
<span data-ttu-id="c2314-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2314-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2314-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="c2314-123">-FilePath</span></span>
<span data-ttu-id="c2314-124">Gibt den filepath-Pfad an, der für den Wiederherstellungsvorgang verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c2314-124">Specifies the filepath which is used for restore operation.</span></span>

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

### <span data-ttu-id="c2314-125">-FromFull</span><span class="sxs-lookup"><span data-stu-id="c2314-125">-FromFull</span></span>
<span data-ttu-id="c2314-126">Gibt den vollständigen Wiederherstellungspoint an, auf den Protokollsicherungen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2314-126">Specifies the Full RecoveryPoint to which Log backups will be applied.</span></span>

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

### <span data-ttu-id="c2314-127">-Item</span><span class="sxs-lookup"><span data-stu-id="c2314-127">-Item</span></span>
<span data-ttu-id="c2314-128">Gibt das Sicherungselement an, für das der Wiederherstellungsvorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2314-128">Specifies the backup item on which the restore operation is being performed.</span></span>

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

### <span data-ttu-id="c2314-129">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="c2314-129">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="c2314-130">Gibt an, dass die gesicherte DB mit den im Wiederherstellungspunkt vorhandenen DB-Informationen überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2314-130">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="c2314-131">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="c2314-131">-PointInTime</span></span>
<span data-ttu-id="c2314-132">Endzeit des Zeitbereichs, für den der Wiederherstellungspunkt abgerufen werden muss</span><span class="sxs-lookup"><span data-stu-id="c2314-132">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="c2314-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="c2314-133">-RecoveryPoint</span></span>
<span data-ttu-id="c2314-134">Wiederherstellungspunktobjekt, das wiederhergestellt werden soll</span><span class="sxs-lookup"><span data-stu-id="c2314-134">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="c2314-135">-RestoreAsFiles</span><span class="sxs-lookup"><span data-stu-id="c2314-135">-RestoreAsFiles</span></span>
<span data-ttu-id="c2314-136">Gibt an, dass eine Datenbank als Dateien auf einem Computer wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2314-136">Specifies to restore Database as files in a machine.</span></span>

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

### <span data-ttu-id="c2314-137">-TargetContainer</span><span class="sxs-lookup"><span data-stu-id="c2314-137">-TargetContainer</span></span>
<span data-ttu-id="c2314-138">Gibt den Zielcomputer an, auf dem die DB Files wiederhergestellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c2314-138">Specifies the target machine on which DB Files need to be restored.</span></span>

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

### <span data-ttu-id="c2314-139">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="c2314-139">-TargetItem</span></span>
<span data-ttu-id="c2314-140">Gibt das Ziel an, für das die DB wiederhergestellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="c2314-140">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="c2314-141">Damit SQL wiederhergestellt werden können, muss es nur vom typ "SQLInstance" des geschützten Elements sein.</span><span class="sxs-lookup"><span data-stu-id="c2314-141">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

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

### <span data-ttu-id="c2314-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="c2314-142">-VaultId</span></span>
<span data-ttu-id="c2314-143">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="c2314-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="c2314-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2314-144">CommonParameters</span></span>
<span data-ttu-id="c2314-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2314-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2314-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2314-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2314-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c2314-147">INPUTS</span></span>

### <span data-ttu-id="c2314-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="c2314-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="c2314-149">System.String</span><span class="sxs-lookup"><span data-stu-id="c2314-149">System.String</span></span>

## <span data-ttu-id="c2314-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c2314-150">OUTPUTS</span></span>

### <span data-ttu-id="c2314-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="c2314-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="c2314-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c2314-152">NOTES</span></span>

## <span data-ttu-id="c2314-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c2314-153">RELATED LINKS</span></span>
