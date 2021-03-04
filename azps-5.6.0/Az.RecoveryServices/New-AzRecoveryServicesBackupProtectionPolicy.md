---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 65bda3a4829971ce3d073c672b578099130fae6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919272"
---
# <span data-ttu-id="382ea-101">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="382ea-101">New-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="382ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="382ea-102">SYNOPSIS</span></span>
<span data-ttu-id="382ea-103">Erstellt eine Sicherungsschutzrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="382ea-103">Creates a Backup protection policy.</span></span>

## <span data-ttu-id="382ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="382ea-104">SYNTAX</span></span>

```
New-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="382ea-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="382ea-105">DESCRIPTION</span></span>
<span data-ttu-id="382ea-106">Das **Cmdlet New-AzRecoveryServicesBackupProtectionPolicy** erstellt eine Sicherungsschutzrichtlinie in einem Tresor.</span><span class="sxs-lookup"><span data-stu-id="382ea-106">The **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="382ea-107">Eine Schutzrichtlinie ist mindestens einer Aufbewahrungsrichtlinie zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="382ea-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="382ea-108">Die Aufbewahrungsrichtlinie definiert, wie lange ein Wiederherstellungspunkt mit Azure Backup aufbewahrt wird.</span><span class="sxs-lookup"><span data-stu-id="382ea-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>
<span data-ttu-id="382ea-109">Sie können das cmdlet Get-AzRecoveryServicesBackupRetentionPolicyObject verwenden, um die Standardaufbewahrungsrichtlinie zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="382ea-109">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="382ea-110">Und Sie können das Get-AzRecoveryServicesBackupSchedulePolicyObject-Cmdlet verwenden, um die Standardzeitplanrichtlinie zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="382ea-110">And you can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="382ea-111">Die **Objekte SchedulePolicy** und **RetentionPolicy** werden als Eingaben für das **Cmdlet New-AzRecoveryServicesBackupProtectionPolicy** verwendet.</span><span class="sxs-lookup"><span data-stu-id="382ea-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="382ea-112">Legen Sie den Tresorkontext mithilfe des cmdlets Set-AzRecoveryServicesVaultContext, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="382ea-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="382ea-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="382ea-113">EXAMPLES</span></span>

### <span data-ttu-id="382ea-114">Beispiel 1: Erstellen einer Sicherungsschutzrichtlinie</span><span class="sxs-lookup"><span data-stu-id="382ea-114">Example 1: Create a Backup protection policy</span></span>
```powershell
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="382ea-115">Der erste Befehl ruft ein **SchedulePolicyObject**-Basisobjekt ab und speichert es dann in der $SchPol Variablen.</span><span class="sxs-lookup"><span data-stu-id="382ea-115">The first command gets a base **SchedulePolicyObject**, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="382ea-116">Mit dem zweiten Befehl werden alle geplanten Laufzeiten aus der Zeitplanrichtlinie in $SchPol.</span><span class="sxs-lookup"><span data-stu-id="382ea-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="382ea-117">Der dritte Befehl verwendet das cmdlet Get-Date, um das aktuelle Datum und die aktuelle Uhrzeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="382ea-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>
<span data-ttu-id="382ea-118">Mit dem vierten Befehl werden das aktuelle Datum und die aktuelle Uhrzeit in $Dt der Zeitplanrichtlinie als geplante Laufzeit addiert.</span><span class="sxs-lookup"><span data-stu-id="382ea-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>
<span data-ttu-id="382ea-119">Der fünfte Befehl ruft ein Base **RetentionPolicy-Objekt** ab und speichert es dann in der $RetPol-Variable.</span><span class="sxs-lookup"><span data-stu-id="382ea-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="382ea-120">Der sechste Befehl legt die Aufbewahrungsdauerrichtlinie auf 365 Tage fest.</span><span class="sxs-lookup"><span data-stu-id="382ea-120">The sixth command sets the retention duration policy to 365 days.</span></span>
<span data-ttu-id="382ea-121">Der letzte Befehl erstellt ein **BackupProtectionPolicy-Objekt** basierend auf den Zeitplan- und Aufbewahrungsrichtlinien, die mit den vorherigen Befehlen erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="382ea-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

### <span data-ttu-id="382ea-122">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="382ea-122">Example 2</span></span>

<span data-ttu-id="382ea-123">Erstellt eine Sicherungsschutzrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="382ea-123">Creates a Backup protection policy.</span></span> <span data-ttu-id="382ea-124">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="382ea-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzRecoveryServicesBackupProtectionPolicy -Name 'NewPolicy' -RetentionPolicy $RetPol -SchedulePolicy $SchPol -VaultId $vault.ID -WorkloadType AzureVM
```

## <span data-ttu-id="382ea-125">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="382ea-125">PARAMETERS</span></span>

### <span data-ttu-id="382ea-126">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="382ea-126">-BackupManagementType</span></span>
<span data-ttu-id="382ea-127">Die Klasse der zu schützenden Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="382ea-127">The class of resources being protected.</span></span> <span data-ttu-id="382ea-128">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="382ea-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="382ea-129">AzureVM</span><span class="sxs-lookup"><span data-stu-id="382ea-129">AzureVM</span></span> 
- <span data-ttu-id="382ea-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="382ea-130">AzureStorage</span></span>
- <span data-ttu-id="382ea-131">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="382ea-131">AzureWorkload</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="382ea-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="382ea-132">-DefaultProfile</span></span>
<span data-ttu-id="382ea-133">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="382ea-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="382ea-134">-Name</span><span class="sxs-lookup"><span data-stu-id="382ea-134">-Name</span></span>
<span data-ttu-id="382ea-135">Gibt den Namen der Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="382ea-135">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="382ea-136">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="382ea-136">-RetentionPolicy</span></span>
<span data-ttu-id="382ea-137">Gibt das **Basis-RetentionPolicy-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="382ea-137">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="382ea-138">Sie können das Get-AzRecoveryServicesBackupRetentionPolicyObject verwenden, um ein **RetentionPolicy-Objekt zu** erhalten.</span><span class="sxs-lookup"><span data-stu-id="382ea-138">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

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

### <span data-ttu-id="382ea-139">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="382ea-139">-SchedulePolicy</span></span>
<span data-ttu-id="382ea-140">Gibt das **Basisobjekt SchedulePolicy** an.</span><span class="sxs-lookup"><span data-stu-id="382ea-140">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="382ea-141">Sie können das cmdlet Get-AzRecoveryServicesBackupSchedulePolicyObject verwenden, um ein **SchedulePolicy-Objekt zu** erhalten.</span><span class="sxs-lookup"><span data-stu-id="382ea-141">You can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

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

### <span data-ttu-id="382ea-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="382ea-142">-VaultId</span></span>
<span data-ttu-id="382ea-143">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="382ea-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="382ea-144">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="382ea-144">-WorkloadType</span></span>
<span data-ttu-id="382ea-145">Arbeitsauslastungstyp der Ressource.</span><span class="sxs-lookup"><span data-stu-id="382ea-145">Workload type of the resource.</span></span> <span data-ttu-id="382ea-146">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="382ea-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="382ea-147">AzureVM</span><span class="sxs-lookup"><span data-stu-id="382ea-147">AzureVM</span></span> 
- <span data-ttu-id="382ea-148">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="382ea-148">AzureFiles</span></span>
- <span data-ttu-id="382ea-149">MSSQL</span><span class="sxs-lookup"><span data-stu-id="382ea-149">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="382ea-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="382ea-150">-Confirm</span></span>
<span data-ttu-id="382ea-151">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="382ea-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="382ea-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="382ea-152">-WhatIf</span></span>
<span data-ttu-id="382ea-153">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="382ea-153">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="382ea-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="382ea-154">CommonParameters</span></span>
<span data-ttu-id="382ea-155">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="382ea-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="382ea-156">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="382ea-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="382ea-157">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="382ea-157">INPUTS</span></span>

### <span data-ttu-id="382ea-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType</span><span class="sxs-lookup"><span data-stu-id="382ea-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType</span></span>

### <span data-ttu-id="382ea-159">System.Nullable'1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.Models, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="382ea-159">System.Nullable\`1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.Models, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="382ea-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="382ea-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

### <span data-ttu-id="382ea-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="382ea-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

### <span data-ttu-id="382ea-162">System.String</span><span class="sxs-lookup"><span data-stu-id="382ea-162">System.String</span></span>

## <span data-ttu-id="382ea-163">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="382ea-163">OUTPUTS</span></span>

### <span data-ttu-id="382ea-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="382ea-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="382ea-165">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="382ea-165">NOTES</span></span>

## <span data-ttu-id="382ea-166">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="382ea-166">RELATED LINKS</span></span>

[<span data-ttu-id="382ea-167">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="382ea-167">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="382ea-168">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="382ea-168">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="382ea-169">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="382ea-169">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="382ea-170">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="382ea-170">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="382ea-171">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="382ea-171">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="382ea-172">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="382ea-172">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


