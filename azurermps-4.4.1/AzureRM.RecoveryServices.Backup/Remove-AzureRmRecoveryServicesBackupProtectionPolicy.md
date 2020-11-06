---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 22dcc7459c0e574e62f3c87745ad6283fd919386
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481710"
---
# <span data-ttu-id="02c2d-101">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="02c2d-101">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="02c2d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="02c2d-102">SYNOPSIS</span></span>
<span data-ttu-id="02c2d-103">Löscht eine Sicherungsschutz Richtlinie aus einem Tresor.</span><span class="sxs-lookup"><span data-stu-id="02c2d-103">Deletes a Backup protection policy from a vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02c2d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="02c2d-104">SYNTAX</span></span>

### <span data-ttu-id="02c2d-105">Richtlinienwert (Standard)</span><span class="sxs-lookup"><span data-stu-id="02c2d-105">PolicyName (Default)</span></span>
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02c2d-106">Richtlinienobject</span><span class="sxs-lookup"><span data-stu-id="02c2d-106">PolicyObject</span></span>
```
Remove-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02c2d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="02c2d-107">DESCRIPTION</span></span>
<span data-ttu-id="02c2d-108">Das Cmdlet **Remove-AzureRmRecoveryServicesBackupProtectionPolicy** löscht Sicherungsrichtlinien für einen Tresor.</span><span class="sxs-lookup"><span data-stu-id="02c2d-108">The **Remove-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>

<span data-ttu-id="02c2d-109">Bevor Sie eine Sicherungsschutz Richtlinie löschen können, darf die Richtlinie keine zugeordneten Sicherungselemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="02c2d-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="02c2d-110">Bevor Sie die Richtlinie löschen, stellen Sie sicher, dass jedes zugeordnete Element einer anderen Richtlinie zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="02c2d-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="02c2d-111">Verwenden Sie das Enable-AzureRmRecoveryServicesBackupProtection-Cmdlet, um eine andere Richtlinie einem Sicherungselement zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="02c2d-111">To associate another policy with a Backup item, use the Enable-AzureRmRecoveryServicesBackupProtection cmdlet.</span></span>

<span data-ttu-id="02c2d-112">Setzen Sie den Vault-Kontext mithilfe des Set-AzureRmRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="02c2d-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="02c2d-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="02c2d-113">EXAMPLES</span></span>

### <span data-ttu-id="02c2d-114">Beispiel 1: Entfernen einer Richtlinie</span><span class="sxs-lookup"><span data-stu-id="02c2d-114">Example 1: Remove a policy</span></span>
```
PS C:\>$Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="02c2d-115">Der erste Befehl ruft die Sicherungsschutz Richtlinie mit dem Namen "Richtlinie" ab und speichert Sie dann in der $Pol-Variablen.</span><span class="sxs-lookup"><span data-stu-id="02c2d-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>

<span data-ttu-id="02c2d-116">Der zweite Befehl entfernt das Richtlinienobjekt in $Pol.</span><span class="sxs-lookup"><span data-stu-id="02c2d-116">The second command removes the policy object in $Pol.</span></span>

## <span data-ttu-id="02c2d-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="02c2d-117">PARAMETERS</span></span>

### <span data-ttu-id="02c2d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="02c2d-118">-Force</span></span>
<span data-ttu-id="02c2d-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="02c2d-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="02c2d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="02c2d-120">-Name</span></span>
<span data-ttu-id="02c2d-121">Gibt den Namen der zu entfernenden Sicherungsschutz Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="02c2d-121">Specifies the name of the Backup protection policy to remove.</span></span>

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

### <span data-ttu-id="02c2d-122">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="02c2d-122">-Policy</span></span>
<span data-ttu-id="02c2d-123">Gibt die zu entfernende Sicherungsschutz Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="02c2d-123">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="02c2d-124">Verwenden Sie das Get-AzureRmRecoveryServicesBackupProtectionPolicy-Cmdlet, um ein **BackupPolicy** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="02c2d-124">To obtain an **BackupPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="02c2d-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="02c2d-125">-Confirm</span></span>
<span data-ttu-id="02c2d-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="02c2d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02c2d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02c2d-127">-WhatIf</span></span>
<span data-ttu-id="02c2d-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="02c2d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02c2d-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="02c2d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02c2d-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02c2d-130">-DefaultProfile</span></span>
<span data-ttu-id="02c2d-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="02c2d-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02c2d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02c2d-132">CommonParameters</span></span>
<span data-ttu-id="02c2d-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02c2d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02c2d-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02c2d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02c2d-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="02c2d-135">INPUTS</span></span>

### <span data-ttu-id="02c2d-136">PolicyBase</span><span class="sxs-lookup"><span data-stu-id="02c2d-136">PolicyBase</span></span>
<span data-ttu-id="02c2d-137">Der Parameter "Richtlinie" akzeptiert den Wert vom Typ "PolicyBase" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="02c2d-137">Parameter 'Policy' accepts value of type 'PolicyBase' from the pipeline</span></span>

## <span data-ttu-id="02c2d-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="02c2d-138">OUTPUTS</span></span>

## <span data-ttu-id="02c2d-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="02c2d-139">NOTES</span></span>

## <span data-ttu-id="02c2d-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="02c2d-140">RELATED LINKS</span></span>

[<span data-ttu-id="02c2d-141">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="02c2d-141">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="02c2d-142">Neu – AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="02c2d-142">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="02c2d-143">Satz-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="02c2d-143">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


