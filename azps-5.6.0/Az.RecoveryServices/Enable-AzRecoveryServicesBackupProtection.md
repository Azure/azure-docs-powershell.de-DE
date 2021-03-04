---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 0472a24e15a05d1ea07639ee5495efc5feaaba6c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936640"
---
# <span data-ttu-id="758c3-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="758c3-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="758c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="758c3-102">SYNOPSIS</span></span>
<span data-ttu-id="758c3-103">Ermöglicht die Sicherung für ein Element mit einer angegebenen Sicherungsschutzrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="758c3-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="758c3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="758c3-104">SYNTAX</span></span>

### <span data-ttu-id="758c3-105">AzureVMComputeEnableProtection (Standard)</span><span class="sxs-lookup"><span data-stu-id="758c3-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-ResourceGroupName] <String> [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="758c3-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="758c3-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String> [-ServiceName] <String>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ExcludeAllDataDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="758c3-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="758c3-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="758c3-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="758c3-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="758c3-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="758c3-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Item] <ItemBase>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ResetExclusionSettings]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="758c3-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="758c3-110">DESCRIPTION</span></span>
<span data-ttu-id="758c3-111">Das **Cmdlet Enable-AzRecoveryServicesBackupProtection** ermöglicht die Sicherung, indem dem Element eine Schutzrichtlinie zuzuordnen ist.</span><span class="sxs-lookup"><span data-stu-id="758c3-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet enables the backup by associating a protection policy with the item.</span></span>
<span data-ttu-id="758c3-112">Wenn keine Richtlinien-ID vorhanden ist oder das Sicherungselement keine Richtlinie zugeordnet ist, erwartet dieser Befehl eine PolicyID.</span><span class="sxs-lookup"><span data-stu-id="758c3-112">If policy ID is not present or the backup item is not associated with any policy, then this command will expect a policyID.</span></span>
<span data-ttu-id="758c3-113">Legen Sie den Tresorkontext mithilfe des cmdlets Set-AzRecoveryServicesVaultContext, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="758c3-113">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="758c3-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="758c3-114">EXAMPLES</span></span>

### <span data-ttu-id="758c3-115">Beispiel 1: Aktivieren des Sicherungsschutzes für ein Element</span><span class="sxs-lookup"><span data-stu-id="758c3-115">Example 1: Enable Backup protection for an item</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $inclusionDiskLUNS = ("1", "2")
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1" -InclusionDisksList $inclusionDiskLUNS
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="758c3-116">Das erste Cmdlet ruft ein Standardrichtlinienobjekt ab und speichert es dann in der $Pol Variablen.</span><span class="sxs-lookup"><span data-stu-id="758c3-116">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="758c3-117">Das zweite Cmdlet gibt die Datenträger-LUNs an, die gesichert werden sollen, und speichert es in $inclusionDiskLUNS Variablen.</span><span class="sxs-lookup"><span data-stu-id="758c3-117">The second cmdlet specifies the disk LUNs which are to be backed up and stores it in $inclusionDiskLUNS variable.</span></span>
<span data-ttu-id="758c3-118">Das dritte Cmdlet legt die Sicherungsschutzrichtlinie für den ARM virtuellen Computer mit dem Namen V2VM mithilfe der Richtlinie in $Pol.</span><span class="sxs-lookup"><span data-stu-id="758c3-118">The third cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

### <span data-ttu-id="758c3-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="758c3-119">Example 2</span></span>

<span data-ttu-id="758c3-120">Ermöglicht die Sicherung für ein Element mit einer angegebenen Sicherungsschutzrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="758c3-120">Enables backup for an item with a specified Backup protection policy.</span></span> <span data-ttu-id="758c3-121">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="758c3-121">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupProtection -Item $Item -Policy $Pol -VaultId $vault
```

## <span data-ttu-id="758c3-122">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="758c3-122">PARAMETERS</span></span>

### <span data-ttu-id="758c3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="758c3-123">-DefaultProfile</span></span>
<span data-ttu-id="758c3-124">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="758c3-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="758c3-125">-ExcludeAllDataDisks</span><span class="sxs-lookup"><span data-stu-id="758c3-125">-ExcludeAllDataDisks</span></span>
<span data-ttu-id="758c3-126">Option zum Angeben, dass nur Betriebssystemdatenträger gesichert werden</span><span class="sxs-lookup"><span data-stu-id="758c3-126">Option to specify to backup OS disks only</span></span>

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

### <span data-ttu-id="758c3-127">-ExclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="758c3-127">-ExclusionDisksList</span></span>
<span data-ttu-id="758c3-128">Liste der Datenträger-LUNs, die in der Sicherung ausgeschlossen werden sollen, und die restlichen werden automatisch einbezogen.</span><span class="sxs-lookup"><span data-stu-id="758c3-128">List of Disk LUNs to be excluded in backup and the rest are automatically included.</span></span>

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

### <span data-ttu-id="758c3-129">-InclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="758c3-129">-InclusionDisksList</span></span>
<span data-ttu-id="758c3-130">Liste der Datenträger-LUNs, die in die Sicherung einbezogen werden sollen, und die restlichen werden mit Ausnahme des Betriebssystemdatenträgers automatisch ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="758c3-130">List of Disk LUNs to be included in backup and the rest are automatically excluded except OS disk.</span></span>

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

### <span data-ttu-id="758c3-131">-Item</span><span class="sxs-lookup"><span data-stu-id="758c3-131">-Item</span></span>
<span data-ttu-id="758c3-132">Gibt das Sicherungselement an, für das dieses Cmdlet schutzfähig ist.</span><span class="sxs-lookup"><span data-stu-id="758c3-132">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="758c3-133">Zum Abrufen eines **AzureRmRecoveryServicesBackupItem** verwenden Sie das Get-AzRecoveryServicesBackupItem Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="758c3-133">To obtain an **AzureRmRecoveryServicesBackupItem**, use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="758c3-134">-Name</span><span class="sxs-lookup"><span data-stu-id="758c3-134">-Name</span></span>
<span data-ttu-id="758c3-135">Gibt den Namen des Sicherungselements an.</span><span class="sxs-lookup"><span data-stu-id="758c3-135">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="758c3-136">-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="758c3-136">-Policy</span></span>
<span data-ttu-id="758c3-137">Gibt eine Schutzrichtlinie an, die dieses Cmdlet einem Element zurät.</span><span class="sxs-lookup"><span data-stu-id="758c3-137">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="758c3-138">Verwenden Sie das cmdlet Get-AzRecoveryServicesBackupProtectionPolicy, um ein **AzureRmRecoveryServicesBackupProtectionPolicy-Objekt** zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="758c3-138">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="758c3-139">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="758c3-139">-ProtectableItem</span></span>
<span data-ttu-id="758c3-140">Gibt das Element an, das mit der angegebenen Richtlinie geschützt werden soll.</span><span class="sxs-lookup"><span data-stu-id="758c3-140">Specifies the item to be protected with the given policy.</span></span>

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

### <span data-ttu-id="758c3-141">-ResetExclusionSettings</span><span class="sxs-lookup"><span data-stu-id="758c3-141">-ResetExclusionSettings</span></span>
<span data-ttu-id="758c3-142">Gibt an, dass die Einstellung für den Datenträgerausschluss zurückgesetzt werden soll, die dem Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="758c3-142">Specifies to reset disk exclusion setting associated with the item</span></span>

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

### <span data-ttu-id="758c3-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="758c3-143">-ResourceGroupName</span></span>
<span data-ttu-id="758c3-144">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="758c3-144">Specifies the name of the resource group.</span></span>
<span data-ttu-id="758c3-145">Geben Sie diesen Parameter nur für ARM virtuelle Computer an.</span><span class="sxs-lookup"><span data-stu-id="758c3-145">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="758c3-146">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="758c3-146">-StorageAccountName</span></span>
<span data-ttu-id="758c3-147">Azure File Share Storage Account Name</span><span class="sxs-lookup"><span data-stu-id="758c3-147">Azure file share storage account name</span></span>

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

### <span data-ttu-id="758c3-148">-VaultId</span><span class="sxs-lookup"><span data-stu-id="758c3-148">-VaultId</span></span>
<span data-ttu-id="758c3-149">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="758c3-149">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="758c3-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="758c3-150">-Confirm</span></span>
<span data-ttu-id="758c3-151">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="758c3-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="758c3-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="758c3-152">-WhatIf</span></span>
<span data-ttu-id="758c3-153">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="758c3-153">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="758c3-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="758c3-154">CommonParameters</span></span>
<span data-ttu-id="758c3-155">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="758c3-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="758c3-156">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="758c3-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="758c3-157">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="758c3-157">INPUTS</span></span>

### <span data-ttu-id="758c3-158">System.String</span><span class="sxs-lookup"><span data-stu-id="758c3-158">System.String</span></span>

### <span data-ttu-id="758c3-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="758c3-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="758c3-160">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="758c3-160">OUTPUTS</span></span>

### <span data-ttu-id="758c3-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="758c3-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="758c3-162">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="758c3-162">NOTES</span></span>

## <span data-ttu-id="758c3-163">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="758c3-163">RELATED LINKS</span></span>

[<span data-ttu-id="758c3-164">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="758c3-164">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="758c3-165">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="758c3-165">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


