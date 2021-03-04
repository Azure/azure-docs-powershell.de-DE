---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/undo-azrecoveryservicesbackupitemdeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
ms.openlocfilehash: f7e82c2ccc939b0492575766c621a81ef9a25e9b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948496"
---
# <span data-ttu-id="6ce8e-101">Undo-AzRecoveryServicesBackupItemDeletion</span><span class="sxs-lookup"><span data-stu-id="6ce8e-101">Undo-AzRecoveryServicesBackupItemDeletion</span></span>

## <span data-ttu-id="6ce8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ce8e-102">SYNOPSIS</span></span>
<span data-ttu-id="6ce8e-103">Wenn ein Sicherungselement gelöscht und in einem Zustand mit einem "Soft-Deleted" vorhanden ist, wird das Element mit diesem Befehl wieder in einen Zustand zurückverteilt, in dem die Daten für immer aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="6ce8e-103">If a backup item is deleted and present in a soft-deleted state, this command brings the item back to a state where the data is retained forever</span></span> 

## <span data-ttu-id="6ce8e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ce8e-104">SYNTAX</span></span>

```
Undo-AzRecoveryServicesBackupItemDeletion [-Item] <ItemBase> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ce8e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ce8e-105">DESCRIPTION</span></span>
<span data-ttu-id="6ce8e-106">Das Undo-AzRecoveryServicesBackupItemDeletion-Cmdlet setzt ein weich gelöschtes Element in einen Zustand zurück, in dem der Schutz beendet, daten aber für immer aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="6ce8e-106">The Undo-AzRecoveryServicesBackupItemDeletion cmdlet reverts a soft-deleted item to a state where the protection is stopped but data is retained forever.</span></span>

## <span data-ttu-id="6ce8e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6ce8e-107">EXAMPLES</span></span>

### <span data-ttu-id="6ce8e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6ce8e-108">Example 1</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM | Where-Object {$_.DeleteState -eq "ToBeDeleted"}
PS C:\> Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0]
```

<span data-ttu-id="6ce8e-109">Der erste Befehl ruft ein Array von Sicherungscontainern ab und speichert es dann im $Cont Array.</span><span class="sxs-lookup"><span data-stu-id="6ce8e-109">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="6ce8e-110">Der zweite Befehl ruft das Sicherungselement ab, das dem ersten Containerelement entspricht, und speichert es dann in $PI Variablen.</span><span class="sxs-lookup"><span data-stu-id="6ce8e-110">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="6ce8e-111">Der dritte Befehl deaktiviert den Sicherungsschutz für das Element in $PI 0 und versetzt das Element \[ \] in einen Softdelet-Zustand.</span><span class="sxs-lookup"><span data-stu-id="6ce8e-111">The third command disables Backup protection for the item in $PI\[0\] and puts the item in a softdeleted state.</span></span>
<span data-ttu-id="6ce8e-112">Der vierte Befehl ruft das Element ab, das sich im Zustand "Softdeleted" befindet.</span><span class="sxs-lookup"><span data-stu-id="6ce8e-112">The fourth command gets the item which is in a softdeleted state.</span></span>
<span data-ttu-id="6ce8e-113">Der letzte Befehl bringt die softdeleted-VM in einen Zustand, in dem der Schutz beendet wird, die Daten jedoch für immer aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="6ce8e-113">The last command brings the softdeleted VM to a state where the protection is stopped but data is retained forever.</span></span>

### <span data-ttu-id="6ce8e-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6ce8e-114">Example 2</span></span>

<span data-ttu-id="6ce8e-115">Wiederherstellen der Hydratation eines weich gelöschten Elements</span><span class="sxs-lookup"><span data-stu-id="6ce8e-115">Rehydrates a soft-deleted Item.</span></span> <span data-ttu-id="6ce8e-116">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="6ce8e-116">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0] -VaultId $vault.ID
```

## <span data-ttu-id="6ce8e-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6ce8e-117">PARAMETERS</span></span>

### <span data-ttu-id="6ce8e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ce8e-118">-DefaultProfile</span></span>
<span data-ttu-id="6ce8e-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6ce8e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ce8e-120">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="6ce8e-120">-Force</span></span>
<span data-ttu-id="6ce8e-121">Durch Erzwingen wird der Sicherungsschutz deaktiviert (Bestätigungsdialogfeld wird verhindert).</span><span class="sxs-lookup"><span data-stu-id="6ce8e-121">Force disables backup protection (prevents confirmation dialog).</span></span>
<span data-ttu-id="6ce8e-122">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6ce8e-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="6ce8e-123">-Item</span><span class="sxs-lookup"><span data-stu-id="6ce8e-123">-Item</span></span>
<span data-ttu-id="6ce8e-124">Gibt das Sicherungselement an, für das dieses Cmdlet den Löschvorgang rückgängig macht.</span><span class="sxs-lookup"><span data-stu-id="6ce8e-124">Specifies the backup item for which this cmdlet reverts the deletion.</span></span>
<span data-ttu-id="6ce8e-125">Zum Abrufen eines AzureRmRecoveryServicesBackupItem verwenden Sie das Get-AzRecoveryServicesBackupItem Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ce8e-125">To obtain an AzureRmRecoveryServicesBackupItem , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce8e-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="6ce8e-126">-VaultId</span></span>
<span data-ttu-id="6ce8e-127">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="6ce8e-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="6ce8e-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6ce8e-128">-Confirm</span></span>
<span data-ttu-id="6ce8e-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6ce8e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ce8e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ce8e-130">-WhatIf</span></span>
<span data-ttu-id="6ce8e-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6ce8e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ce8e-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6ce8e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ce8e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ce8e-133">CommonParameters</span></span>
<span data-ttu-id="6ce8e-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ce8e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ce8e-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ce8e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ce8e-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6ce8e-136">INPUTS</span></span>

### <span data-ttu-id="6ce8e-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="6ce8e-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="6ce8e-138">System.String</span><span class="sxs-lookup"><span data-stu-id="6ce8e-138">System.String</span></span>

## <span data-ttu-id="6ce8e-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6ce8e-139">OUTPUTS</span></span>

### <span data-ttu-id="6ce8e-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="6ce8e-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="6ce8e-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6ce8e-141">NOTES</span></span>

## <span data-ttu-id="6ce8e-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6ce8e-142">RELATED LINKS</span></span>

[<span data-ttu-id="6ce8e-143">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="6ce8e-143">Get-AzRecoveryServicesBackupContainer</span></span>]()

[<span data-ttu-id="6ce8e-144">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="6ce8e-144">Get-AzRecoveryServicesBackupItem</span></span>]()

