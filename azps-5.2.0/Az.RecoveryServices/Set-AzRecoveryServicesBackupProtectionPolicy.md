---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: e9f89a39b283f073c0fe826f22157570be29e74b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357397"
---
# <span data-ttu-id="0bf57-101">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0bf57-101">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="0bf57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bf57-102">SYNOPSIS</span></span>
<span data-ttu-id="0bf57-103">Ändert eine Sicherungsschutzrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="0bf57-103">Modifies a Backup protection policy.</span></span>

## <span data-ttu-id="0bf57-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0bf57-104">SYNTAX</span></span>

### <span data-ttu-id="0bf57-105">ModifyPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="0bf57-105">ModifyPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bf57-106">FixPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="0bf57-106">FixPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-FixForInconsistentItems]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bf57-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0bf57-107">DESCRIPTION</span></span>
<span data-ttu-id="0bf57-108">Das **Cmdlet Set-AzRecoveryServicesBackupProtectionPolicy** ändert eine vorhandene Azure Backup-Schutzrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="0bf57-108">The **Set-AzRecoveryServicesBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="0bf57-109">Sie können die Komponenten für den Sicherungszeitplan und die Aufbewahrungsrichtlinie ändern.</span><span class="sxs-lookup"><span data-stu-id="0bf57-109">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="0bf57-110">Alle Änderungen, die Sie vornehmen, wirken sich auf die Sicherung und Aufbewahrung der Elemente aus, die mit der Richtlinie verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="0bf57-110">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="0bf57-111">Legen Sie den Tresorkontext mithilfe des cmdlets Set-AzRecoveryServicesVaultContext, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="0bf57-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="0bf57-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0bf57-112">EXAMPLES</span></span>

### <span data-ttu-id="0bf57-113">Beispiel 1: Ändern einer Sicherungsschutzrichtlinie</span><span class="sxs-lookup"><span data-stu-id="0bf57-113">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Time = Get-Date
PS C:\> $Time1 = Get-Date -Year $Time.Year -Month $Time.Month -Day $Time.Day -Hour $Time.Hour -Minute 0 -Second 0 -Millisecond 0
PS C:\> $Time1 = $Time1.ToUniversalTime()
PS C:\> $SchPol.ScheduleRunTimes.Add($Time1)
PS C:\> $SchPol.ScheduleRunFrequency.Clear
PS C:\> $SchPol.ScheduleRunDays.Add("Monday")
PS C:\> $SchPol.ScheduleRunFrequency="Weekly"
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.IsDailyScheduleEnabled=$false
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 0
PS C:\> $RetPol.IsWeeklyScheduleEnabled=$true 
PS C:\> $RetPol.WeeklySchedule.DaysOfTheWeek.Add("Monday")
PS C:\> $RetPol.WeeklySchedule.DurationCountInWeeks = 365
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "azurefiles" -Name "azurefilesvault"
PS C:\> $Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "TestPolicy" -VaultId $vault.ID
PS C:\> $Pol.SnapshotRetentionInDays=5
PS C:\> Set-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="0bf57-114">Hier finden Sie eine allgemeine Beschreibung der Schritte zum Ändern einer Schutzrichtlinie:</span><span class="sxs-lookup"><span data-stu-id="0bf57-114">Here is the high-level description of the steps to be followed for modifying a protection policy:</span></span> 
1.  <span data-ttu-id="0bf57-115">Erhalten Sie eine Basis "SchedulePolicyObject" und "RetentionPolicyObject".</span><span class="sxs-lookup"><span data-stu-id="0bf57-115">Get a base SchedulePolicyObject and base RetentionPolicyObject.</span></span> <span data-ttu-id="0bf57-116">Speichern Sie sie in einer Variablen.</span><span class="sxs-lookup"><span data-stu-id="0bf57-116">Store them in some variable.</span></span>
2.  <span data-ttu-id="0bf57-117">Legen Sie die verschiedenen Parameter des Zeitplan- und Aufbewahrungsrichtlinienobjekts ihren Anforderungen nach fest.</span><span class="sxs-lookup"><span data-stu-id="0bf57-117">Set the different parameters of schedule and retention policy object as per your requirement.</span></span> <span data-ttu-id="0bf57-118">Beispiel: Im obigen Beispielskript versuchen wir, eine wöchentliche Schutzrichtlinie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0bf57-118">For example- In the above sample script, we are trying to set a weekly protection policy.</span></span> <span data-ttu-id="0bf57-119">Daher haben wir die Terminplanhäufigkeit in "Wöchentlich" geändert und außerdem die Ausführungszeit des Zeitplans aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0bf57-119">Hence, we changed the schedule frequency to "Weekly" and also updated the schedule run time.</span></span> <span data-ttu-id="0bf57-120">Im Aufbewahrungsrichtlinienobjekt haben wir die wöchentliche Aufbewahrungsdauer aktualisiert und das richtige Kennzeichen "Wochenplan aktiviert" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0bf57-120">In the retention policy object, we updated the weekly retention duration and set the correct "weekly schedule enabled" flag.</span></span> <span data-ttu-id="0bf57-121">Legen Sie für den Fall, dass Sie eine tägliche Richtlinie festlegen möchten, das Kennzeichen "Tagesplan aktiviert" auf "true" fest, und weisen Sie geeignete Werte für andere Objektparameter zu.</span><span class="sxs-lookup"><span data-stu-id="0bf57-121">In case you want to set a Daily policy, set the "daily schedule enabled" flag to true and assign appropriate values for other object parameters.</span></span>
3.  <span data-ttu-id="0bf57-122">Holen Sie sich die Sicherungsschutzrichtlinie, die Sie ändern möchten, und speichern Sie sie in einer Variablen.</span><span class="sxs-lookup"><span data-stu-id="0bf57-122">Get the backup protection policy that you want to modify and store it in a variable.</span></span> <span data-ttu-id="0bf57-123">Im vorstehenden Beispiel haben wir die Sicherungsrichtlinie mit dem Namen "TestPolicy" abgerufen, den wir ändern wollten.</span><span class="sxs-lookup"><span data-stu-id="0bf57-123">In the above example, we retrieved the backup policy with the name "TestPolicy" that we wanted to modify.</span></span>
4.  <span data-ttu-id="0bf57-124">Ändern Sie die in Schritt 3 abgerufene Sicherungsschutzrichtlinie mit dem geänderten Richtlinienobjekt und Aufbewahrungsrichtlinienobjekt.</span><span class="sxs-lookup"><span data-stu-id="0bf57-124">Modify the backup protection policy retrieved in step 3 using the modified schedule policy object and retention policy object.</span></span>

## <span data-ttu-id="0bf57-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0bf57-125">PARAMETERS</span></span>

### <span data-ttu-id="0bf57-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bf57-126">-DefaultProfile</span></span>
<span data-ttu-id="0bf57-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0bf57-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bf57-128">-FixForInconsistentItems</span><span class="sxs-lookup"><span data-stu-id="0bf57-128">-FixForInconsistentItems</span></span>
<span data-ttu-id="0bf57-129">"Parameter wechseln", der angibt, ob die Richtlinienaktualisierung für fehlgeschlagene Elemente erneut verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0bf57-129">Switch Parameter indicating whether or not to retry Policy Update for failed items.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FixPolicyParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bf57-130">-Policy</span><span class="sxs-lookup"><span data-stu-id="0bf57-130">-Policy</span></span>
<span data-ttu-id="0bf57-131">Gibt die Sicherungsschutzrichtlinie an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0bf57-131">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="0bf57-132">Zum Abrufen eines **"BackupProtectionPolicy"-Objekts** verwenden Sie das Get-AzRecoveryServicesBackupProtectionPolicy Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bf57-132">To obtain a **BackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0bf57-133">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0bf57-133">-RetentionPolicy</span></span>
<span data-ttu-id="0bf57-134">Gibt die Basisaufbewahrungsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="0bf57-134">Specifies the base retention policy.</span></span>
<span data-ttu-id="0bf57-135">Zum Abrufen eines **RetentionPolicy-Objekts** verwenden Sie das Get-AzRecoveryServicesBackupRetentionPolicyObject-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bf57-135">To obtain a **RetentionPolicy** object, use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: ModifyPolicyParamSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bf57-136">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="0bf57-136">-SchedulePolicy</span></span>
<span data-ttu-id="0bf57-137">Gibt das Basisplanrichtlinienobjekt an.</span><span class="sxs-lookup"><span data-stu-id="0bf57-137">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="0bf57-138">Um ein **"SchedulePolicy"-Objekt zu** erhalten, verwenden Sie das Get-AzRecoveryServicesBackupSchedulePolicyObject-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0bf57-138">To obtain a **SchedulePolicy** object, use the Get-AzRecoveryServicesBackupSchedulePolicyObject object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: ModifyPolicyParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bf57-139">-VaultId</span><span class="sxs-lookup"><span data-stu-id="0bf57-139">-VaultId</span></span>
<span data-ttu-id="0bf57-140">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="0bf57-140">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0bf57-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0bf57-141">-Confirm</span></span>
<span data-ttu-id="0bf57-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0bf57-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bf57-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0bf57-143">-WhatIf</span></span>
<span data-ttu-id="0bf57-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0bf57-144">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="0bf57-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bf57-145">CommonParameters</span></span>
<span data-ttu-id="0bf57-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bf57-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bf57-147">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0bf57-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bf57-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0bf57-148">INPUTS</span></span>

### <span data-ttu-id="0bf57-149">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="0bf57-149">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="0bf57-150">System.String</span><span class="sxs-lookup"><span data-stu-id="0bf57-150">System.String</span></span>

## <span data-ttu-id="0bf57-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0bf57-151">OUTPUTS</span></span>

### <span data-ttu-id="0bf57-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="0bf57-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="0bf57-153">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0bf57-153">NOTES</span></span>

## <span data-ttu-id="0bf57-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0bf57-154">RELATED LINKS</span></span>

[<span data-ttu-id="0bf57-155">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0bf57-155">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="0bf57-156">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="0bf57-156">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="0bf57-157">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0bf57-157">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="0bf57-158">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0bf57-158">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


