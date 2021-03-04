---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 4723fd3087b2f547659e72c1af6b0f5cb7764cf5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919176"
---
# <span data-ttu-id="a71bb-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a71bb-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="a71bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a71bb-102">SYNOPSIS</span></span>
<span data-ttu-id="a71bb-103">Löscht eine Sicherungsschutzrichtlinie aus einem Tresor.</span><span class="sxs-lookup"><span data-stu-id="a71bb-103">Deletes a Backup protection policy from a vault.</span></span>

## <span data-ttu-id="a71bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a71bb-104">SYNTAX</span></span>

### <span data-ttu-id="a71bb-105">PolicyName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a71bb-105">PolicyName (Default)</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a71bb-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="a71bb-106">PolicyObject</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a71bb-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a71bb-107">DESCRIPTION</span></span>
<span data-ttu-id="a71bb-108">Das **Cmdlet Remove-AzRecoveryServicesBackupProtectionPolicy** löscht Sicherungsrichtlinien für einen Tresor.</span><span class="sxs-lookup"><span data-stu-id="a71bb-108">The **Remove-AzRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>
<span data-ttu-id="a71bb-109">Bevor Sie eine Sicherungsschutzrichtlinie löschen können, darf die Richtlinie keine zugeordneten Sicherungselemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="a71bb-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="a71bb-110">Stellen Sie vor dem Löschen der Richtlinie sicher, dass jedes zugeordnete Element einer anderen Richtlinie zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a71bb-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="a71bb-111">Wenn Sie einem Sicherungselement eine andere Richtlinie zuordnen möchten, verwenden Sie das Enable-AzRecoveryServicesBackupProtection Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a71bb-111">To associate another policy with a Backup item, use the Enable-AzRecoveryServicesBackupProtection cmdlet.</span></span>
<span data-ttu-id="a71bb-112">Legen Sie den Tresorkontext mithilfe des cmdlets Set-AzRecoveryServicesVaultContext, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="a71bb-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="a71bb-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a71bb-113">EXAMPLES</span></span>

### <span data-ttu-id="a71bb-114">Beispiel 1: Entfernen einer Richtlinie</span><span class="sxs-lookup"><span data-stu-id="a71bb-114">Example 1: Remove a policy</span></span>
```powershell
PS C:\>$Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="a71bb-115">Der erste Befehl ruft die Sicherungsschutzrichtlinie mit dem Namen NewPolicy ab und speichert sie dann in der $Pol-Variable.</span><span class="sxs-lookup"><span data-stu-id="a71bb-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="a71bb-116">Der zweite Befehl entfernt das Richtlinienobjekt in $Pol.</span><span class="sxs-lookup"><span data-stu-id="a71bb-116">The second command removes the policy object in $Pol.</span></span>

### <span data-ttu-id="a71bb-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a71bb-117">Example 2</span></span>

<span data-ttu-id="a71bb-118">Löscht eine Sicherungsschutzrichtlinie aus einem Tresor.</span><span class="sxs-lookup"><span data-stu-id="a71bb-118">Deletes a Backup protection policy from a vault.</span></span> <span data-ttu-id="a71bb-119">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="a71bb-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Remove-AzRecoveryServicesBackupProtectionPolicy -Name 'V2VM' -VaultId $vault.ID
```

## <span data-ttu-id="a71bb-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a71bb-120">PARAMETERS</span></span>

### <span data-ttu-id="a71bb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a71bb-121">-DefaultProfile</span></span>
<span data-ttu-id="a71bb-122">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a71bb-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a71bb-123">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="a71bb-123">-Force</span></span>
<span data-ttu-id="a71bb-124">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="a71bb-124">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a71bb-125">-Name</span><span class="sxs-lookup"><span data-stu-id="a71bb-125">-Name</span></span>
<span data-ttu-id="a71bb-126">Gibt den Namen der Sicherungsschutzrichtlinie an, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a71bb-126">Specifies the name of the Backup protection policy to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a71bb-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a71bb-127">-PassThru</span></span>
<span data-ttu-id="a71bb-128">Geben Sie die zu löschende Richtlinie zurück.</span><span class="sxs-lookup"><span data-stu-id="a71bb-128">Return the policy to be deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a71bb-129">-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="a71bb-129">-Policy</span></span>
<span data-ttu-id="a71bb-130">Gibt die Sicherungsschutzrichtlinie an, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a71bb-130">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="a71bb-131">Um ein **BackupPolicy-Objekt zu** erhalten, verwenden Sie das Get-AzRecoveryServicesBackupProtectionPolicy Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a71bb-131">To obtain an **BackupPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: PolicyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a71bb-132">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a71bb-132">-VaultId</span></span>
<span data-ttu-id="a71bb-133">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="a71bb-133">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a71bb-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a71bb-134">-Confirm</span></span>
<span data-ttu-id="a71bb-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a71bb-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a71bb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a71bb-136">-WhatIf</span></span>
<span data-ttu-id="a71bb-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a71bb-137">Shows what would happen if the cmdlet runs.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a71bb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a71bb-138">CommonParameters</span></span>
<span data-ttu-id="a71bb-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a71bb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a71bb-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a71bb-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a71bb-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a71bb-141">INPUTS</span></span>

### <span data-ttu-id="a71bb-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="a71bb-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="a71bb-143">System.String</span><span class="sxs-lookup"><span data-stu-id="a71bb-143">System.String</span></span>

## <span data-ttu-id="a71bb-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a71bb-144">OUTPUTS</span></span>

### <span data-ttu-id="a71bb-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="a71bb-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="a71bb-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a71bb-146">NOTES</span></span>

## <span data-ttu-id="a71bb-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a71bb-147">RELATED LINKS</span></span>

[<span data-ttu-id="a71bb-148">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a71bb-148">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="a71bb-149">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a71bb-149">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="a71bb-150">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a71bb-150">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


