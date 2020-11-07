---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: 71650d36c319536db5ad96aa142e2712e229d712
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824316"
---
# <span data-ttu-id="b70ff-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="b70ff-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="b70ff-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b70ff-102">SYNOPSIS</span></span>
<span data-ttu-id="b70ff-103">Ruft ein Basis Zeitplan-Richtlinienobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="b70ff-103">Gets a base schedule policy object.</span></span>

## <span data-ttu-id="b70ff-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b70ff-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b70ff-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b70ff-105">DESCRIPTION</span></span>
<span data-ttu-id="b70ff-106">Das Cmdlet " **Get-AzRecoveryServicesBackupSchedulePolicyObject** " Ruft eine Basis- **AzureRMRecoveryServicesSchedulePolicyObject** ab.</span><span class="sxs-lookup"><span data-stu-id="b70ff-106">The **Get-AzRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="b70ff-107">Dieses Objekt wird im System nicht beibehalten.</span><span class="sxs-lookup"><span data-stu-id="b70ff-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="b70ff-108">Es handelt sich um ein temporäres Objekt, das Sie mit dem New-AzRecoveryServicesBackupProtectionPolicy-Cmdlet bearbeiten und verwenden können, um eine neue Sicherungsschutz Richtlinie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b70ff-108">It is temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="b70ff-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b70ff-109">EXAMPLES</span></span>

### <span data-ttu-id="b70ff-110">Beispiel 1: Festlegen der Häufigkeit "Zeitplan" auf "wöchentlich"</span><span class="sxs-lookup"><span data-stu-id="b70ff-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="b70ff-111">Der erste Befehl ruft das Aufbewahrungsrichtlinienobjekt ab und speichert es dann in der $RetPol Variablen.</span><span class="sxs-lookup"><span data-stu-id="b70ff-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="b70ff-112">Der zweite Befehl ruft das Schedule-Richtlinienobjekt ab und speichert es dann in der $SchPol-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b70ff-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="b70ff-113">Der dritte Befehl ändert die Häufigkeit der Zeit Plan Richtlinie in Weekly.</span><span class="sxs-lookup"><span data-stu-id="b70ff-113">The third command changes the frequency for the schedule policy to weekly.</span></span>
<span data-ttu-id="b70ff-114">Der letzte Befehl erstellt eine Sicherungsschutz Richtlinie mit dem aktualisierten Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="b70ff-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="b70ff-115">Beispiel 2: Einrichten der Sicherungszeit</span><span class="sxs-lookup"><span data-stu-id="b70ff-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="b70ff-116">Der erste Befehl ruft das Schedule-Richtlinienobjekt ab und speichert es dann in der $SchPol-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b70ff-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="b70ff-117">Der zweite Befehl entfernt alle geplanten Ausführungszeiten von $SchPol.</span><span class="sxs-lookup"><span data-stu-id="b70ff-117">The second command removes all scheduled run times from $SchPol.</span></span>
<span data-ttu-id="b70ff-118">Der dritte Befehl ruft das aktuelle Datum und die aktuelle Uhrzeit ab und speichert es dann in der $dt Variablen.</span><span class="sxs-lookup"><span data-stu-id="b70ff-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="b70ff-119">Der vierte Befehl ersetzt die geplanten Ausführungszeiten durch die aktuelle Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="b70ff-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="b70ff-120">Sie können AzureVM nur einmal pro Tag sichern, sodass Sie den ursprünglichen Zeitplan ersetzen müssen, um die Sicherungszeit zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="b70ff-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>
<span data-ttu-id="b70ff-121">Mit dem letzten Befehl wird eine Sicherungsschutz Richtlinie mit dem neuen Zeitplan erstellt.</span><span class="sxs-lookup"><span data-stu-id="b70ff-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="b70ff-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="b70ff-122">PARAMETERS</span></span>

### <span data-ttu-id="b70ff-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="b70ff-123">-BackupManagementType</span></span>
<span data-ttu-id="b70ff-124">Gibt den Sicherungs Verwaltungstyp an.</span><span class="sxs-lookup"><span data-stu-id="b70ff-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="b70ff-125">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b70ff-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b70ff-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="b70ff-126">AzureVM</span></span> 
- <span data-ttu-id="b70ff-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="b70ff-127">AzureSQLDatabase</span></span>
- <span data-ttu-id="b70ff-128">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="b70ff-128">AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b70ff-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b70ff-129">-DefaultProfile</span></span>
<span data-ttu-id="b70ff-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b70ff-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b70ff-131">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="b70ff-131">-WorkloadType</span></span>
<span data-ttu-id="b70ff-132">Gibt den Arbeits Auslastungs an.</span><span class="sxs-lookup"><span data-stu-id="b70ff-132">Specifies the workload type.</span></span>
<span data-ttu-id="b70ff-133">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b70ff-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b70ff-134">AzureVM</span><span class="sxs-lookup"><span data-stu-id="b70ff-134">AzureVM</span></span> 
- <span data-ttu-id="b70ff-135">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="b70ff-135">AzureSQLDatabase</span></span>
- <span data-ttu-id="b70ff-136">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="b70ff-136">AzureFiles</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b70ff-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b70ff-137">CommonParameters</span></span>
<span data-ttu-id="b70ff-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b70ff-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b70ff-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b70ff-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b70ff-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b70ff-140">INPUTS</span></span>

### <span data-ttu-id="b70ff-141">Keine</span><span class="sxs-lookup"><span data-stu-id="b70ff-141">None</span></span>

## <span data-ttu-id="b70ff-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b70ff-142">OUTPUTS</span></span>

### <span data-ttu-id="b70ff-143">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="b70ff-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="b70ff-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="b70ff-144">NOTES</span></span>

## <span data-ttu-id="b70ff-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b70ff-145">RELATED LINKS</span></span>

[<span data-ttu-id="b70ff-146">Neu – AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b70ff-146">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="b70ff-147">Satz-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b70ff-147">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


