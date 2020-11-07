---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 1f7dcd013bb91b8ba209cf3f7b031a90f7bb49cc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659811"
---
# <span data-ttu-id="8f7a6-101">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8f7a6-101">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="8f7a6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8f7a6-102">SYNOPSIS</span></span>
<span data-ttu-id="8f7a6-103">Ändert eine Sicherungsschutz Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="8f7a6-103">Modifies a Backup protection policy.</span></span>

## <span data-ttu-id="8f7a6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f7a6-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f7a6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8f7a6-105">DESCRIPTION</span></span>
<span data-ttu-id="8f7a6-106">Das Cmdlet " **festlegen-AzBackupProtectionPolicy** " ändert eine vorhandene Azure Backup-Schutzrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="8f7a6-106">The **Set-AzBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="8f7a6-107">Sie können die Komponenten für den Sicherungszeitplan und die Aufbewahrungsrichtlinie ändern.</span><span class="sxs-lookup"><span data-stu-id="8f7a6-107">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="8f7a6-108">Alle Änderungen, die Sie vornehmen, wirken sich auf die Sicherung und Aufbewahrung der Elemente aus, die der Richtlinie zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="8f7a6-108">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="8f7a6-109">Setzen Sie den Vault-Kontext mithilfe des Set-AzRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="8f7a6-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="8f7a6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8f7a6-110">EXAMPLES</span></span>

### <span data-ttu-id="8f7a6-111">Beispiel 1: Ändern einer Sicherungsschutz Richtlinie</span><span class="sxs-lookup"><span data-stu-id="8f7a6-111">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Set-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="8f7a6-112">Der erste Befehl ruft ein Basis SchedulePolicy-Objekt ab und speichert es dann in der $SchPol-Variablen.</span><span class="sxs-lookup"><span data-stu-id="8f7a6-112">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="8f7a6-113">Der zweite Befehl entfernt alle geplanten Ausführungszeiten aus der Terminplan Richtlinie in $SchPol.</span><span class="sxs-lookup"><span data-stu-id="8f7a6-113">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="8f7a6-114">Der dritte Befehl verwendet das Get-Date-Cmdlet, um das aktuelle Datum und die aktuelle Uhrzeit abzurufen, und speichert es dann in der $dt-Variablen.</span><span class="sxs-lookup"><span data-stu-id="8f7a6-114">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="8f7a6-115">Der vierte Befehl addiert das Datum und die Uhrzeit in $dt zur Zeit Plan Laufzeit für die Terminplan Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="8f7a6-115">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>
<span data-ttu-id="8f7a6-116">Der fünfte Befehl ruft ein Basis Aufbewahrungsrichtlinienobjekt ab und speichert es dann in der $RetPol Variablen.</span><span class="sxs-lookup"><span data-stu-id="8f7a6-116">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="8f7a6-117">Der sechste Befehl legt die Aufbewahrungsdauer auf 365 Tage fest.</span><span class="sxs-lookup"><span data-stu-id="8f7a6-117">The sixth command sets the retention duration to 365 days.</span></span>
<span data-ttu-id="8f7a6-118">Der siebte Befehl ruft die Sicherungsschutz Richtlinie mit dem Namen "Richtlinie" ab und speichert Sie dann in der $Pol-Variablen.</span><span class="sxs-lookup"><span data-stu-id="8f7a6-118">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="8f7a6-119">Der endgültige Befehl ändert die Richtlinie für den Sicherungsschutz in $Pol mithilfe der Zeit Plan Richtlinie in $SchPol und der Aufbewahrungsrichtlinie in $RetPol.</span><span class="sxs-lookup"><span data-stu-id="8f7a6-119">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="8f7a6-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f7a6-120">PARAMETERS</span></span>

### <span data-ttu-id="8f7a6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f7a6-121">-DefaultProfile</span></span>
<span data-ttu-id="8f7a6-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8f7a6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f7a6-123">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="8f7a6-123">-Policy</span></span>
<span data-ttu-id="8f7a6-124">Gibt die Richtlinie für den Sicherungsschutz an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="8f7a6-124">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="8f7a6-125">Verwenden Sie das Get-AzRecoveryServicesBackupProtectionPolicy-Cmdlet, um ein **BackupProtectionPolicy** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8f7a6-125">To obtain a **BackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="8f7a6-126">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8f7a6-126">-RetentionPolicy</span></span>
<span data-ttu-id="8f7a6-127">Gibt die Basis Aufbewahrungsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="8f7a6-127">Specifies the base retention policy.</span></span>
<span data-ttu-id="8f7a6-128">Verwenden Sie das Get-AzRecoveryServicesBackupRetentionPolicyObject-Cmdlet, um ein **RetentionPolicy** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8f7a6-128">To obtain a **RetentionPolicy** object, use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f7a6-129">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="8f7a6-129">-SchedulePolicy</span></span>
<span data-ttu-id="8f7a6-130">Gibt das Basis Zeitplan-Richtlinienobjekt an.</span><span class="sxs-lookup"><span data-stu-id="8f7a6-130">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="8f7a6-131">Verwenden Sie zum Abrufen eines **SchedulePolicy** -Objekts das Get-AzRecoveryServicesBackupSchedulePolicyObject-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8f7a6-131">To obtain a **SchedulePolicy** object, use the Get-AzRecoveryServicesBackupSchedulePolicyObject object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f7a6-132">-Tresor</span><span class="sxs-lookup"><span data-stu-id="8f7a6-132">-VaultId</span></span>
<span data-ttu-id="8f7a6-133">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="8f7a6-133">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8f7a6-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8f7a6-134">-Confirm</span></span>
<span data-ttu-id="8f7a6-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8f7a6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f7a6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f7a6-136">-WhatIf</span></span>
<span data-ttu-id="8f7a6-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8f7a6-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f7a6-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8f7a6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f7a6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f7a6-139">CommonParameters</span></span>
<span data-ttu-id="8f7a6-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f7a6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f7a6-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f7a6-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f7a6-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8f7a6-142">INPUTS</span></span>

### <span data-ttu-id="8f7a6-143">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="8f7a6-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="8f7a6-144">System. String</span><span class="sxs-lookup"><span data-stu-id="8f7a6-144">System.String</span></span>

## <span data-ttu-id="8f7a6-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8f7a6-145">OUTPUTS</span></span>

### <span data-ttu-id="8f7a6-146">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="8f7a6-146">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="8f7a6-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="8f7a6-147">NOTES</span></span>

## <span data-ttu-id="8f7a6-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8f7a6-148">RELATED LINKS</span></span>

[<span data-ttu-id="8f7a6-149">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8f7a6-149">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="8f7a6-150">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="8f7a6-150">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="8f7a6-151">Neu – AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8f7a6-151">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="8f7a6-152">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8f7a6-152">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


