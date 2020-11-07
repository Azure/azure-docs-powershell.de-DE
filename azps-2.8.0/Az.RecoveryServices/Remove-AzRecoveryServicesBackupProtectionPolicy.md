---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: b900e9b137c8268969ef1eb715f0b79356abc720
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825247"
---
# <span data-ttu-id="fcda0-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="fcda0-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="fcda0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fcda0-102">SYNOPSIS</span></span>
<span data-ttu-id="fcda0-103">Löscht eine Sicherungsschutz Richtlinie aus einem Tresor.</span><span class="sxs-lookup"><span data-stu-id="fcda0-103">Deletes a Backup protection policy from a vault.</span></span>

## <span data-ttu-id="fcda0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fcda0-104">SYNTAX</span></span>

### <span data-ttu-id="fcda0-105">Richtlinienwert (Standard)</span><span class="sxs-lookup"><span data-stu-id="fcda0-105">PolicyName (Default)</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcda0-106">Richtlinienobject</span><span class="sxs-lookup"><span data-stu-id="fcda0-106">PolicyObject</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcda0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fcda0-107">DESCRIPTION</span></span>
<span data-ttu-id="fcda0-108">Das Cmdlet **Remove-AzRecoveryServicesBackupProtectionPolicy** löscht Sicherungsrichtlinien für einen Tresor.</span><span class="sxs-lookup"><span data-stu-id="fcda0-108">The **Remove-AzRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>
<span data-ttu-id="fcda0-109">Bevor Sie eine Sicherungsschutz Richtlinie löschen können, darf die Richtlinie keine zugeordneten Sicherungselemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="fcda0-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="fcda0-110">Bevor Sie die Richtlinie löschen, stellen Sie sicher, dass jedes zugeordnete Element einer anderen Richtlinie zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fcda0-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="fcda0-111">Verwenden Sie das Enable-AzRecoveryServicesBackupProtection-Cmdlet, um eine andere Richtlinie einem Sicherungselement zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="fcda0-111">To associate another policy with a Backup item, use the Enable-AzRecoveryServicesBackupProtection cmdlet.</span></span>
<span data-ttu-id="fcda0-112">Setzen Sie den Vault-Kontext mithilfe des Set-AzRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="fcda0-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="fcda0-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fcda0-113">EXAMPLES</span></span>

### <span data-ttu-id="fcda0-114">Beispiel 1: Entfernen einer Richtlinie</span><span class="sxs-lookup"><span data-stu-id="fcda0-114">Example 1: Remove a policy</span></span>
```
PS C:\>$Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="fcda0-115">Der erste Befehl ruft die Sicherungsschutz Richtlinie mit dem Namen "Richtlinie" ab und speichert Sie dann in der $Pol-Variablen.</span><span class="sxs-lookup"><span data-stu-id="fcda0-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="fcda0-116">Der zweite Befehl entfernt das Richtlinienobjekt in $Pol.</span><span class="sxs-lookup"><span data-stu-id="fcda0-116">The second command removes the policy object in $Pol.</span></span>

## <span data-ttu-id="fcda0-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="fcda0-117">PARAMETERS</span></span>

### <span data-ttu-id="fcda0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcda0-118">-DefaultProfile</span></span>
<span data-ttu-id="fcda0-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fcda0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcda0-120">-Force</span><span class="sxs-lookup"><span data-stu-id="fcda0-120">-Force</span></span>
<span data-ttu-id="fcda0-121">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="fcda0-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fcda0-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fcda0-122">-Name</span></span>
<span data-ttu-id="fcda0-123">Gibt den Namen der zu entfernenden Sicherungsschutz Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="fcda0-123">Specifies the name of the Backup protection policy to remove.</span></span>

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

### <span data-ttu-id="fcda0-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fcda0-124">-PassThru</span></span>
<span data-ttu-id="fcda0-125">Gibt die zu löschende Richtlinie zurück.</span><span class="sxs-lookup"><span data-stu-id="fcda0-125">Return the policy to be deleted.</span></span>

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

### <span data-ttu-id="fcda0-126">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="fcda0-126">-Policy</span></span>
<span data-ttu-id="fcda0-127">Gibt die zu entfernende Sicherungsschutz Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="fcda0-127">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="fcda0-128">Verwenden Sie das Get-AzRecoveryServicesBackupProtectionPolicy-Cmdlet, um ein **BackupPolicy** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fcda0-128">To obtain an **BackupPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="fcda0-129">-Tresor</span><span class="sxs-lookup"><span data-stu-id="fcda0-129">-VaultId</span></span>
<span data-ttu-id="fcda0-130">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="fcda0-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="fcda0-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fcda0-131">-Confirm</span></span>
<span data-ttu-id="fcda0-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fcda0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcda0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcda0-133">-WhatIf</span></span>
<span data-ttu-id="fcda0-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fcda0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcda0-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fcda0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcda0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcda0-136">CommonParameters</span></span>
<span data-ttu-id="fcda0-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcda0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcda0-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcda0-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcda0-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fcda0-139">INPUTS</span></span>

### <span data-ttu-id="fcda0-140">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="fcda0-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="fcda0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="fcda0-141">System.String</span></span>

## <span data-ttu-id="fcda0-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fcda0-142">OUTPUTS</span></span>

### <span data-ttu-id="fcda0-143">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="fcda0-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="fcda0-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="fcda0-144">NOTES</span></span>

## <span data-ttu-id="fcda0-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fcda0-145">RELATED LINKS</span></span>

[<span data-ttu-id="fcda0-146">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="fcda0-146">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="fcda0-147">Neu – AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="fcda0-147">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="fcda0-148">Satz-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="fcda0-148">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


