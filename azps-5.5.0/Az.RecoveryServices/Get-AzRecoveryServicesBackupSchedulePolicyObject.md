---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: d66b8515c6b2c3782c6f6c2b49d462dbb7bd1660
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160188"
---
# <span data-ttu-id="13200-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="13200-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="13200-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13200-102">SYNOPSIS</span></span>
<span data-ttu-id="13200-103">Ruft ein Basisplanrichtlinienobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="13200-103">Gets a base schedule policy object.</span></span>

## <span data-ttu-id="13200-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13200-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13200-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="13200-105">DESCRIPTION</span></span>
<span data-ttu-id="13200-106">Das **Cmdlet "Get-AzRecoveryServicesBackupSchedulePolicyObject"** ruft eine Basisversion von **AzureRMRecoveryServicesSchedulePolicyObject ab.**</span><span class="sxs-lookup"><span data-stu-id="13200-106">The **Get-AzRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="13200-107">Dieses Objekt wird nicht im System beibehalten.</span><span class="sxs-lookup"><span data-stu-id="13200-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="13200-108">Es ist ein temporäres Objekt, das Sie bearbeiten und mit dem New-AzRecoveryServicesBackupProtectionPolicy verwenden können, um eine neue Sicherungsschutzrichtlinie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="13200-108">It is temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="13200-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="13200-109">EXAMPLES</span></span>

### <span data-ttu-id="13200-110">Beispiel 1: Festlegen der Terminplanhäufigkeit auf "Wöchentlich"</span><span class="sxs-lookup"><span data-stu-id="13200-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="13200-111">Der erste Befehl ruft das Aufbewahrungsrichtlinienobjekt ab und speichert es dann in der $RetPol Variable.</span><span class="sxs-lookup"><span data-stu-id="13200-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="13200-112">Der zweite Befehl ruft das Zeitplanrichtlinienobjekt ab und speichert es dann in der $SchPol Variable.</span><span class="sxs-lookup"><span data-stu-id="13200-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="13200-113">Mit dem dritten Befehl wird die Häufigkeit für die Zeitplanrichtlinie in "Wöchentlich" geändert.</span><span class="sxs-lookup"><span data-stu-id="13200-113">The third command changes the frequency for the schedule policy to weekly.</span></span>
<span data-ttu-id="13200-114">Der letzte Befehl erstellt eine Sicherungsschutzrichtlinie mit dem aktualisierten Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="13200-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="13200-115">Beispiel 2: Festlegen der Sicherungszeit</span><span class="sxs-lookup"><span data-stu-id="13200-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="13200-116">Der erste Befehl ruft das Zeitplanrichtlinienobjekt ab und speichert es dann in der $SchPol Variable.</span><span class="sxs-lookup"><span data-stu-id="13200-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="13200-117">Der zweite Befehl entfernt alle geplanten Laufzeiten aus $SchPol.</span><span class="sxs-lookup"><span data-stu-id="13200-117">The second command removes all scheduled run times from $SchPol.</span></span>
<span data-ttu-id="13200-118">Der dritte Befehl ruft das aktuelle Datum und die aktuelle Uhrzeit ab und speichert ihn dann in der $DT Variable.</span><span class="sxs-lookup"><span data-stu-id="13200-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="13200-119">Der vierte Befehl ersetzt die geplanten Laufzeiten durch die aktuelle Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="13200-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="13200-120">Da Sie AzureVM nur einmal pro Tag sichern können, müssen Sie den ursprünglichen Zeitplan ersetzen, um die Sicherungszeit zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="13200-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>
<span data-ttu-id="13200-121">Der letzte Befehl erstellt eine Sicherungsschutzrichtlinie mit dem neuen Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="13200-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="13200-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13200-122">PARAMETERS</span></span>

### <span data-ttu-id="13200-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="13200-123">-BackupManagementType</span></span>
<span data-ttu-id="13200-124">Die Klasse der geschützten Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="13200-124">The class of resources being protected.</span></span> <span data-ttu-id="13200-125">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="13200-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="13200-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="13200-126">AzureVM</span></span> 
- <span data-ttu-id="13200-127">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="13200-127">AzureStorage</span></span>
- <span data-ttu-id="13200-128">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="13200-128">AzureWorkload</span></span>

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

### <span data-ttu-id="13200-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13200-129">-DefaultProfile</span></span>
<span data-ttu-id="13200-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="13200-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13200-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="13200-131">-WorkloadType</span></span>
<span data-ttu-id="13200-132">Arbeitsauslastungstyp der Ressource.</span><span class="sxs-lookup"><span data-stu-id="13200-132">Workload type of the resource.</span></span> <span data-ttu-id="13200-133">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="13200-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="13200-134">AzureVM</span><span class="sxs-lookup"><span data-stu-id="13200-134">AzureVM</span></span> 
- <span data-ttu-id="13200-135">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="13200-135">AzureFiles</span></span>
- <span data-ttu-id="13200-136">MSSQL</span><span class="sxs-lookup"><span data-stu-id="13200-136">MSSQL</span></span>


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

### <span data-ttu-id="13200-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13200-137">CommonParameters</span></span>
<span data-ttu-id="13200-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13200-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13200-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13200-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13200-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="13200-140">INPUTS</span></span>

### <span data-ttu-id="13200-141">Keine</span><span class="sxs-lookup"><span data-stu-id="13200-141">None</span></span>

## <span data-ttu-id="13200-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="13200-142">OUTPUTS</span></span>

### <span data-ttu-id="13200-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="13200-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="13200-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="13200-144">NOTES</span></span>

## <span data-ttu-id="13200-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="13200-145">RELATED LINKS</span></span>

[<span data-ttu-id="13200-146">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="13200-146">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="13200-147">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="13200-147">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


