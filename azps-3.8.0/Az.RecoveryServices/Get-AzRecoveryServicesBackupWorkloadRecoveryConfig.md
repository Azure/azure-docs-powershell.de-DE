---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 6033421b9a78e7cb531d2a33eabba1e97010c4f6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004926"
---
# <span data-ttu-id="b8d29-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="b8d29-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="b8d29-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b8d29-102">SYNOPSIS</span></span>
<span data-ttu-id="b8d29-103">Dieser Befehl erstellt die Wiederherstellungskonfiguration eines gesicherten Elements wie SQL DB.</span><span class="sxs-lookup"><span data-stu-id="b8d29-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="b8d29-104">Das Configuration-Objekt speichert alle Details wie den Wiederherstellungsmodus, Ziel Ziele für die Wiederherstellungs-und anwendungsspezifischen Parameter wie physische Ziel Pfade für SQL.</span><span class="sxs-lookup"><span data-stu-id="b8d29-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="b8d29-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8d29-105">SYNTAX</span></span>

### <span data-ttu-id="b8d29-106">RpParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b8d29-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8d29-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8d29-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8d29-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b8d29-108">DESCRIPTION</span></span>
<span data-ttu-id="b8d29-109">Der Befehl gibt eine Wiederherstellungskonfiguration für AzureWorkload-Elemente zurück, die an das Restore-Cmdlet übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="b8d29-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="b8d29-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b8d29-110">EXAMPLES</span></span>

### <span data-ttu-id="b8d29-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b8d29-111">Example 1</span></span>
```
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="b8d29-112">Das erste Cmdlet wird verwendet, um das Wiederherstellungspunkt Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b8d29-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="b8d29-113">Das zweite Cmdlet erstellt einen Wiederherstellungsplan für eine ursprüngliche Standortwiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="b8d29-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="b8d29-114">Das dritte Cmdlet erstellt einen Wiederherstellungsplan für eine Alternative Standortwiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="b8d29-114">THe third cmdlet creates a recovery plan for a alternate location restore.</span></span>

## <span data-ttu-id="b8d29-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8d29-115">PARAMETERS</span></span>

### <span data-ttu-id="b8d29-116">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="b8d29-116">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="b8d29-117">Gibt an, dass die gesicherte DB mit den im Wiederherstellungspunkt vorhandenen DB-Informationen überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8d29-117">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="b8d29-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8d29-118">-DefaultProfile</span></span>
<span data-ttu-id="b8d29-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b8d29-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8d29-120">-FilePath</span><span class="sxs-lookup"><span data-stu-id="b8d29-120">-FilePath</span></span>
<span data-ttu-id="b8d29-121">Gibt den filePath für den Wiederherstellungsvorgang an.</span><span class="sxs-lookup"><span data-stu-id="b8d29-121">Specifies the filepath for restore operation.</span></span>

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

### <span data-ttu-id="b8d29-122">-FromFull</span><span class="sxs-lookup"><span data-stu-id="b8d29-122">-FromFull</span></span>
<span data-ttu-id="b8d29-123">Gibt den vollständigen RecoveryPoint an, auf den Protokollsicherungen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8d29-123">Specifies the Full RecoveryPoint to which Log backups will be applied.</span></span>

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

### <span data-ttu-id="b8d29-124">-Item</span><span class="sxs-lookup"><span data-stu-id="b8d29-124">-Item</span></span>
<span data-ttu-id="b8d29-125">Gibt das Sicherungselement an, für das der Wiederherstellungsvorgang durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b8d29-125">Specifies the backup item on which the restore operation is being performed.</span></span>

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

### <span data-ttu-id="b8d29-126">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="b8d29-126">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="b8d29-127">Gibt an, dass die gesicherte DB mit den im Wiederherstellungspunkt vorhandenen DB-Informationen überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8d29-127">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="b8d29-128">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="b8d29-128">-PointInTime</span></span>
<span data-ttu-id="b8d29-129">Endzeit des Zeitbereichs, für den der Wiederherstellungspunkt abgerufen werden muss</span><span class="sxs-lookup"><span data-stu-id="b8d29-129">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="b8d29-130">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="b8d29-130">-RecoveryPoint</span></span>
<span data-ttu-id="b8d29-131">Wiederherstellungspunkt Objekt, das wiederhergestellt werden soll</span><span class="sxs-lookup"><span data-stu-id="b8d29-131">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="b8d29-132">-RestoreAsFiles</span><span class="sxs-lookup"><span data-stu-id="b8d29-132">-RestoreAsFiles</span></span>
<span data-ttu-id="b8d29-133">Gibt an, dass die Datenbank als Dateien auf einem Computer wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8d29-133">Specifies to restore Database as files in a machine.</span></span>

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

### <span data-ttu-id="b8d29-134">-Zielcontainer</span><span class="sxs-lookup"><span data-stu-id="b8d29-134">-TargetContainer</span></span>
<span data-ttu-id="b8d29-135">Gibt den Zielcomputer an, auf dem DB-Dateien wiederhergestellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b8d29-135">Specifies the target machine on which DB Files need to be restored.</span></span>

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

### <span data-ttu-id="b8d29-136">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="b8d29-136">-TargetItem</span></span>
<span data-ttu-id="b8d29-137">Gibt das Ziel an, auf dem die DB wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8d29-137">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="b8d29-138">Bei SQL-Wiederherstellungen muss es sich um einen geschützten Elementtyp SQLInstance handeln.</span><span class="sxs-lookup"><span data-stu-id="b8d29-138">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

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

### <span data-ttu-id="b8d29-139">-Tresor</span><span class="sxs-lookup"><span data-stu-id="b8d29-139">-VaultId</span></span>
<span data-ttu-id="b8d29-140">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="b8d29-140">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="b8d29-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8d29-141">CommonParameters</span></span>
<span data-ttu-id="b8d29-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8d29-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8d29-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8d29-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8d29-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b8d29-144">INPUTS</span></span>

### <span data-ttu-id="b8d29-145">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="b8d29-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="b8d29-146">System. String</span><span class="sxs-lookup"><span data-stu-id="b8d29-146">System.String</span></span>

## <span data-ttu-id="b8d29-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b8d29-147">OUTPUTS</span></span>

### <span data-ttu-id="b8d29-148">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="b8d29-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="b8d29-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="b8d29-149">NOTES</span></span>

## <span data-ttu-id="b8d29-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b8d29-150">RELATED LINKS</span></span>
