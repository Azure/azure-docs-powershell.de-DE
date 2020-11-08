---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: f0147cea03d4b535102efd53af1a4d5f88338530
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007910"
---
# <span data-ttu-id="8ae49-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="8ae49-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="8ae49-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8ae49-102">SYNOPSIS</span></span>
<span data-ttu-id="8ae49-103">Aktiviert die Sicherung für ein Element mit einer angegebenen Sicherungsschutz Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="8ae49-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="8ae49-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ae49-104">SYNTAX</span></span>

### <span data-ttu-id="8ae49-105">AzureVMComputeEnableProtection (Standard)</span><span class="sxs-lookup"><span data-stu-id="8ae49-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-ResourceGroupName] <String> [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ae49-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="8ae49-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String> [-ServiceName] <String>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ExcludeAllDataDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ae49-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="8ae49-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ae49-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="8ae49-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ae49-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="8ae49-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Item] <ItemBase>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ResetExclusionSettings]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ae49-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ae49-110">DESCRIPTION</span></span>
<span data-ttu-id="8ae49-111">Mit dem Cmdlet **enable-AzRecoveryServicesBackupProtection** können Sie die Sicherung durch Zuordnen einer Schutzrichtlinie zum Element aktivieren.</span><span class="sxs-lookup"><span data-stu-id="8ae49-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet enables the backup by associating a protection policy with the item.</span></span>
<span data-ttu-id="8ae49-112">Setzen Sie den Vault-Kontext mithilfe des Set-AzRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="8ae49-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="8ae49-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8ae49-113">EXAMPLES</span></span>

### <span data-ttu-id="8ae49-114">Beispiel 1: Aktivieren des Sicherungs Schutzes für ein Element</span><span class="sxs-lookup"><span data-stu-id="8ae49-114">Example 1: Enable Backup protection for an item</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $inclusionDiskLUNS = ("1", "2")
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1" -InclusionDisksList $inclusionDiskLUNS
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="8ae49-115">Das erste Cmdlet ruft ein Standardrichtlinienobjekt ab und speichert es dann in der $Pol-Variablen.</span><span class="sxs-lookup"><span data-stu-id="8ae49-115">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="8ae49-116">Das zweite Cmdlet gibt die zu sichernden Datenträger-LUNs an und speichert Sie in $inclusionDiskLUNS Variablen.</span><span class="sxs-lookup"><span data-stu-id="8ae49-116">The second cmdlet specifies the disk LUNs which are to be backed up and stores it in $inclusionDiskLUNS variable.</span></span>
<span data-ttu-id="8ae49-117">Das dritte Cmdlet legt die Sicherungsschutz Richtlinie für den virtuellen Arm-Computer mit dem Namen V2VM mithilfe der Richtlinie in $Pol fest.</span><span class="sxs-lookup"><span data-stu-id="8ae49-117">The third cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

### <span data-ttu-id="8ae49-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8ae49-118">Example 2</span></span>

<span data-ttu-id="8ae49-119">Aktiviert die Sicherung für ein Element mit einer angegebenen Sicherungsschutz Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="8ae49-119">Enables backup for an item with a specified Backup protection policy.</span></span> <span data-ttu-id="8ae49-120">automatisch</span><span class="sxs-lookup"><span data-stu-id="8ae49-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupProtection -Item $Item -Policy $Pol -VaultId $vault
```

## <span data-ttu-id="8ae49-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ae49-121">PARAMETERS</span></span>

### <span data-ttu-id="8ae49-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ae49-122">-DefaultProfile</span></span>
<span data-ttu-id="8ae49-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8ae49-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ae49-124">-ExcludeAllDataDisks</span><span class="sxs-lookup"><span data-stu-id="8ae49-124">-ExcludeAllDataDisks</span></span>
<span data-ttu-id="8ae49-125">Option zum angeben nur für Backup-Betriebssystemdatenträger</span><span class="sxs-lookup"><span data-stu-id="8ae49-125">Option to specify to backup OS disks only</span></span>

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

### <span data-ttu-id="8ae49-126">-ExclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="8ae49-126">-ExclusionDisksList</span></span>
<span data-ttu-id="8ae49-127">Liste der Datenträger-LUNs, die in einer Sicherung ausgeschlossen werden sollen, und die restlichen werden automatisch eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="8ae49-127">List of Disk LUNs to be excluded in backup and the rest are automatically included.</span></span>

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

### <span data-ttu-id="8ae49-128">-InclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="8ae49-128">-InclusionDisksList</span></span>
<span data-ttu-id="8ae49-129">Liste der Datenträger-LUNs, die in die Sicherung eingeschlossen werden sollen, und die restlichen werden automatisch ausgeschlossen, außer der Betriebssystem Diskette.</span><span class="sxs-lookup"><span data-stu-id="8ae49-129">List of Disk LUNs to be included in backup and the rest are automatically excluded except OS disk.</span></span>

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

### <span data-ttu-id="8ae49-130">-Item</span><span class="sxs-lookup"><span data-stu-id="8ae49-130">-Item</span></span>
<span data-ttu-id="8ae49-131">Gibt das Sicherungselement an, für das dieses Cmdlet den Schutz aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8ae49-131">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="8ae49-132">Verwenden Sie zum Abrufen eines **AzureRmRecoveryServicesBackupItem** das Get-AzRecoveryServicesBackupItem-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ae49-132">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="8ae49-133">-Name</span><span class="sxs-lookup"><span data-stu-id="8ae49-133">-Name</span></span>
<span data-ttu-id="8ae49-134">Gibt den Namen des sicherungselements an.</span><span class="sxs-lookup"><span data-stu-id="8ae49-134">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="8ae49-135">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="8ae49-135">-Policy</span></span>
<span data-ttu-id="8ae49-136">Gibt eine Schutzrichtlinie an, die mit diesem Cmdlet einem Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8ae49-136">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="8ae49-137">Verwenden Sie das Get-AzRecoveryServicesBackupProtectionPolicy-Cmdlet, um ein **AzureRmRecoveryServicesBackupProtectionPolicy** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8ae49-137">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="8ae49-138">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="8ae49-138">-ProtectableItem</span></span>
<span data-ttu-id="8ae49-139">Gibt das Element an, das mit der angegebenen Richtlinie geschützt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8ae49-139">Specifies the item to be protected with the given policy.</span></span>

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

### <span data-ttu-id="8ae49-140">-ResetExclusionSettings</span><span class="sxs-lookup"><span data-stu-id="8ae49-140">-ResetExclusionSettings</span></span>
<span data-ttu-id="8ae49-141">Gibt an, dass die dem Element zugeordnete Datenträger Ausschluss Einstellung zurückgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8ae49-141">Specifies to reset disk exclusion setting associated with the item</span></span>

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

### <span data-ttu-id="8ae49-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ae49-142">-ResourceGroupName</span></span>
<span data-ttu-id="8ae49-143">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="8ae49-143">Specifies the name of the resource group.</span></span>
<span data-ttu-id="8ae49-144">Geben Sie diesen Parameter nur für virtuelle Arm-Computer an.</span><span class="sxs-lookup"><span data-stu-id="8ae49-144">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="8ae49-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8ae49-145">-StorageAccountName</span></span>
<span data-ttu-id="8ae49-146">Name des Azure File Share-speicherkontos</span><span class="sxs-lookup"><span data-stu-id="8ae49-146">Azure file share storage account name</span></span>

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

### <span data-ttu-id="8ae49-147">-Tresor</span><span class="sxs-lookup"><span data-stu-id="8ae49-147">-VaultId</span></span>
<span data-ttu-id="8ae49-148">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="8ae49-148">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8ae49-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8ae49-149">-Confirm</span></span>
<span data-ttu-id="8ae49-150">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8ae49-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ae49-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ae49-151">-WhatIf</span></span>
<span data-ttu-id="8ae49-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8ae49-152">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="8ae49-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ae49-153">CommonParameters</span></span>
<span data-ttu-id="8ae49-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ae49-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ae49-155">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ae49-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ae49-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8ae49-156">INPUTS</span></span>

### <span data-ttu-id="8ae49-157">System. String</span><span class="sxs-lookup"><span data-stu-id="8ae49-157">System.String</span></span>

### <span data-ttu-id="8ae49-158">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="8ae49-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="8ae49-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8ae49-159">OUTPUTS</span></span>

### <span data-ttu-id="8ae49-160">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="8ae49-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="8ae49-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="8ae49-161">NOTES</span></span>

## <span data-ttu-id="8ae49-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8ae49-162">RELATED LINKS</span></span>

[<span data-ttu-id="8ae49-163">Deaktivieren-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="8ae49-163">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="8ae49-164">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8ae49-164">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


