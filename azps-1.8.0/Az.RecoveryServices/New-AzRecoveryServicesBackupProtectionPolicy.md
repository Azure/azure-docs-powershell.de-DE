---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 6aaf7fcd32ae7d50f273d69835f9131032b68c21
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659856"
---
# <span data-ttu-id="caf2a-101">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="caf2a-101">New-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="caf2a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="caf2a-102">SYNOPSIS</span></span>
<span data-ttu-id="caf2a-103">Erstellt eine Sicherungsschutz Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="caf2a-103">Creates a Backup protection policy.</span></span>

## <span data-ttu-id="caf2a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="caf2a-104">SYNTAX</span></span>

```
New-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="caf2a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="caf2a-105">DESCRIPTION</span></span>
<span data-ttu-id="caf2a-106">Das Cmdlet **New-AzRecoveryServicesBackupProtectionPolicy** erstellt eine Sicherungsschutz Richtlinie in einem Tresor.</span><span class="sxs-lookup"><span data-stu-id="caf2a-106">The **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="caf2a-107">Eine Schutzrichtlinie ist mit mindestens einer Aufbewahrungsrichtlinie verbunden.</span><span class="sxs-lookup"><span data-stu-id="caf2a-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="caf2a-108">Die Aufbewahrungsrichtlinie definiert, wie lange ein Wiederherstellungspunkt mit Azure-Sicherung beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="caf2a-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>
<span data-ttu-id="caf2a-109">Sie können das Get-AzRecoveryServicesBackupRetentionPolicyObject-Cmdlet verwenden, um die Standardaufbewahrungsrichtlinie abzurufen.</span><span class="sxs-lookup"><span data-stu-id="caf2a-109">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="caf2a-110">Und Sie können das Get-AzRecoveryServicesBackupSchedulePolicyObject-Cmdlet verwenden, um die standardmäßige Terminplan Richtlinie abzurufen.</span><span class="sxs-lookup"><span data-stu-id="caf2a-110">And you can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="caf2a-111">Die Objekte **SchedulePolicy** und **RetentionPolicy** werden als Eingaben für das Cmdlet **New-AzRecoveryServicesBackupProtectionPolicy** verwendet.</span><span class="sxs-lookup"><span data-stu-id="caf2a-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="caf2a-112">Setzen Sie den Vault-Kontext mithilfe des Set-AzRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="caf2a-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="caf2a-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="caf2a-113">EXAMPLES</span></span>

### <span data-ttu-id="caf2a-114">Beispiel 1: Erstellen einer Sicherungsschutz Richtlinie</span><span class="sxs-lookup"><span data-stu-id="caf2a-114">Example 1: Create a Backup protection policy</span></span>
```
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="caf2a-115">Der erste Befehl ruft einen Basis- **SchedulePolicyObject** ab und speichert ihn dann in der $SchPol-Variablen.</span><span class="sxs-lookup"><span data-stu-id="caf2a-115">The first command gets a base **SchedulePolicyObject** , and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="caf2a-116">Der zweite Befehl entfernt alle geplanten Ausführungszeiten aus der Terminplan Richtlinie in $SchPol.</span><span class="sxs-lookup"><span data-stu-id="caf2a-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="caf2a-117">Der dritte Befehl verwendet das Get-Date-Cmdlet, um das aktuelle Datum und die aktuelle Uhrzeit abzurufen.</span><span class="sxs-lookup"><span data-stu-id="caf2a-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>
<span data-ttu-id="caf2a-118">Der vierte Befehl addiert das aktuelle Datum und die aktuelle Uhrzeit in $dt als geplante Laufzeit zur Zeit Plan Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="caf2a-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>
<span data-ttu-id="caf2a-119">Der fünfte Befehl ruft ein Basis **RetentionPolicy** -Objekt ab und speichert es dann in der $RetPol-Variablen.</span><span class="sxs-lookup"><span data-stu-id="caf2a-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="caf2a-120">Der sechste Befehl legt die Richtlinie für die Aufbewahrungsdauer auf 365 Tage fest.</span><span class="sxs-lookup"><span data-stu-id="caf2a-120">The sixth command sets the retention duration policy to 365 days.</span></span>
<span data-ttu-id="caf2a-121">Der endgültige Befehl erstellt ein **BackupProtectionPolicy** -Objekt basierend auf den von den vorherigen Befehlen erstellten Plan-und Aufbewahrungsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="caf2a-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

## <span data-ttu-id="caf2a-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="caf2a-122">PARAMETERS</span></span>

### <span data-ttu-id="caf2a-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="caf2a-123">-BackupManagementType</span></span>
<span data-ttu-id="caf2a-124">Gibt den Sicherungs Verwaltungstyp an.</span><span class="sxs-lookup"><span data-stu-id="caf2a-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="caf2a-125">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="caf2a-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="caf2a-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="caf2a-126">AzureVM</span></span> 
- <span data-ttu-id="caf2a-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="caf2a-127">AzureSQLDatabase</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caf2a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caf2a-128">-DefaultProfile</span></span>
<span data-ttu-id="caf2a-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="caf2a-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="caf2a-130">-Name</span><span class="sxs-lookup"><span data-stu-id="caf2a-130">-Name</span></span>
<span data-ttu-id="caf2a-131">Gibt den Namen der Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="caf2a-131">Specifies the name of the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caf2a-132">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="caf2a-132">-RetentionPolicy</span></span>
<span data-ttu-id="caf2a-133">Gibt das Basis **RetentionPolicy** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="caf2a-133">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="caf2a-134">Sie können das Get-AzRecoveryServicesBackupRetentionPolicyObject-Cmdlet verwenden, um ein **RetentionPolicy** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="caf2a-134">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caf2a-135">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="caf2a-135">-SchedulePolicy</span></span>
<span data-ttu-id="caf2a-136">Gibt das Basis **SchedulePolicy** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="caf2a-136">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="caf2a-137">Sie können das Get-AzRecoveryServicesBackupSchedulePolicyObject-Cmdlet verwenden, um ein **SchedulePolicy** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="caf2a-137">You can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caf2a-138">-Tresor</span><span class="sxs-lookup"><span data-stu-id="caf2a-138">-VaultId</span></span>
<span data-ttu-id="caf2a-139">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="caf2a-139">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="caf2a-140">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="caf2a-140">-WorkloadType</span></span>
<span data-ttu-id="caf2a-141">Gibt den Arbeits Auslastungs an.</span><span class="sxs-lookup"><span data-stu-id="caf2a-141">Specifies the workload type.</span></span>
<span data-ttu-id="caf2a-142">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="caf2a-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="caf2a-143">AzureVM</span><span class="sxs-lookup"><span data-stu-id="caf2a-143">AzureVM</span></span> 
- <span data-ttu-id="caf2a-144">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="caf2a-144">AzureSQLDatabase</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caf2a-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="caf2a-145">-Confirm</span></span>
<span data-ttu-id="caf2a-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="caf2a-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="caf2a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caf2a-147">-WhatIf</span></span>
<span data-ttu-id="caf2a-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="caf2a-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="caf2a-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="caf2a-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="caf2a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caf2a-150">CommonParameters</span></span>
<span data-ttu-id="caf2a-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="caf2a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caf2a-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caf2a-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caf2a-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="caf2a-153">INPUTS</span></span>

### <span data-ttu-id="caf2a-154">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. workloadtype</span><span class="sxs-lookup"><span data-stu-id="caf2a-154">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType</span></span>

### <span data-ttu-id="caf2a-155">System. Nullable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. BackupManagementType, Microsoft. Azure. PowerShell. Cmdlets. RecoveryServices. Backup. Models, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="caf2a-155">System.Nullable\`1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.Models, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="caf2a-156">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="caf2a-156">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

### <span data-ttu-id="caf2a-157">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="caf2a-157">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

### <span data-ttu-id="caf2a-158">System. String</span><span class="sxs-lookup"><span data-stu-id="caf2a-158">System.String</span></span>

## <span data-ttu-id="caf2a-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="caf2a-159">OUTPUTS</span></span>

### <span data-ttu-id="caf2a-160">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="caf2a-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="caf2a-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="caf2a-161">NOTES</span></span>

## <span data-ttu-id="caf2a-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="caf2a-162">RELATED LINKS</span></span>

[<span data-ttu-id="caf2a-163">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="caf2a-163">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="caf2a-164">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="caf2a-164">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="caf2a-165">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="caf2a-165">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="caf2a-166">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="caf2a-166">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="caf2a-167">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="caf2a-167">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="caf2a-168">Satz-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="caf2a-168">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


