---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: A8FDC5A3-F309-49B3-B417-8E0A1535BAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/stop-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 41234c91d5c833f15a4914d2af2de93c9c5bf288
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169244"
---
# <span data-ttu-id="3cae5-101">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="3cae5-101">Stop-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="3cae5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cae5-102">SYNOPSIS</span></span>
<span data-ttu-id="3cae5-103">Bricht einen ausgeführten Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="3cae5-103">Cancels a running job.</span></span>

## <span data-ttu-id="3cae5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3cae5-104">SYNTAX</span></span>

### <span data-ttu-id="3cae5-105">JobFilterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3cae5-105">JobFilterSet (Default)</span></span>
```
Stop-AzRecoveryServicesBackupJob [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cae5-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="3cae5-106">IdFilterSet</span></span>
```
Stop-AzRecoveryServicesBackupJob [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cae5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3cae5-107">DESCRIPTION</span></span>
<span data-ttu-id="3cae5-108">Das **Cmdlet "Stop-AzRecoveryServicesBackupJob"** bricht einen vorhandenen Azure -Sicherungsauftrag ab.</span><span class="sxs-lookup"><span data-stu-id="3cae5-108">The **Stop-AzRecoveryServicesBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="3cae5-109">Verwenden Sie dieses Cmdlet, um einen Auftrag zu lange zu beenden und andere Aktivitäten zu sperren.</span><span class="sxs-lookup"><span data-stu-id="3cae5-109">Use this cmdlet to stop a job that takes too long and blocks other activities.</span></span>
<span data-ttu-id="3cae5-110">Sie können nur die Typen von Sicherungs- und Wiederherstellungsauftrag abbrechen.</span><span class="sxs-lookup"><span data-stu-id="3cae5-110">You can cancel only Backup and Restore job types.</span></span>
<span data-ttu-id="3cae5-111">Legen Sie den Tresorkontext mithilfe des cmdlets Set-AzRecoveryServicesVaultContext, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="3cae5-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="3cae5-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3cae5-112">EXAMPLES</span></span>

### <span data-ttu-id="3cae5-113">Beispiel 1: Beenden eines Sicherungsauftrags</span><span class="sxs-lookup"><span data-stu-id="3cae5-113">Example 1: Stop a backup job</span></span>
```
PS C:\>$Job = Get-AzRecoveryServicesBackupJob -Operation Backup
PS C:\> Stop-AzRecoveryServicesBackupJob -JobID $Job.InstanceId
```

<span data-ttu-id="3cae5-114">Der erste Befehl ruft einen Sicherungsauftrag ab und speichert den Auftrag dann in der $Job Variable.</span><span class="sxs-lookup"><span data-stu-id="3cae5-114">The first command gets a backup job, and then stores the job in the $Job variable.</span></span>
<span data-ttu-id="3cae5-115">Der letzte Befehl beendet den Auftrag, indem er die Instanz-ID des Sicherungsauftrags in $Job.</span><span class="sxs-lookup"><span data-stu-id="3cae5-115">The last command stops the job by specifying the Instance ID of the backup job in $Job.</span></span>

## <span data-ttu-id="3cae5-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3cae5-116">PARAMETERS</span></span>

### <span data-ttu-id="3cae5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cae5-117">-DefaultProfile</span></span>
<span data-ttu-id="3cae5-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3cae5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cae5-119">-Job</span><span class="sxs-lookup"><span data-stu-id="3cae5-119">-Job</span></span>
<span data-ttu-id="3cae5-120">Gibt einen Auftrag an, der von diesem Cmdlet abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="3cae5-120">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="3cae5-121">Verwenden Sie das cmdlet Get-AzRecoveryServicesBackupJob **BackupJob,** um ein "BackupJob"-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3cae5-121">To obtain a **BackupJob** object, use the Get-AzRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: JobFilterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cae5-122">-JobId</span><span class="sxs-lookup"><span data-stu-id="3cae5-122">-JobId</span></span>
<span data-ttu-id="3cae5-123">Gibt die ID des zu abbrechenden Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="3cae5-123">Specifies the ID of the job to cancel.</span></span>
<span data-ttu-id="3cae5-124">Die ID ist die "InstanceId"-Eigenschaft eines **BackupJob-Objekts.**</span><span class="sxs-lookup"><span data-stu-id="3cae5-124">The ID is the InstanceId property of a **BackupJob** object.</span></span>
<span data-ttu-id="3cae5-125">Verwenden Sie "Get-AzRecoveryServicesBackupJob", um ein **"BackupJob"-Objekt** zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3cae5-125">To obtain an **BackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

```yaml
Type: System.String
Parameter Sets: IdFilterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cae5-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="3cae5-126">-VaultId</span></span>
<span data-ttu-id="3cae5-127">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="3cae5-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="3cae5-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3cae5-128">-Confirm</span></span>
<span data-ttu-id="3cae5-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3cae5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cae5-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3cae5-130">-WhatIf</span></span>
<span data-ttu-id="3cae5-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3cae5-131">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="3cae5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cae5-132">CommonParameters</span></span>
<span data-ttu-id="3cae5-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cae5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cae5-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3cae5-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cae5-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3cae5-135">INPUTS</span></span>

### <span data-ttu-id="3cae5-136">System.String</span><span class="sxs-lookup"><span data-stu-id="3cae5-136">System.String</span></span>

## <span data-ttu-id="3cae5-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3cae5-137">OUTPUTS</span></span>

### <span data-ttu-id="3cae5-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="3cae5-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="3cae5-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3cae5-139">NOTES</span></span>

## <span data-ttu-id="3cae5-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3cae5-140">RELATED LINKS</span></span>

[<span data-ttu-id="3cae5-141">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="3cae5-141">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="3cae5-142">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="3cae5-142">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)


