---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: f9cd7064c1949639526f2e7b84f01fb6355b584f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174226"
---
# <span data-ttu-id="aee5a-101">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="aee5a-101">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="aee5a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aee5a-102">SYNOPSIS</span></span>
<span data-ttu-id="aee5a-103">Ändert eine Sicherungsschutz Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="aee5a-103">Modifies a Backup protection policy.</span></span>

## <span data-ttu-id="aee5a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aee5a-104">SYNTAX</span></span>

### <span data-ttu-id="aee5a-105">ModifyPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="aee5a-105">ModifyPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aee5a-106">FixPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="aee5a-106">FixPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-FixForInconsistentItems]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aee5a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aee5a-107">DESCRIPTION</span></span>
<span data-ttu-id="aee5a-108">Das Cmdlet " **festlegen-AzRecoveryServicesBackupProtectionPolicy** " ändert eine vorhandene Azure Backup-Schutzrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="aee5a-108">The **Set-AzRecoveryServicesBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="aee5a-109">Sie können die Komponenten für den Sicherungszeitplan und die Aufbewahrungsrichtlinie ändern.</span><span class="sxs-lookup"><span data-stu-id="aee5a-109">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="aee5a-110">Alle Änderungen, die Sie vornehmen, wirken sich auf die Sicherung und Aufbewahrung der Elemente aus, die der Richtlinie zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="aee5a-110">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="aee5a-111">Setzen Sie den Vault-Kontext mithilfe des Set-AzRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="aee5a-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="aee5a-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aee5a-112">EXAMPLES</span></span>

### <span data-ttu-id="aee5a-113">Beispiel 1: Ändern einer Sicherungsschutz Richtlinie</span><span class="sxs-lookup"><span data-stu-id="aee5a-113">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> $Pol.AzureBackupRGName = "RG_prefix"
PS C:\> $Pol.AzureBackupRGNameSuffix = "RG_suffix"
PS C:\> Set-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="aee5a-114">Der erste Befehl ruft ein Basis SchedulePolicy-Objekt ab und speichert es dann in der $SchPol-Variablen.</span><span class="sxs-lookup"><span data-stu-id="aee5a-114">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="aee5a-115">Der zweite Befehl entfernt alle geplanten Ausführungszeiten aus der Terminplan Richtlinie in $SchPol.</span><span class="sxs-lookup"><span data-stu-id="aee5a-115">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="aee5a-116">Der dritte Befehl verwendet das Get-Date-Cmdlet, um das aktuelle Datum und die aktuelle Uhrzeit abzurufen, und speichert es dann in der $dt-Variablen.</span><span class="sxs-lookup"><span data-stu-id="aee5a-116">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="aee5a-117">Der vierte Befehl addiert das Datum und die Uhrzeit in $dt zur Zeit Plan Laufzeit für die Terminplan Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="aee5a-117">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>
<span data-ttu-id="aee5a-118">Der fünfte Befehl ruft ein Basis Aufbewahrungsrichtlinienobjekt ab und speichert es dann in der $RetPol Variablen.</span><span class="sxs-lookup"><span data-stu-id="aee5a-118">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="aee5a-119">Der sechste Befehl legt die Aufbewahrungsdauer auf 365 Tage fest.</span><span class="sxs-lookup"><span data-stu-id="aee5a-119">The sixth command sets the retention duration to 365 days.</span></span>
<span data-ttu-id="aee5a-120">Der siebte Befehl ruft die Sicherungsschutz Richtlinie mit dem Namen "Richtlinie" ab und speichert Sie dann in der $Pol-Variablen.</span><span class="sxs-lookup"><span data-stu-id="aee5a-120">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="aee5a-121">Mit dem achten und neunten werden die Ressourcengruppen Parameter festgelegt, die der Richtlinie zugeordnet sind, die die Wiederherstellungspunkte speichert.</span><span class="sxs-lookup"><span data-stu-id="aee5a-121">The eighth and ninth sets the resource group parameters associated with policy which stores the restore points.</span></span>
<span data-ttu-id="aee5a-122">Der endgültige Befehl ändert die Richtlinie für den Sicherungsschutz in $Pol mithilfe der Zeit Plan Richtlinie in $SchPol und der Aufbewahrungsrichtlinie in $RetPol.</span><span class="sxs-lookup"><span data-stu-id="aee5a-122">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="aee5a-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="aee5a-123">PARAMETERS</span></span>

### <span data-ttu-id="aee5a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aee5a-124">-DefaultProfile</span></span>
<span data-ttu-id="aee5a-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aee5a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aee5a-126">-FixForInconsistentItems</span><span class="sxs-lookup"><span data-stu-id="aee5a-126">-FixForInconsistentItems</span></span>
<span data-ttu-id="aee5a-127">Switch-Parameter, der angibt, ob die Richtlinienaktualisierung für fehlerhafte Elemente wiederholt werden soll.</span><span class="sxs-lookup"><span data-stu-id="aee5a-127">Switch Parameter indicating whether or not to retry Policy Update for failed items.</span></span>

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

### <span data-ttu-id="aee5a-128">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="aee5a-128">-Policy</span></span>
<span data-ttu-id="aee5a-129">Gibt die Richtlinie für den Sicherungsschutz an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="aee5a-129">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="aee5a-130">Verwenden Sie das Get-AzRecoveryServicesBackupProtectionPolicy-Cmdlet, um ein **BackupProtectionPolicy** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="aee5a-130">To obtain a **BackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="aee5a-131">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="aee5a-131">-RetentionPolicy</span></span>
<span data-ttu-id="aee5a-132">Gibt die Basis Aufbewahrungsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="aee5a-132">Specifies the base retention policy.</span></span>
<span data-ttu-id="aee5a-133">Verwenden Sie das Get-AzRecoveryServicesBackupRetentionPolicyObject-Cmdlet, um ein **RetentionPolicy** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="aee5a-133">To obtain a **RetentionPolicy** object, use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

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

### <span data-ttu-id="aee5a-134">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="aee5a-134">-SchedulePolicy</span></span>
<span data-ttu-id="aee5a-135">Gibt das Basis Zeitplan-Richtlinienobjekt an.</span><span class="sxs-lookup"><span data-stu-id="aee5a-135">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="aee5a-136">Verwenden Sie zum Abrufen eines **SchedulePolicy** -Objekts das Get-AzRecoveryServicesBackupSchedulePolicyObject-Objekt.</span><span class="sxs-lookup"><span data-stu-id="aee5a-136">To obtain a **SchedulePolicy** object, use the Get-AzRecoveryServicesBackupSchedulePolicyObject object.</span></span>

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

### <span data-ttu-id="aee5a-137">-Tresor</span><span class="sxs-lookup"><span data-stu-id="aee5a-137">-VaultId</span></span>
<span data-ttu-id="aee5a-138">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="aee5a-138">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="aee5a-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aee5a-139">-Confirm</span></span>
<span data-ttu-id="aee5a-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aee5a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aee5a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aee5a-141">-WhatIf</span></span>
<span data-ttu-id="aee5a-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aee5a-142">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="aee5a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aee5a-143">CommonParameters</span></span>
<span data-ttu-id="aee5a-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aee5a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aee5a-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aee5a-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aee5a-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aee5a-146">INPUTS</span></span>

### <span data-ttu-id="aee5a-147">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="aee5a-147">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="aee5a-148">System. String</span><span class="sxs-lookup"><span data-stu-id="aee5a-148">System.String</span></span>

## <span data-ttu-id="aee5a-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aee5a-149">OUTPUTS</span></span>

### <span data-ttu-id="aee5a-150">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="aee5a-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="aee5a-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="aee5a-151">NOTES</span></span>

## <span data-ttu-id="aee5a-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aee5a-152">RELATED LINKS</span></span>

[<span data-ttu-id="aee5a-153">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="aee5a-153">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="aee5a-154">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="aee5a-154">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="aee5a-155">Neu – AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="aee5a-155">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="aee5a-156">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="aee5a-156">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


