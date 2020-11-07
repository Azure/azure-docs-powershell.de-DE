---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/enable-azurermrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: 357256d1c1a754915cbebc978e5c4ccf4440ccf4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664024"
---
# <span data-ttu-id="c0c8a-101">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="c0c8a-101">Enable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="c0c8a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c0c8a-102">SYNOPSIS</span></span>
<span data-ttu-id="c0c8a-103">Aktiviert die Sicherung für ein Element mit einer angegebenen Sicherungsschutz Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="c0c8a-103">Enables backup for an item with a specified Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0c8a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0c8a-104">SYNTAX</span></span>

### <span data-ttu-id="c0c8a-105">AzureVMComputeEnableProtection (Standard)</span><span class="sxs-lookup"><span data-stu-id="c0c8a-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-ResourceGroupName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0c8a-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="c0c8a-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0c8a-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="c0c8a-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 -StorageAccountName <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0c8a-108">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="c0c8a-108">ModifyProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0c8a-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c0c8a-109">DESCRIPTION</span></span>
<span data-ttu-id="c0c8a-110">Das Cmdlet **enable-AzureRmRecoveryServicesBackupProtection** legt die Azure-Sicherungsschutz Richtlinie für ein Element fest.</span><span class="sxs-lookup"><span data-stu-id="c0c8a-110">The **Enable-AzureRmRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>
<span data-ttu-id="c0c8a-111">Setzen Sie den Vault-Kontext mithilfe des Set-AzureRmRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="c0c8a-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="c0c8a-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c0c8a-112">EXAMPLES</span></span>

### <span data-ttu-id="c0c8a-113">Beispiel 1: Aktivieren des Sicherungs Schutzes für ein Element</span><span class="sxs-lookup"><span data-stu-id="c0c8a-113">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzureRmRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="c0c8a-114">Das erste Cmdlet ruft ein Standardrichtlinienobjekt ab und speichert es dann in der $Pol-Variablen.</span><span class="sxs-lookup"><span data-stu-id="c0c8a-114">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="c0c8a-115">Das zweite Cmdlet legt die Sicherungsschutz Richtlinie für den virtuellen Arm-Computer mit dem Namen V2VM mithilfe der Richtlinie in $Pol fest.</span><span class="sxs-lookup"><span data-stu-id="c0c8a-115">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="c0c8a-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0c8a-116">PARAMETERS</span></span>

### <span data-ttu-id="c0c8a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0c8a-117">-DefaultProfile</span></span>
<span data-ttu-id="c0c8a-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c0c8a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0c8a-119">-Item</span><span class="sxs-lookup"><span data-stu-id="c0c8a-119">-Item</span></span>
<span data-ttu-id="c0c8a-120">Gibt das Sicherungselement an, für das dieses Cmdlet den Schutz aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c0c8a-120">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="c0c8a-121">Verwenden Sie zum Abrufen eines **AzureRmRecoveryServicesBackupItem** das Get-AzureRmRecoveryServicesBackupItem-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0c8a-121">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="c0c8a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c0c8a-122">-Name</span></span>
<span data-ttu-id="c0c8a-123">Gibt den Namen des sicherungselements an.</span><span class="sxs-lookup"><span data-stu-id="c0c8a-123">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="c0c8a-124">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="c0c8a-124">-Policy</span></span>
<span data-ttu-id="c0c8a-125">Gibt eine Schutzrichtlinie an, die mit diesem Cmdlet einem Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c0c8a-125">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="c0c8a-126">Verwenden Sie das Get-AzureRmRecoveryServicesBackupProtectionPolicy-Cmdlet, um ein **AzureRmRecoveryServicesBackupProtectionPolicy** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c0c8a-126">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="c0c8a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0c8a-127">-ResourceGroupName</span></span>
<span data-ttu-id="c0c8a-128">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c0c8a-128">Specifies the name of the resource group.</span></span>
<span data-ttu-id="c0c8a-129">Geben Sie diesen Parameter nur für virtuelle Arm-Computer an.</span><span class="sxs-lookup"><span data-stu-id="c0c8a-129">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="c0c8a-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c0c8a-130">-ServiceName</span></span>
<span data-ttu-id="c0c8a-131">Gibt den Namen des Diensts an.</span><span class="sxs-lookup"><span data-stu-id="c0c8a-131">Specifies the service name.</span></span>
<span data-ttu-id="c0c8a-132">Geben Sie diesen Parameter nur für ASM Virtual Machines an.</span><span class="sxs-lookup"><span data-stu-id="c0c8a-132">Specify this parameter only for ASM virtual machines.</span></span>

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

### <span data-ttu-id="c0c8a-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c0c8a-133">-StorageAccountName</span></span>
<span data-ttu-id="c0c8a-134">Name des Azure File Share-speicherkontos</span><span class="sxs-lookup"><span data-stu-id="c0c8a-134">Azure file share storage account name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileShareEnableProtection
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0c8a-135">-Tresor</span><span class="sxs-lookup"><span data-stu-id="c0c8a-135">-VaultId</span></span>
<span data-ttu-id="c0c8a-136">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="c0c8a-136">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="c0c8a-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c0c8a-137">-Confirm</span></span>
<span data-ttu-id="c0c8a-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c0c8a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0c8a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0c8a-139">-WhatIf</span></span>
<span data-ttu-id="c0c8a-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c0c8a-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0c8a-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0c8a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0c8a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0c8a-142">CommonParameters</span></span>
<span data-ttu-id="c0c8a-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0c8a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0c8a-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0c8a-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0c8a-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c0c8a-145">INPUTS</span></span>

### <span data-ttu-id="c0c8a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="c0c8a-146">System.String</span></span>
<span data-ttu-id="c0c8a-147">Parameter: Vault-ByValue</span><span class="sxs-lookup"><span data-stu-id="c0c8a-147">Parameters: VaultId (ByValue)</span></span>

### <span data-ttu-id="c0c8a-148">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="c0c8a-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="c0c8a-149">Parameter: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c0c8a-149">Parameters: Item (ByValue)</span></span>

## <span data-ttu-id="c0c8a-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c0c8a-150">OUTPUTS</span></span>

### <span data-ttu-id="c0c8a-151">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="c0c8a-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="c0c8a-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="c0c8a-152">NOTES</span></span>

## <span data-ttu-id="c0c8a-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c0c8a-153">RELATED LINKS</span></span>

[<span data-ttu-id="c0c8a-154">Deaktivieren-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="c0c8a-154">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="c0c8a-155">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c0c8a-155">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)


