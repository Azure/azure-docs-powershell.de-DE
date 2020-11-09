---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 4209755de3475b21405fafd7f1e769bbbe3f7718
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303001"
---
# <span data-ttu-id="53669-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="53669-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="53669-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="53669-102">SYNOPSIS</span></span>
<span data-ttu-id="53669-103">Dieser Befehl erstellt die Wiederherstellungskonfiguration eines gesicherten Elements wie SQL DB.</span><span class="sxs-lookup"><span data-stu-id="53669-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="53669-104">Das Configuration-Objekt speichert alle Details wie den Wiederherstellungsmodus, Ziel Ziele für die Wiederherstellungs-und anwendungsspezifischen Parameter wie physische Ziel Pfade für SQL.</span><span class="sxs-lookup"><span data-stu-id="53669-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="53669-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="53669-105">SYNTAX</span></span>

### <span data-ttu-id="53669-106">RpParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="53669-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53669-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="53669-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53669-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="53669-108">DESCRIPTION</span></span>
<span data-ttu-id="53669-109">Der Befehl gibt eine Wiederherstellungskonfiguration für AzureWorkload-Elemente zurück, die an das Restore-Cmdlet übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="53669-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="53669-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53669-110">EXAMPLES</span></span>

### <span data-ttu-id="53669-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="53669-111">Example 1</span></span>
```powershell
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="53669-112">Das erste Cmdlet wird verwendet, um das Wiederherstellungspunkt Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="53669-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="53669-113">Das zweite Cmdlet erstellt einen Wiederherstellungsplan für eine ursprüngliche Standortwiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="53669-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="53669-114">Das dritte Cmdlet erstellt einen Wiederherstellungsplan für eine Alternative Standortwiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="53669-114">THe third cmdlet creates a recovery plan for a alternate location restore.</span></span>

### <span data-ttu-id="53669-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="53669-115">Example 2</span></span>

<span data-ttu-id="53669-116">Dieser Befehl erstellt die Wiederherstellungskonfiguration eines gesicherten Elements wie SQL DB.</span><span class="sxs-lookup"><span data-stu-id="53669-116">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="53669-117">automatisch</span><span class="sxs-lookup"><span data-stu-id="53669-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -AlternateWorkloadRestore -RecoveryPoint $rp[0] -TargetItem <ProtectableItemBase> -VaultId $vault.ID
```

## <span data-ttu-id="53669-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="53669-118">PARAMETERS</span></span>

### <span data-ttu-id="53669-119">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="53669-119">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="53669-120">Gibt an, dass die gesicherte Datenbank auf einem anderen ausgewählten Server wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="53669-120">Specifies that the backed up DB should be restored onto another selected server.</span></span>

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

### <span data-ttu-id="53669-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53669-121">-DefaultProfile</span></span>
<span data-ttu-id="53669-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="53669-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53669-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="53669-123">-FilePath</span></span>
<span data-ttu-id="53669-124">Gibt den Dateipfad an, der für den Wiederherstellungsvorgang verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="53669-124">Specifies the filepath which is used for restore operation.</span></span>

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

### <span data-ttu-id="53669-125">-FromFull</span><span class="sxs-lookup"><span data-stu-id="53669-125">-FromFull</span></span>
<span data-ttu-id="53669-126">Gibt den vollständigen RecoveryPoint an, auf den Protokollsicherungen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="53669-126">Specifies the Full RecoveryPoint to which Log backups will be applied.</span></span>

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

### <span data-ttu-id="53669-127">-Item</span><span class="sxs-lookup"><span data-stu-id="53669-127">-Item</span></span>
<span data-ttu-id="53669-128">Gibt das Sicherungselement an, für das der Wiederherstellungsvorgang durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="53669-128">Specifies the backup item on which the restore operation is being performed.</span></span>

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

### <span data-ttu-id="53669-129">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="53669-129">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="53669-130">Gibt an, dass die gesicherte DB mit den im Wiederherstellungspunkt vorhandenen DB-Informationen überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="53669-130">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="53669-131">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="53669-131">-PointInTime</span></span>
<span data-ttu-id="53669-132">Endzeit des Zeitbereichs, für den der Wiederherstellungspunkt abgerufen werden muss</span><span class="sxs-lookup"><span data-stu-id="53669-132">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="53669-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="53669-133">-RecoveryPoint</span></span>
<span data-ttu-id="53669-134">Wiederherstellungspunkt Objekt, das wiederhergestellt werden soll</span><span class="sxs-lookup"><span data-stu-id="53669-134">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="53669-135">-RestoreAsFiles</span><span class="sxs-lookup"><span data-stu-id="53669-135">-RestoreAsFiles</span></span>
<span data-ttu-id="53669-136">Gibt an, dass die Datenbank als Dateien auf einem Computer wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="53669-136">Specifies to restore Database as files in a machine.</span></span>

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

### <span data-ttu-id="53669-137">-Zielcontainer</span><span class="sxs-lookup"><span data-stu-id="53669-137">-TargetContainer</span></span>
<span data-ttu-id="53669-138">Gibt den Zielcomputer an, auf dem DB-Dateien wiederhergestellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="53669-138">Specifies the target machine on which DB Files need to be restored.</span></span>

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

### <span data-ttu-id="53669-139">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="53669-139">-TargetItem</span></span>
<span data-ttu-id="53669-140">Gibt das Ziel an, auf dem die DB wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="53669-140">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="53669-141">Bei SQL-Wiederherstellungen muss es sich um einen geschützten Elementtyp SQLInstance handeln.</span><span class="sxs-lookup"><span data-stu-id="53669-141">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

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

### <span data-ttu-id="53669-142">-Tresor</span><span class="sxs-lookup"><span data-stu-id="53669-142">-VaultId</span></span>
<span data-ttu-id="53669-143">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="53669-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="53669-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53669-144">CommonParameters</span></span>
<span data-ttu-id="53669-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53669-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53669-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53669-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53669-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="53669-147">INPUTS</span></span>

### <span data-ttu-id="53669-148">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="53669-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="53669-149">System. String</span><span class="sxs-lookup"><span data-stu-id="53669-149">System.String</span></span>

## <span data-ttu-id="53669-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="53669-150">OUTPUTS</span></span>

### <span data-ttu-id="53669-151">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="53669-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="53669-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="53669-152">NOTES</span></span>

## <span data-ttu-id="53669-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="53669-153">RELATED LINKS</span></span>
