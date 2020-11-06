---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/set-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: fb0373e97d719535c87c01c0a4b53b029cc2a878
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500146"
---
# <span data-ttu-id="2cc6b-101">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2cc6b-101">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="2cc6b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2cc6b-102">SYNOPSIS</span></span>
<span data-ttu-id="2cc6b-103">Ändert eine Sicherungsschutz Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-103">Modifies a Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cc6b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2cc6b-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase>
 [[-RetentionPolicy] <RetentionPolicyBase>] [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cc6b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2cc6b-105">DESCRIPTION</span></span>
<span data-ttu-id="2cc6b-106">Das Cmdlet " **festlegen-AzureRmBackupProtectionPolicy** " ändert eine vorhandene Azure Backup-Schutzrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-106">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="2cc6b-107">Sie können die Komponenten für den Sicherungszeitplan und die Aufbewahrungsrichtlinie ändern.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-107">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="2cc6b-108">Alle Änderungen, die Sie vornehmen, wirken sich auf die Sicherung und Aufbewahrung der Elemente aus, die der Richtlinie zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-108">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="2cc6b-109">Setzen Sie den Vault-Kontext mithilfe des Set-AzureRmRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="2cc6b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2cc6b-110">EXAMPLES</span></span>

### <span data-ttu-id="2cc6b-111">Beispiel 1: Ändern einer Sicherungsschutz Richtlinie</span><span class="sxs-lookup"><span data-stu-id="2cc6b-111">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\>$SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Set-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="2cc6b-112">Der erste Befehl ruft ein Basis SchedulePolicy-Objekt ab und speichert es dann in der $SchPol-Variablen.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-112">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="2cc6b-113">Der zweite Befehl entfernt alle geplanten Ausführungszeiten aus der Terminplan Richtlinie in $SchPol.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-113">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="2cc6b-114">Der dritte Befehl verwendet das Get-Date-Cmdlet, um das aktuelle Datum und die aktuelle Uhrzeit abzurufen, und speichert es dann in der $dt-Variablen.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-114">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="2cc6b-115">Der vierte Befehl addiert das Datum und die Uhrzeit in $dt zur Zeit Plan Laufzeit für die Terminplan Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-115">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>
<span data-ttu-id="2cc6b-116">Der fünfte Befehl ruft ein Basis Aufbewahrungsrichtlinienobjekt ab und speichert es dann in der $RetPol Variablen.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-116">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="2cc6b-117">Der sechste Befehl legt die Aufbewahrungsdauer auf 365 Tage fest.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-117">The sixth command sets the retention duration to 365 days.</span></span>
<span data-ttu-id="2cc6b-118">Der siebte Befehl ruft die Sicherungsschutz Richtlinie mit dem Namen "Richtlinie" ab und speichert Sie dann in der $Pol-Variablen.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-118">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="2cc6b-119">Der endgültige Befehl ändert die Richtlinie für den Sicherungsschutz in $Pol mithilfe der Zeit Plan Richtlinie in $SchPol und der Aufbewahrungsrichtlinie in $RetPol.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-119">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="2cc6b-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="2cc6b-120">PARAMETERS</span></span>

### <span data-ttu-id="2cc6b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cc6b-121">-DefaultProfile</span></span>
<span data-ttu-id="2cc6b-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cc6b-123">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="2cc6b-123">-Policy</span></span>
<span data-ttu-id="2cc6b-124">Gibt die Richtlinie für den Sicherungsschutz an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-124">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="2cc6b-125">Verwenden Sie das Get-AzureRmRecoveryServicesBackupProtectionPolicy-Cmdlet, um ein **BackupProtectionPolicy** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-125">To obtain a **BackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="2cc6b-126">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2cc6b-126">-RetentionPolicy</span></span>
<span data-ttu-id="2cc6b-127">Gibt die Basis Aufbewahrungsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-127">Specifies the base retention policy.</span></span>
<span data-ttu-id="2cc6b-128">Verwenden Sie das Get-AzureRmRecoveryServicesBackupRetentionPolicyObject-Cmdlet, um ein **RetentionPolicy** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-128">To obtain a **RetentionPolicy** object, use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

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

### <span data-ttu-id="2cc6b-129">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="2cc6b-129">-SchedulePolicy</span></span>
<span data-ttu-id="2cc6b-130">Gibt das Basis Zeitplan-Richtlinienobjekt an.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-130">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="2cc6b-131">Verwenden Sie zum Abrufen eines **SchedulePolicy** -Objekts das Get-AzureRmRecoveryServicesBackupSchedulePolicyObject-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-131">To obtain a **SchedulePolicy** object, use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject object.</span></span>

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

### <span data-ttu-id="2cc6b-132">-Tresor</span><span class="sxs-lookup"><span data-stu-id="2cc6b-132">-VaultId</span></span>
<span data-ttu-id="2cc6b-133">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="2cc6b-133">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="2cc6b-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2cc6b-134">-Confirm</span></span>
<span data-ttu-id="2cc6b-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cc6b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cc6b-136">-WhatIf</span></span>
<span data-ttu-id="2cc6b-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2cc6b-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cc6b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cc6b-139">CommonParameters</span></span>
<span data-ttu-id="2cc6b-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cc6b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cc6b-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cc6b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cc6b-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2cc6b-142">INPUTS</span></span>

### <span data-ttu-id="2cc6b-143">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="2cc6b-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>
<span data-ttu-id="2cc6b-144">Parameter: Richtlinie (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2cc6b-144">Parameters: Policy (ByValue)</span></span>

### <span data-ttu-id="2cc6b-145">System. String</span><span class="sxs-lookup"><span data-stu-id="2cc6b-145">System.String</span></span>
<span data-ttu-id="2cc6b-146">Parameter: Vault-ByValue</span><span class="sxs-lookup"><span data-stu-id="2cc6b-146">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="2cc6b-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2cc6b-147">OUTPUTS</span></span>

### <span data-ttu-id="2cc6b-148">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="2cc6b-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="2cc6b-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="2cc6b-149">NOTES</span></span>

## <span data-ttu-id="2cc6b-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2cc6b-150">RELATED LINKS</span></span>

[<span data-ttu-id="2cc6b-151">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2cc6b-151">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="2cc6b-152">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="2cc6b-152">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="2cc6b-153">Neu – AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2cc6b-153">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="2cc6b-154">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2cc6b-154">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)


