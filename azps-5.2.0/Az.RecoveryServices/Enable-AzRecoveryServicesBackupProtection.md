---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: f0147cea03d4b535102efd53af1a4d5f88338530
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301200"
---
# <span data-ttu-id="2f36a-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="2f36a-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="2f36a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f36a-102">SYNOPSIS</span></span>
<span data-ttu-id="2f36a-103">Aktiviert die Sicherung für ein Element mit einer angegebenen Sicherungsschutzrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="2f36a-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="2f36a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f36a-104">SYNTAX</span></span>

### <span data-ttu-id="2f36a-105">AzureVMComputeEnableProtection (Standard)</span><span class="sxs-lookup"><span data-stu-id="2f36a-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-ResourceGroupName] <String> [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f36a-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="2f36a-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String> [-ServiceName] <String>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ExcludeAllDataDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f36a-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="2f36a-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f36a-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="2f36a-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f36a-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="2f36a-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Item] <ItemBase>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ResetExclusionSettings]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f36a-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2f36a-110">DESCRIPTION</span></span>
<span data-ttu-id="2f36a-111">Das **Cmdlet "Enable-AzRecoveryServicesBackupProtection"** aktiviert die Sicherung durch Zuordnen einer Schutzrichtlinie zum Element.</span><span class="sxs-lookup"><span data-stu-id="2f36a-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet enables the backup by associating a protection policy with the item.</span></span>
<span data-ttu-id="2f36a-112">Legen Sie den Tresorkontext mithilfe des cmdlets Set-AzRecoveryServicesVaultContext, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="2f36a-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="2f36a-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2f36a-113">EXAMPLES</span></span>

### <span data-ttu-id="2f36a-114">Beispiel 1: Aktivieren des Sicherungsschutzes für ein Element</span><span class="sxs-lookup"><span data-stu-id="2f36a-114">Example 1: Enable Backup protection for an item</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $inclusionDiskLUNS = ("1", "2")
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1" -InclusionDisksList $inclusionDiskLUNS
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="2f36a-115">Das erste Cmdlet ruft ein Standardrichtlinienobjekt ab und speichert es dann in der $Pol Variable.</span><span class="sxs-lookup"><span data-stu-id="2f36a-115">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="2f36a-116">Das zweite Cmdlet gibt die zu sichernden Datenträger-LUNs an und speichert sie in $inclusionDiskLUNS Variable.</span><span class="sxs-lookup"><span data-stu-id="2f36a-116">The second cmdlet specifies the disk LUNs which are to be backed up and stores it in $inclusionDiskLUNS variable.</span></span>
<span data-ttu-id="2f36a-117">Das dritte Cmdlet legt die Sicherungsschutzrichtlinie für den ARM virtuellen Computer V2VM mithilfe der Richtlinie in $Pol.</span><span class="sxs-lookup"><span data-stu-id="2f36a-117">The third cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

### <span data-ttu-id="2f36a-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2f36a-118">Example 2</span></span>

<span data-ttu-id="2f36a-119">Aktiviert die Sicherung für ein Element mit einer angegebenen Sicherungsschutzrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="2f36a-119">Enables backup for an item with a specified Backup protection policy.</span></span> <span data-ttu-id="2f36a-120">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="2f36a-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupProtection -Item $Item -Policy $Pol -VaultId $vault
```

## <span data-ttu-id="2f36a-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f36a-121">PARAMETERS</span></span>

### <span data-ttu-id="2f36a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f36a-122">-DefaultProfile</span></span>
<span data-ttu-id="2f36a-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2f36a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f36a-124">-ExcludeAllDataDisks</span><span class="sxs-lookup"><span data-stu-id="2f36a-124">-ExcludeAllDataDisks</span></span>
<span data-ttu-id="2f36a-125">Option zum Angeben, dass nur Betriebssystemdatenträger gesichert werden</span><span class="sxs-lookup"><span data-stu-id="2f36a-125">Option to specify to backup OS disks only</span></span>

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

### <span data-ttu-id="2f36a-126">-ExclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="2f36a-126">-ExclusionDisksList</span></span>
<span data-ttu-id="2f36a-127">Liste der Disk-LUNs, die in die Sicherung ausgeschlossen werden sollen, und die restlichen werden automatisch einbezogen.</span><span class="sxs-lookup"><span data-stu-id="2f36a-127">List of Disk LUNs to be excluded in backup and the rest are automatically included.</span></span>

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

### <span data-ttu-id="2f36a-128">-InclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="2f36a-128">-InclusionDisksList</span></span>
<span data-ttu-id="2f36a-129">Liste der in die Sicherung eingeschlossenen Datenträger-LUNs, und die restlichen werden mit Ausnahme des Betriebssystemdatenträgers automatisch ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="2f36a-129">List of Disk LUNs to be included in backup and the rest are automatically excluded except OS disk.</span></span>

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

### <span data-ttu-id="2f36a-130">-Item</span><span class="sxs-lookup"><span data-stu-id="2f36a-130">-Item</span></span>
<span data-ttu-id="2f36a-131">Gibt das Sicherungselement an, für das dieses Cmdlet schutzfähig ist.</span><span class="sxs-lookup"><span data-stu-id="2f36a-131">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="2f36a-132">Verwenden Sie zum **Abrufen eines AzureRmRecoveryServicesBackupItem** das Get-AzRecoveryServicesBackupItem Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f36a-132">To obtain an **AzureRmRecoveryServicesBackupItem**, use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="2f36a-133">-Name</span><span class="sxs-lookup"><span data-stu-id="2f36a-133">-Name</span></span>
<span data-ttu-id="2f36a-134">Gibt den Namen des Sicherungselements an.</span><span class="sxs-lookup"><span data-stu-id="2f36a-134">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="2f36a-135">-Policy</span><span class="sxs-lookup"><span data-stu-id="2f36a-135">-Policy</span></span>
<span data-ttu-id="2f36a-136">Gibt die Schutzrichtlinie an, die dieses Cmdlet einem Element zu ordnet.</span><span class="sxs-lookup"><span data-stu-id="2f36a-136">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="2f36a-137">Verwenden Sie zum Abrufen **eines AzureRmRecoveryServicesBackupProtectionPolicy-Objekts** das Get-AzRecoveryServicesBackupProtectionPolicy Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f36a-137">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="2f36a-138">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="2f36a-138">-ProtectableItem</span></span>
<span data-ttu-id="2f36a-139">Gibt das Element an, das mit der angegebenen Richtlinie geschützt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2f36a-139">Specifies the item to be protected with the given policy.</span></span>

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

### <span data-ttu-id="2f36a-140">-ResetExclusionSettings</span><span class="sxs-lookup"><span data-stu-id="2f36a-140">-ResetExclusionSettings</span></span>
<span data-ttu-id="2f36a-141">Gibt an, dass die dem Element zugeordnete Datenträgerausschlusseinstellung zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="2f36a-141">Specifies to reset disk exclusion setting associated with the item</span></span>

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

### <span data-ttu-id="2f36a-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f36a-142">-ResourceGroupName</span></span>
<span data-ttu-id="2f36a-143">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2f36a-143">Specifies the name of the resource group.</span></span>
<span data-ttu-id="2f36a-144">Geben Sie diesen Parameter nur für ARM virtuelle Computer an.</span><span class="sxs-lookup"><span data-stu-id="2f36a-144">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="2f36a-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2f36a-145">-StorageAccountName</span></span>
<span data-ttu-id="2f36a-146">Name des Azure-Dateifreigabespeicherkontos</span><span class="sxs-lookup"><span data-stu-id="2f36a-146">Azure file share storage account name</span></span>

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

### <span data-ttu-id="2f36a-147">-VaultId</span><span class="sxs-lookup"><span data-stu-id="2f36a-147">-VaultId</span></span>
<span data-ttu-id="2f36a-148">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="2f36a-148">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="2f36a-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f36a-149">-Confirm</span></span>
<span data-ttu-id="2f36a-150">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2f36a-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f36a-151">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2f36a-151">-WhatIf</span></span>
<span data-ttu-id="2f36a-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2f36a-152">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="2f36a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f36a-153">CommonParameters</span></span>
<span data-ttu-id="2f36a-154">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f36a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f36a-155">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f36a-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f36a-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2f36a-156">INPUTS</span></span>

### <span data-ttu-id="2f36a-157">System.String</span><span class="sxs-lookup"><span data-stu-id="2f36a-157">System.String</span></span>

### <span data-ttu-id="2f36a-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="2f36a-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="2f36a-159">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2f36a-159">OUTPUTS</span></span>

### <span data-ttu-id="2f36a-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="2f36a-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="2f36a-161">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2f36a-161">NOTES</span></span>

## <span data-ttu-id="2f36a-162">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2f36a-162">RELATED LINKS</span></span>

[<span data-ttu-id="2f36a-163">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="2f36a-163">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="2f36a-164">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2f36a-164">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


