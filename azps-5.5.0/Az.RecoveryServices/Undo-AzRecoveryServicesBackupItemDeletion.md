---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/undo-azrecoveryservicesbackupitemdeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
ms.openlocfilehash: 62d8dc302dc5819272034cfdd1c3fd0c0c79f54c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153817"
---
# <span data-ttu-id="2ff49-101">Undo-AzRecoveryServicesBackupItemDeletion</span><span class="sxs-lookup"><span data-stu-id="2ff49-101">Undo-AzRecoveryServicesBackupItemDeletion</span></span>

## <span data-ttu-id="2ff49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ff49-102">SYNOPSIS</span></span>
<span data-ttu-id="2ff49-103">Wenn ein Sicherungselement gelöscht wird und sich in einem Status "Soft-Deleted" befindet, bringt dieser Befehl das Element wieder in einen Zustand zurück, in dem die Daten für immer aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="2ff49-103">If a backup item is deleted and present in a soft-deleted state, this command brings the item back to a state where the data is retained forever</span></span> 

## <span data-ttu-id="2ff49-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ff49-104">SYNTAX</span></span>

```
Undo-AzRecoveryServicesBackupItemDeletion [-Item] <ItemBase> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ff49-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2ff49-105">DESCRIPTION</span></span>
<span data-ttu-id="2ff49-106">Das Undo-AzRecoveryServicesBackupItemDeletion-Cmdlet setzt ein soft-deleted-Element in einen Zustand zurück, in dem der Schutz beendet wird, die Daten aber für immer erhalten bleiben.</span><span class="sxs-lookup"><span data-stu-id="2ff49-106">The Undo-AzRecoveryServicesBackupItemDeletion cmdlet reverts a soft-deleted item to a state where the protection is stopped but data is retained forever.</span></span>

## <span data-ttu-id="2ff49-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2ff49-107">EXAMPLES</span></span>

### <span data-ttu-id="2ff49-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2ff49-108">Example 1</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM | Where-Object {$_.DeleteState -eq "ToBeDeleted"}
PS C:\> Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0]
```

<span data-ttu-id="2ff49-109">Der erste Befehl ruft ein Array mit Sicherungscontainern ab und speichert es dann im $Cont Array.</span><span class="sxs-lookup"><span data-stu-id="2ff49-109">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="2ff49-110">Der zweite Befehl ruft das Sicherungselement ab, das dem ersten Containerelement entspricht, und speichert es dann in $PI Variable.</span><span class="sxs-lookup"><span data-stu-id="2ff49-110">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="2ff49-111">Der dritte Befehl deaktiviert den Sicherungsschutz für das Element in $PI 0 und versetzt das Element in einen \[ \] Softdeleted-Zustand.</span><span class="sxs-lookup"><span data-stu-id="2ff49-111">The third command disables Backup protection for the item in $PI\[0\] and puts the item in a softdeleted state.</span></span>
<span data-ttu-id="2ff49-112">Der vierte Befehl ruft das Element ab, das sich in einem Softdeletedzustand befindet.</span><span class="sxs-lookup"><span data-stu-id="2ff49-112">The fourth command gets the item which is in a softdeleted state.</span></span>
<span data-ttu-id="2ff49-113">Der letzte Befehl bringt die softdeleted VM in einen Zustand, in dem der Schutz gestoppt wird, die Daten jedoch für immer erhalten bleiben.</span><span class="sxs-lookup"><span data-stu-id="2ff49-113">The last command brings the softdeleted VM to a state where the protection is stopped but data is retained forever.</span></span>

### <span data-ttu-id="2ff49-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2ff49-114">Example 2</span></span>

<span data-ttu-id="2ff49-115">Ein soft-deleted Item wird erneut wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="2ff49-115">Rehydrates a soft-deleted Item.</span></span> <span data-ttu-id="2ff49-116">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="2ff49-116">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0] -VaultId $vault.ID
```

## <span data-ttu-id="2ff49-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ff49-117">PARAMETERS</span></span>

### <span data-ttu-id="2ff49-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ff49-118">-DefaultProfile</span></span>
<span data-ttu-id="2ff49-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2ff49-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ff49-120">-Force</span><span class="sxs-lookup"><span data-stu-id="2ff49-120">-Force</span></span>
<span data-ttu-id="2ff49-121">Deaktiviert den Sicherungsschutz mit "Erzwingen" (Bestätigungsdialogfeld wird verhindert).</span><span class="sxs-lookup"><span data-stu-id="2ff49-121">Force disables backup protection (prevents confirmation dialog).</span></span>
<span data-ttu-id="2ff49-122">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="2ff49-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="2ff49-123">-Item</span><span class="sxs-lookup"><span data-stu-id="2ff49-123">-Item</span></span>
<span data-ttu-id="2ff49-124">Gibt das Sicherungselement an, für das dieses Cmdlet den Löschvorgang zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="2ff49-124">Specifies the backup item for which this cmdlet reverts the deletion.</span></span>
<span data-ttu-id="2ff49-125">Verwenden Sie zum Abrufen eines AzureRmRecoveryServicesBackupItem das Get-AzRecoveryServicesBackupItem Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ff49-125">To obtain an AzureRmRecoveryServicesBackupItem , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="2ff49-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="2ff49-126">-VaultId</span></span>
<span data-ttu-id="2ff49-127">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="2ff49-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="2ff49-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ff49-128">-Confirm</span></span>
<span data-ttu-id="2ff49-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2ff49-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ff49-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2ff49-130">-WhatIf</span></span>
<span data-ttu-id="2ff49-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2ff49-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ff49-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2ff49-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ff49-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ff49-133">CommonParameters</span></span>
<span data-ttu-id="2ff49-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ff49-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ff49-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ff49-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ff49-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2ff49-136">INPUTS</span></span>

### <span data-ttu-id="2ff49-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="2ff49-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="2ff49-138">System.String</span><span class="sxs-lookup"><span data-stu-id="2ff49-138">System.String</span></span>

## <span data-ttu-id="2ff49-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2ff49-139">OUTPUTS</span></span>

### <span data-ttu-id="2ff49-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="2ff49-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="2ff49-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2ff49-141">NOTES</span></span>

## <span data-ttu-id="2ff49-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2ff49-142">RELATED LINKS</span></span>

[<span data-ttu-id="2ff49-143">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="2ff49-143">Get-AzRecoveryServicesBackupContainer</span></span>]()

[<span data-ttu-id="2ff49-144">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="2ff49-144">Get-AzRecoveryServicesBackupItem</span></span>]()

