---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: 4a3602363436c396b0706d9c195569874a35fdf3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478342"
---
# <span data-ttu-id="a94a9-101">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="a94a9-101">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="a94a9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a94a9-102">SYNOPSIS</span></span>
<span data-ttu-id="a94a9-103">Ruft ein Basis Zeitplan-Richtlinienobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="a94a9-103">Gets a base schedule policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a94a9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a94a9-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a94a9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a94a9-105">DESCRIPTION</span></span>
<span data-ttu-id="a94a9-106">Das Cmdlet " **Get-AzureRmRecoveryServicesBackupSchedulePolicyObject** " Ruft eine Basis- **AzureRMRecoveryServicesSchedulePolicyObject** ab.</span><span class="sxs-lookup"><span data-stu-id="a94a9-106">The **Get-AzureRmRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="a94a9-107">Dieses Objekt wird im System nicht beibehalten.</span><span class="sxs-lookup"><span data-stu-id="a94a9-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="a94a9-108">Es handelt sich um ein temporäres Objekt, das Sie mit dem New-AzureRmRecoveryServicesBackupProtectionPolicy-Cmdlet bearbeiten und verwenden können, um eine neue Sicherungsschutz Richtlinie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a94a9-108">It is temporary object that you can manipulate and use with the New-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="a94a9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a94a9-109">EXAMPLES</span></span>

### <span data-ttu-id="a94a9-110">Beispiel 1: Festlegen der Häufigkeit "Zeitplan" auf "wöchentlich"</span><span class="sxs-lookup"><span data-stu-id="a94a9-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="a94a9-111">Der erste Befehl ruft das Aufbewahrungsrichtlinienobjekt ab und speichert es dann in der $RetPol Variablen.</span><span class="sxs-lookup"><span data-stu-id="a94a9-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="a94a9-112">Der zweite Befehl ruft das Schedule-Richtlinienobjekt ab und speichert es dann in der $SchPol-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a94a9-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="a94a9-113">Der dritte Befehl ändert die Häufigkeit der Zeit Plan Richtlinie in Weekly.</span><span class="sxs-lookup"><span data-stu-id="a94a9-113">The third command changes the frequency for the schedule policy to weekly.</span></span>

<span data-ttu-id="a94a9-114">Der letzte Befehl erstellt eine Sicherungsschutz Richtlinie mit dem aktualisierten Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="a94a9-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="a94a9-115">Beispiel 2: Einrichten der Sicherungszeit</span><span class="sxs-lookup"><span data-stu-id="a94a9-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="a94a9-116">Der erste Befehl ruft das Schedule-Richtlinienobjekt ab und speichert es dann in der $SchPol-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a94a9-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="a94a9-117">Der zweite Befehl entfernt alle geplanten Ausführungszeiten von $SchPol.</span><span class="sxs-lookup"><span data-stu-id="a94a9-117">The second command removes all scheduled run times from $SchPol.</span></span>

<span data-ttu-id="a94a9-118">Der dritte Befehl ruft das aktuelle Datum und die aktuelle Uhrzeit ab und speichert es dann in der $dt Variablen.</span><span class="sxs-lookup"><span data-stu-id="a94a9-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>

<span data-ttu-id="a94a9-119">Der vierte Befehl ersetzt die geplanten Ausführungszeiten durch die aktuelle Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="a94a9-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="a94a9-120">Sie können AzureVM nur einmal pro Tag sichern, sodass Sie den ursprünglichen Zeitplan ersetzen müssen, um die Sicherungszeit zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="a94a9-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>

<span data-ttu-id="a94a9-121">Mit dem letzten Befehl wird eine Sicherungsschutz Richtlinie mit dem neuen Zeitplan erstellt.</span><span class="sxs-lookup"><span data-stu-id="a94a9-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="a94a9-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="a94a9-122">PARAMETERS</span></span>

### <span data-ttu-id="a94a9-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="a94a9-123">-BackupManagementType</span></span>
<span data-ttu-id="a94a9-124">Gibt den Sicherungs Verwaltungstyp an.</span><span class="sxs-lookup"><span data-stu-id="a94a9-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="a94a9-125">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a94a9-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a94a9-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="a94a9-126">AzureVM</span></span> 
- <span data-ttu-id="a94a9-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="a94a9-127">AzureSQLDatabase</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a94a9-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a94a9-128">-DefaultProfile</span></span>
<span data-ttu-id="a94a9-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a94a9-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a94a9-130">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="a94a9-130">-WorkloadType</span></span>
<span data-ttu-id="a94a9-131">Gibt den Arbeits Auslastungs an.</span><span class="sxs-lookup"><span data-stu-id="a94a9-131">Specifies the workload type.</span></span>
<span data-ttu-id="a94a9-132">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a94a9-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a94a9-133">AzureVM</span><span class="sxs-lookup"><span data-stu-id="a94a9-133">AzureVM</span></span> 
- <span data-ttu-id="a94a9-134">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="a94a9-134">AzureSQLDatabase</span></span>

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a94a9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a94a9-135">CommonParameters</span></span>
<span data-ttu-id="a94a9-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a94a9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a94a9-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a94a9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a94a9-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a94a9-138">INPUTS</span></span>

### <span data-ttu-id="a94a9-139">Keine</span><span class="sxs-lookup"><span data-stu-id="a94a9-139">None</span></span>
<span data-ttu-id="a94a9-140">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="a94a9-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a94a9-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a94a9-141">OUTPUTS</span></span>

### <span data-ttu-id="a94a9-142">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="a94a9-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="a94a9-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="a94a9-143">NOTES</span></span>

## <span data-ttu-id="a94a9-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a94a9-144">RELATED LINKS</span></span>

[<span data-ttu-id="a94a9-145">Neu – AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a94a9-145">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="a94a9-146">Satz-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a94a9-146">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


