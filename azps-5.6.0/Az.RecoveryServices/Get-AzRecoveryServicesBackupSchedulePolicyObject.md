---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: 5bf91aafffb1c6fd650b5fd88f343897afc6c5d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932331"
---
# <span data-ttu-id="34144-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="34144-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="34144-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34144-102">SYNOPSIS</span></span>
<span data-ttu-id="34144-103">Ruft ein Basiszeitplanrichtlinienobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="34144-103">Gets a base schedule policy object.</span></span>

## <span data-ttu-id="34144-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34144-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="34144-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34144-105">DESCRIPTION</span></span>
<span data-ttu-id="34144-106">Das **Get-AzRecoveryServicesBackupSchedulePolicyObject-Cmdlet** ruft ein **AzureRMRecoveryServicesSchedulePolicyObject ab.**</span><span class="sxs-lookup"><span data-stu-id="34144-106">The **Get-AzRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="34144-107">Dieses Objekt wird im System nicht beibehalten.</span><span class="sxs-lookup"><span data-stu-id="34144-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="34144-108">Es ist ein temporäres Objekt, das Sie bearbeiten und mit dem New-AzRecoveryServicesBackupProtectionPolicy verwenden können, um eine neue Sicherungsschutzrichtlinie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="34144-108">It is temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="34144-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="34144-109">EXAMPLES</span></span>

### <span data-ttu-id="34144-110">Beispiel 1: Festlegen der Zeitplanhäufigkeit auf wöchentlich</span><span class="sxs-lookup"><span data-stu-id="34144-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="34144-111">Der erste Befehl ruft das Aufbewahrungsrichtlinienobjekt ab und speichert es dann in der $RetPol-Variable.</span><span class="sxs-lookup"><span data-stu-id="34144-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="34144-112">Der zweite Befehl ruft das Richtlinienobjekt des Zeitplans ab und speichert es dann in der $SchPol Variablen.</span><span class="sxs-lookup"><span data-stu-id="34144-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="34144-113">Mit dem dritten Befehl wird die Häufigkeit für die Zeitplanrichtlinie in wöchentlich geändert.</span><span class="sxs-lookup"><span data-stu-id="34144-113">The third command changes the frequency for the schedule policy to weekly.</span></span>
<span data-ttu-id="34144-114">Mit dem letzten Befehl wird eine Sicherungsschutzrichtlinie mit dem aktualisierten Zeitplan erstellt.</span><span class="sxs-lookup"><span data-stu-id="34144-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="34144-115">Beispiel 2: Festlegen der Sicherungszeit</span><span class="sxs-lookup"><span data-stu-id="34144-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="34144-116">Der erste Befehl ruft das Richtlinienobjekt des Zeitplans ab und speichert es dann in der $SchPol Variablen.</span><span class="sxs-lookup"><span data-stu-id="34144-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="34144-117">Mit dem zweiten Befehl werden alle geplanten Laufzeiten aus $SchPol.</span><span class="sxs-lookup"><span data-stu-id="34144-117">The second command removes all scheduled run times from $SchPol.</span></span>
<span data-ttu-id="34144-118">Der dritte Befehl ruft das aktuelle Datum und die aktuelle Uhrzeit ab und speichert ihn dann in der $DT Variablen.</span><span class="sxs-lookup"><span data-stu-id="34144-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="34144-119">Der vierte Befehl ersetzt die geplanten Laufzeiten durch die aktuelle Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="34144-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="34144-120">Sie können AzureVM nur einmal pro Tag sichern. Um also die Sicherungszeit zurückzusetzen, müssen Sie den ursprünglichen Zeitplan ersetzen.</span><span class="sxs-lookup"><span data-stu-id="34144-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>
<span data-ttu-id="34144-121">Mit dem letzten Befehl wird mithilfe des neuen Zeitplans eine Sicherungsschutzrichtlinie erstellt.</span><span class="sxs-lookup"><span data-stu-id="34144-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="34144-122">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="34144-122">PARAMETERS</span></span>

### <span data-ttu-id="34144-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="34144-123">-BackupManagementType</span></span>
<span data-ttu-id="34144-124">Die Klasse der zu schützenden Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="34144-124">The class of resources being protected.</span></span> <span data-ttu-id="34144-125">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="34144-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="34144-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="34144-126">AzureVM</span></span> 
- <span data-ttu-id="34144-127">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="34144-127">AzureStorage</span></span>
- <span data-ttu-id="34144-128">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="34144-128">AzureWorkload</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34144-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34144-129">-DefaultProfile</span></span>
<span data-ttu-id="34144-130">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="34144-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34144-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="34144-131">-WorkloadType</span></span>
<span data-ttu-id="34144-132">Arbeitsauslastungstyp der Ressource.</span><span class="sxs-lookup"><span data-stu-id="34144-132">Workload type of the resource.</span></span> <span data-ttu-id="34144-133">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="34144-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="34144-134">AzureVM</span><span class="sxs-lookup"><span data-stu-id="34144-134">AzureVM</span></span> 
- <span data-ttu-id="34144-135">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="34144-135">AzureFiles</span></span>
- <span data-ttu-id="34144-136">MSSQL</span><span class="sxs-lookup"><span data-stu-id="34144-136">MSSQL</span></span>


```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34144-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34144-137">CommonParameters</span></span>
<span data-ttu-id="34144-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34144-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34144-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34144-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34144-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="34144-140">INPUTS</span></span>

### <span data-ttu-id="34144-141">Keine</span><span class="sxs-lookup"><span data-stu-id="34144-141">None</span></span>

## <span data-ttu-id="34144-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="34144-142">OUTPUTS</span></span>

### <span data-ttu-id="34144-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="34144-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="34144-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="34144-144">NOTES</span></span>

## <span data-ttu-id="34144-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="34144-145">RELATED LINKS</span></span>

[<span data-ttu-id="34144-146">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="34144-146">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="34144-147">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="34144-147">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


