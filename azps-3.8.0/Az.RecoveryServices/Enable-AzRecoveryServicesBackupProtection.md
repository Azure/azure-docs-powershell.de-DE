---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 7b52c6064f7dd692b732558b682290e8612f383c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846987"
---
# <span data-ttu-id="762cf-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="762cf-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="762cf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="762cf-102">SYNOPSIS</span></span>
<span data-ttu-id="762cf-103">Aktiviert die Sicherung für ein Element mit einer angegebenen Sicherungsschutz Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="762cf-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="762cf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="762cf-104">SYNTAX</span></span>

### <span data-ttu-id="762cf-105">AzureVMComputeEnableProtection (Standard)</span><span class="sxs-lookup"><span data-stu-id="762cf-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-ResourceGroupName] <String> [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="762cf-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="762cf-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String> [-ServiceName] <String>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ExcludeAllDataDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="762cf-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="762cf-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="762cf-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="762cf-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="762cf-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="762cf-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Item] <ItemBase>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ResetExclusionSettings]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="762cf-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="762cf-110">DESCRIPTION</span></span>
<span data-ttu-id="762cf-111">Das Cmdlet **enable-AzRecoveryServicesBackupProtection** legt die Azure-Sicherungsschutz Richtlinie für ein Element fest.</span><span class="sxs-lookup"><span data-stu-id="762cf-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>
<span data-ttu-id="762cf-112">Setzen Sie den Vault-Kontext mithilfe des Set-AzRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="762cf-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="762cf-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="762cf-113">EXAMPLES</span></span>

### <span data-ttu-id="762cf-114">Beispiel 1: Aktivieren des Sicherungs Schutzes für ein Element</span><span class="sxs-lookup"><span data-stu-id="762cf-114">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $inclusionDiskLUNS = ("1", "2")
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1" -InclusionDisksList $inclusionDiskLUNS
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="762cf-115">Das erste Cmdlet ruft ein Standardrichtlinienobjekt ab und speichert es dann in der $Pol-Variablen.</span><span class="sxs-lookup"><span data-stu-id="762cf-115">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="762cf-116">Das zweite Cmdlet gibt die zu sichernden Datenträger-LUNs an und speichert Sie in $inclusionDiskLUNS Variablen.</span><span class="sxs-lookup"><span data-stu-id="762cf-116">The second cmdlet specifies the disk LUNs which are to be backed up and stores it in $inclusionDiskLUNS variable.</span></span>
<span data-ttu-id="762cf-117">Das dritte Cmdlet legt die Sicherungsschutz Richtlinie für den virtuellen Arm-Computer mit dem Namen V2VM mithilfe der Richtlinie in $Pol fest.</span><span class="sxs-lookup"><span data-stu-id="762cf-117">The third cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="762cf-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="762cf-118">PARAMETERS</span></span>

### <span data-ttu-id="762cf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="762cf-119">-DefaultProfile</span></span>
<span data-ttu-id="762cf-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="762cf-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="762cf-121">-ExcludeAllDataDisks</span><span class="sxs-lookup"><span data-stu-id="762cf-121">-ExcludeAllDataDisks</span></span>
<span data-ttu-id="762cf-122">Option zum angeben nur für Backup-Betriebssystemdatenträger</span><span class="sxs-lookup"><span data-stu-id="762cf-122">Option to specify to backup OS disks only</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="762cf-123">-ExclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="762cf-123">-ExclusionDisksList</span></span>
<span data-ttu-id="762cf-124">Liste der Datenträger-LUNs, die in einer Sicherung ausgeschlossen werden sollen</span><span class="sxs-lookup"><span data-stu-id="762cf-124">List of Disk LUNs to exclude in backup</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="762cf-125">-InclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="762cf-125">-InclusionDisksList</span></span>
<span data-ttu-id="762cf-126">Liste der Datenträger-LUNs, die in die Sicherung einbezogen werden sollen</span><span class="sxs-lookup"><span data-stu-id="762cf-126">List of Disk LUNs to include in backup</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="762cf-127">-Item</span><span class="sxs-lookup"><span data-stu-id="762cf-127">-Item</span></span>
<span data-ttu-id="762cf-128">Gibt das Sicherungselement an, für das dieses Cmdlet den Schutz aktiviert.</span><span class="sxs-lookup"><span data-stu-id="762cf-128">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="762cf-129">Verwenden Sie zum Abrufen eines **AzureRmRecoveryServicesBackupItem** das Get-AzRecoveryServicesBackupItem-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="762cf-129">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: ModifyProtection
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="762cf-130">-Name</span><span class="sxs-lookup"><span data-stu-id="762cf-130">-Name</span></span>
<span data-ttu-id="762cf-131">Gibt den Namen des sicherungselements an.</span><span class="sxs-lookup"><span data-stu-id="762cf-131">Specifies the name of the Backup item.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, AzureFileShareEnableProtection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="762cf-132">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="762cf-132">-Policy</span></span>
<span data-ttu-id="762cf-133">Gibt eine Schutzrichtlinie an, die mit diesem Cmdlet einem Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="762cf-133">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="762cf-134">Verwenden Sie das Get-AzRecoveryServicesBackupProtectionPolicy-Cmdlet, um ein **AzureRmRecoveryServicesBackupProtectionPolicy** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="762cf-134">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="762cf-135">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="762cf-135">-ProtectableItem</span></span>
<span data-ttu-id="762cf-136">Filter Wert für den Status des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="762cf-136">Filter value for status of job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: AzureWorkloadEnableProtection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="762cf-137">-ResetExclusionSettings</span><span class="sxs-lookup"><span data-stu-id="762cf-137">-ResetExclusionSettings</span></span>
<span data-ttu-id="762cf-138">Gibt an, dass die dem Element zugeordnete Datenträger Ausschluss Einstellung zurückgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="762cf-138">Specifies to reset disk exclusion setting associated with the item</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="762cf-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="762cf-139">-ResourceGroupName</span></span>
<span data-ttu-id="762cf-140">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="762cf-140">Specifies the name of the resource group.</span></span>
<span data-ttu-id="762cf-141">Geben Sie diesen Parameter nur für virtuelle Arm-Computer an.</span><span class="sxs-lookup"><span data-stu-id="762cf-141">Specify this parameter only for ARM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="762cf-142">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="762cf-142">-ServiceName</span></span>
<span data-ttu-id="762cf-143">Gibt den Namen des Diensts an.</span><span class="sxs-lookup"><span data-stu-id="762cf-143">Specifies the service name.</span></span>
<span data-ttu-id="762cf-144">Geben Sie diesen Parameter nur für ASM Virtual Machines an.</span><span class="sxs-lookup"><span data-stu-id="762cf-144">Specify this parameter only for ASM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMClassicComputeEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="762cf-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="762cf-145">-StorageAccountName</span></span>
<span data-ttu-id="762cf-146">Name des Azure File Share-speicherkontos</span><span class="sxs-lookup"><span data-stu-id="762cf-146">Azure file share storage account name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileShareEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="762cf-147">-Tresor</span><span class="sxs-lookup"><span data-stu-id="762cf-147">-VaultId</span></span>
<span data-ttu-id="762cf-148">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="762cf-148">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="762cf-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="762cf-149">-Confirm</span></span>
<span data-ttu-id="762cf-150">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="762cf-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="762cf-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="762cf-151">-WhatIf</span></span>
<span data-ttu-id="762cf-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="762cf-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="762cf-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="762cf-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="762cf-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="762cf-154">CommonParameters</span></span>
<span data-ttu-id="762cf-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="762cf-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="762cf-156">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="762cf-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="762cf-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="762cf-157">INPUTS</span></span>

### <span data-ttu-id="762cf-158">System. String</span><span class="sxs-lookup"><span data-stu-id="762cf-158">System.String</span></span>

### <span data-ttu-id="762cf-159">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="762cf-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="762cf-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="762cf-160">OUTPUTS</span></span>

### <span data-ttu-id="762cf-161">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="762cf-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="762cf-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="762cf-162">NOTES</span></span>

## <span data-ttu-id="762cf-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="762cf-163">RELATED LINKS</span></span>

[<span data-ttu-id="762cf-164">Deaktivieren-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="762cf-164">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="762cf-165">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="762cf-165">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


