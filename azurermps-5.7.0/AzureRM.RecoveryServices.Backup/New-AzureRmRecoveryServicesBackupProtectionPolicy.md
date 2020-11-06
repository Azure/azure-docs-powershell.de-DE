---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/new-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: e9834236a72a68f64cc9b19d6576e56102f96b13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478333"
---
# <span data-ttu-id="e037b-101">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e037b-101">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="e037b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e037b-102">SYNOPSIS</span></span>
<span data-ttu-id="e037b-103">Erstellt eine Sicherungsschutz Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="e037b-103">Creates a Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e037b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e037b-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e037b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e037b-105">DESCRIPTION</span></span>
<span data-ttu-id="e037b-106">Das Cmdlet **New-AzureRmRecoveryServicesBackupProtectionPolicy** erstellt eine Sicherungsschutz Richtlinie in einem Tresor.</span><span class="sxs-lookup"><span data-stu-id="e037b-106">The **New-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="e037b-107">Eine Schutzrichtlinie ist mit mindestens einer Aufbewahrungsrichtlinie verbunden.</span><span class="sxs-lookup"><span data-stu-id="e037b-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="e037b-108">Die Aufbewahrungsrichtlinie definiert, wie lange ein Wiederherstellungspunkt mit Azure-Sicherung beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="e037b-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>

<span data-ttu-id="e037b-109">Sie können das Get-AzureRmRecoveryServicesBackupRetentionPolicyObject-Cmdlet verwenden, um die Standardaufbewahrungsrichtlinie abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e037b-109">You can use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="e037b-110">Und Sie können das Get-AzureRmRecoveryServicesBackupSchedulePolicyObject-Cmdlet verwenden, um die standardmäßige Terminplan Richtlinie abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e037b-110">And you can use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="e037b-111">Die Objekte **SchedulePolicy** und **RetentionPolicy** werden als Eingaben für das Cmdlet **New-AzureRmRecoveryServicesBackupProtectionPolicy** verwendet.</span><span class="sxs-lookup"><span data-stu-id="e037b-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>

<span data-ttu-id="e037b-112">Setzen Sie den Vault-Kontext mithilfe des Set-AzureRmRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="e037b-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="e037b-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e037b-113">EXAMPLES</span></span>

### <span data-ttu-id="e037b-114">Beispiel 1: Erstellen einer Sicherungsschutz Richtlinie</span><span class="sxs-lookup"><span data-stu-id="e037b-114">Example 1: Create a Backup protection policy</span></span>
```
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="e037b-115">Der erste Befehl ruft einen Basis- **SchedulePolicyObject** ab und speichert ihn dann in der $SchPol-Variablen.</span><span class="sxs-lookup"><span data-stu-id="e037b-115">The first command gets a base **SchedulePolicyObject** , and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="e037b-116">Der zweite Befehl entfernt alle geplanten Ausführungszeiten aus der Terminplan Richtlinie in $SchPol.</span><span class="sxs-lookup"><span data-stu-id="e037b-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>

<span data-ttu-id="e037b-117">Der dritte Befehl verwendet das Get-Date-Cmdlet, um das aktuelle Datum und die aktuelle Uhrzeit abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e037b-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>

<span data-ttu-id="e037b-118">Der vierte Befehl addiert das aktuelle Datum und die aktuelle Uhrzeit in $dt als geplante Laufzeit zur Zeit Plan Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="e037b-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>

<span data-ttu-id="e037b-119">Der fünfte Befehl ruft ein Basis **RetentionPolicy** -Objekt ab und speichert es dann in der $RetPol-Variablen.</span><span class="sxs-lookup"><span data-stu-id="e037b-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="e037b-120">Der sechste Befehl legt die Richtlinie für die Aufbewahrungsdauer auf 365 Tage fest.</span><span class="sxs-lookup"><span data-stu-id="e037b-120">The sixth command sets the retention duration policy to 365 days.</span></span>

<span data-ttu-id="e037b-121">Der endgültige Befehl erstellt ein **BackupProtectionPolicy** -Objekt basierend auf den von den vorherigen Befehlen erstellten Plan-und Aufbewahrungsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="e037b-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

## <span data-ttu-id="e037b-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="e037b-122">PARAMETERS</span></span>

### <span data-ttu-id="e037b-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="e037b-123">-BackupManagementType</span></span>
<span data-ttu-id="e037b-124">Gibt den Sicherungs Verwaltungstyp an.</span><span class="sxs-lookup"><span data-stu-id="e037b-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="e037b-125">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e037b-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e037b-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="e037b-126">AzureVM</span></span> 
- <span data-ttu-id="e037b-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="e037b-127">AzureSQLDatabase</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e037b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e037b-128">-DefaultProfile</span></span>
<span data-ttu-id="e037b-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e037b-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e037b-130">-Name</span><span class="sxs-lookup"><span data-stu-id="e037b-130">-Name</span></span>
<span data-ttu-id="e037b-131">Gibt den Namen der Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="e037b-131">Specifies the name of the policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e037b-132">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e037b-132">-RetentionPolicy</span></span>
<span data-ttu-id="e037b-133">Gibt das Basis **RetentionPolicy** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="e037b-133">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="e037b-134">Sie können das Get-AzureRmRecoveryServicesBackupRetentionPolicyObject-Cmdlet verwenden, um ein **RetentionPolicy** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e037b-134">You can use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

```yaml
Type: RetentionPolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e037b-135">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="e037b-135">-SchedulePolicy</span></span>
<span data-ttu-id="e037b-136">Gibt das Basis **SchedulePolicy** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="e037b-136">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="e037b-137">Sie können das Get-AzureRmRecoveryServicesBackupSchedulePolicyObject-Cmdlet verwenden, um ein **SchedulePolicy** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e037b-137">You can use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

```yaml
Type: SchedulePolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e037b-138">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="e037b-138">-WorkloadType</span></span>
<span data-ttu-id="e037b-139">Gibt den Arbeits Auslastungs an.</span><span class="sxs-lookup"><span data-stu-id="e037b-139">Specifies the workload type.</span></span>
<span data-ttu-id="e037b-140">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e037b-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e037b-141">AzureVM</span><span class="sxs-lookup"><span data-stu-id="e037b-141">AzureVM</span></span> 
- <span data-ttu-id="e037b-142">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="e037b-142">AzureSQLDatabase</span></span>

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e037b-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e037b-143">-Confirm</span></span>
<span data-ttu-id="e037b-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e037b-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e037b-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e037b-145">-WhatIf</span></span>
<span data-ttu-id="e037b-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e037b-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e037b-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e037b-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e037b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e037b-148">CommonParameters</span></span>
<span data-ttu-id="e037b-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e037b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e037b-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e037b-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e037b-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e037b-151">INPUTS</span></span>

### <span data-ttu-id="e037b-152">Keine</span><span class="sxs-lookup"><span data-stu-id="e037b-152">None</span></span>
<span data-ttu-id="e037b-153">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="e037b-153">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e037b-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e037b-154">OUTPUTS</span></span>

### <span data-ttu-id="e037b-155">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="e037b-155">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="e037b-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="e037b-156">NOTES</span></span>

## <span data-ttu-id="e037b-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e037b-157">RELATED LINKS</span></span>

[<span data-ttu-id="e037b-158">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="e037b-158">Enable-AzureRmRecoveryServicesBackupProtection</span></span>](./Enable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="e037b-159">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e037b-159">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="e037b-160">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="e037b-160">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="e037b-161">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="e037b-161">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="e037b-162">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e037b-162">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="e037b-163">Satz-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e037b-163">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


