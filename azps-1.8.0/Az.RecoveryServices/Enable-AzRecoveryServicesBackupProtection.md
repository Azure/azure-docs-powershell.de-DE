---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 7f29c0bef53d75be4f5b253e3a15bf78cbacd04b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659956"
---
# <span data-ttu-id="83cf7-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="83cf7-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="83cf7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="83cf7-102">SYNOPSIS</span></span>
<span data-ttu-id="83cf7-103">Aktiviert die Sicherung für ein Element mit einer angegebenen Sicherungsschutz Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="83cf7-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="83cf7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="83cf7-104">SYNTAX</span></span>

### <span data-ttu-id="83cf7-105">AzureVMComputeEnableProtection (Standard)</span><span class="sxs-lookup"><span data-stu-id="83cf7-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ResourceGroupName] <String>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83cf7-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="83cf7-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83cf7-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="83cf7-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83cf7-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="83cf7-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83cf7-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="83cf7-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83cf7-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83cf7-110">DESCRIPTION</span></span>
<span data-ttu-id="83cf7-111">Das Cmdlet **enable-AzRecoveryServicesBackupProtection** legt die Azure-Sicherungsschutz Richtlinie für ein Element fest.</span><span class="sxs-lookup"><span data-stu-id="83cf7-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>
<span data-ttu-id="83cf7-112">Setzen Sie den Vault-Kontext mithilfe des Set-AzRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="83cf7-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="83cf7-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="83cf7-113">EXAMPLES</span></span>

### <span data-ttu-id="83cf7-114">Beispiel 1: Aktivieren des Sicherungs Schutzes für ein Element</span><span class="sxs-lookup"><span data-stu-id="83cf7-114">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="83cf7-115">Das erste Cmdlet ruft ein Standardrichtlinienobjekt ab und speichert es dann in der $Pol-Variablen.</span><span class="sxs-lookup"><span data-stu-id="83cf7-115">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="83cf7-116">Das zweite Cmdlet legt die Sicherungsschutz Richtlinie für den virtuellen Arm-Computer mit dem Namen V2VM mithilfe der Richtlinie in $Pol fest.</span><span class="sxs-lookup"><span data-stu-id="83cf7-116">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="83cf7-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="83cf7-117">PARAMETERS</span></span>

### <span data-ttu-id="83cf7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83cf7-118">-DefaultProfile</span></span>
<span data-ttu-id="83cf7-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="83cf7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83cf7-120">-Item</span><span class="sxs-lookup"><span data-stu-id="83cf7-120">-Item</span></span>
<span data-ttu-id="83cf7-121">Gibt das Sicherungselement an, für das dieses Cmdlet den Schutz aktiviert.</span><span class="sxs-lookup"><span data-stu-id="83cf7-121">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="83cf7-122">Verwenden Sie zum Abrufen eines **AzureRmRecoveryServicesBackupItem** das Get-AzRecoveryServicesBackupItem-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83cf7-122">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="83cf7-123">-Name</span><span class="sxs-lookup"><span data-stu-id="83cf7-123">-Name</span></span>
<span data-ttu-id="83cf7-124">Gibt den Namen des sicherungselements an.</span><span class="sxs-lookup"><span data-stu-id="83cf7-124">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="83cf7-125">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="83cf7-125">-Policy</span></span>
<span data-ttu-id="83cf7-126">Gibt eine Schutzrichtlinie an, die mit diesem Cmdlet einem Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="83cf7-126">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="83cf7-127">Verwenden Sie das Get-AzRecoveryServicesBackupProtectionPolicy-Cmdlet, um ein **AzureRmRecoveryServicesBackupProtectionPolicy** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="83cf7-127">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83cf7-128">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="83cf7-128">-ProtectableItem</span></span>
<span data-ttu-id="83cf7-129">Filter Wert für den Status des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="83cf7-129">Filter value for status of job.</span></span>

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

### <span data-ttu-id="83cf7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83cf7-130">-ResourceGroupName</span></span>
<span data-ttu-id="83cf7-131">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="83cf7-131">Specifies the name of the resource group.</span></span>
<span data-ttu-id="83cf7-132">Geben Sie diesen Parameter nur für virtuelle Arm-Computer an.</span><span class="sxs-lookup"><span data-stu-id="83cf7-132">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="83cf7-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="83cf7-133">-ServiceName</span></span>
<span data-ttu-id="83cf7-134">Gibt den Namen des Diensts an.</span><span class="sxs-lookup"><span data-stu-id="83cf7-134">Specifies the service name.</span></span>
<span data-ttu-id="83cf7-135">Geben Sie diesen Parameter nur für ASM Virtual Machines an.</span><span class="sxs-lookup"><span data-stu-id="83cf7-135">Specify this parameter only for ASM virtual machines.</span></span>

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

### <span data-ttu-id="83cf7-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="83cf7-136">-StorageAccountName</span></span>
<span data-ttu-id="83cf7-137">Name des Azure File Share-speicherkontos</span><span class="sxs-lookup"><span data-stu-id="83cf7-137">Azure file share storage account name</span></span>

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

### <span data-ttu-id="83cf7-138">-Tresor</span><span class="sxs-lookup"><span data-stu-id="83cf7-138">-VaultId</span></span>
<span data-ttu-id="83cf7-139">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="83cf7-139">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="83cf7-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="83cf7-140">-Confirm</span></span>
<span data-ttu-id="83cf7-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="83cf7-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83cf7-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83cf7-142">-WhatIf</span></span>
<span data-ttu-id="83cf7-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="83cf7-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="83cf7-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="83cf7-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83cf7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83cf7-145">CommonParameters</span></span>
<span data-ttu-id="83cf7-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83cf7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83cf7-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83cf7-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83cf7-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="83cf7-148">INPUTS</span></span>

### <span data-ttu-id="83cf7-149">System. String</span><span class="sxs-lookup"><span data-stu-id="83cf7-149">System.String</span></span>

### <span data-ttu-id="83cf7-150">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="83cf7-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="83cf7-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="83cf7-151">OUTPUTS</span></span>

### <span data-ttu-id="83cf7-152">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="83cf7-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="83cf7-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="83cf7-153">NOTES</span></span>

## <span data-ttu-id="83cf7-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="83cf7-154">RELATED LINKS</span></span>

[<span data-ttu-id="83cf7-155">Deaktivieren-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="83cf7-155">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="83cf7-156">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="83cf7-156">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


