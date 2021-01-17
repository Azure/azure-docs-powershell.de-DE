---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/undo-azrecoveryservicesbackupitemdeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
ms.openlocfilehash: 62d8dc302dc5819272034cfdd1c3fd0c0c79f54c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378341"
---
# <span data-ttu-id="6831b-101">Undo-AzRecoveryServicesBackupItemDeletion</span><span class="sxs-lookup"><span data-stu-id="6831b-101">Undo-AzRecoveryServicesBackupItemDeletion</span></span>

## <span data-ttu-id="6831b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6831b-102">SYNOPSIS</span></span>
<span data-ttu-id="6831b-103">Wenn ein Sicherungselement gelöscht wird und sich in einem Status "Soft-Deleted" befindet, bringt dieser Befehl das Element wieder in einen Zustand zurück, in dem die Daten für immer aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="6831b-103">If a backup item is deleted and present in a soft-deleted state, this command brings the item back to a state where the data is retained forever</span></span> 

## <span data-ttu-id="6831b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6831b-104">SYNTAX</span></span>

```
Undo-AzRecoveryServicesBackupItemDeletion [-Item] <ItemBase> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6831b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6831b-105">DESCRIPTION</span></span>
<span data-ttu-id="6831b-106">Das Undo-AzRecoveryServicesBackupItemDeletion-Cmdlet setzt ein soft-deleted-Element in einen Zustand zurück, in dem der Schutz beendet wird, die Daten jedoch für immer beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="6831b-106">The Undo-AzRecoveryServicesBackupItemDeletion cmdlet reverts a soft-deleted item to a state where the protection is stopped but data is retained forever.</span></span>

## <span data-ttu-id="6831b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6831b-107">EXAMPLES</span></span>

### <span data-ttu-id="6831b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6831b-108">Example 1</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM | Where-Object {$_.DeleteState -eq "ToBeDeleted"}
PS C:\> Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0]
```

<span data-ttu-id="6831b-109">Der erste Befehl ruft ein Array mit Sicherungscontainern ab und speichert es dann im $Cont Array.</span><span class="sxs-lookup"><span data-stu-id="6831b-109">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="6831b-110">Der zweite Befehl ruft das Sicherungselement ab, das dem ersten Containerelement entspricht, und speichert es dann in $PI Variable.</span><span class="sxs-lookup"><span data-stu-id="6831b-110">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="6831b-111">Der dritte Befehl deaktiviert den Sicherungsschutz für das Element in $PI 0 und versetzt das Element in einen \[ \] Softdelet-Zustand.</span><span class="sxs-lookup"><span data-stu-id="6831b-111">The third command disables Backup protection for the item in $PI\[0\] and puts the item in a softdeleted state.</span></span>
<span data-ttu-id="6831b-112">Der vierte Befehl ruft das Element ab, das sich in einem softdeleted-Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="6831b-112">The fourth command gets the item which is in a softdeleted state.</span></span>
<span data-ttu-id="6831b-113">Der letzte Befehl bringt die softdeleted VM in einen Zustand, in dem der Schutz gestoppt wird, die Daten jedoch für immer erhalten bleiben.</span><span class="sxs-lookup"><span data-stu-id="6831b-113">The last command brings the softdeleted VM to a state where the protection is stopped but data is retained forever.</span></span>

### <span data-ttu-id="6831b-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6831b-114">Example 2</span></span>

<span data-ttu-id="6831b-115">Ein soft-deleted Item wird erneut wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="6831b-115">Rehydrates a soft-deleted Item.</span></span> <span data-ttu-id="6831b-116">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="6831b-116">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0] -VaultId $vault.ID
```

## <span data-ttu-id="6831b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6831b-117">PARAMETERS</span></span>

### <span data-ttu-id="6831b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6831b-118">-DefaultProfile</span></span>
<span data-ttu-id="6831b-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6831b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6831b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="6831b-120">-Force</span></span>
<span data-ttu-id="6831b-121">Deaktiviert den Sicherungsschutz mit "Erzwingen" (Bestätigungsdialogfeld wird verhindert).</span><span class="sxs-lookup"><span data-stu-id="6831b-121">Force disables backup protection (prevents confirmation dialog).</span></span>
<span data-ttu-id="6831b-122">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6831b-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="6831b-123">-Item</span><span class="sxs-lookup"><span data-stu-id="6831b-123">-Item</span></span>
<span data-ttu-id="6831b-124">Gibt das Sicherungselement an, für das dieses Cmdlet den Löschvorgang zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="6831b-124">Specifies the backup item for which this cmdlet reverts the deletion.</span></span>
<span data-ttu-id="6831b-125">Verwenden Sie zum Abrufen eines AzureRmRecoveryServicesBackupItem das Get-AzRecoveryServicesBackupItem Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6831b-125">To obtain an AzureRmRecoveryServicesBackupItem , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="6831b-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="6831b-126">-VaultId</span></span>
<span data-ttu-id="6831b-127">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="6831b-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="6831b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6831b-128">-Confirm</span></span>
<span data-ttu-id="6831b-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6831b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6831b-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6831b-130">-WhatIf</span></span>
<span data-ttu-id="6831b-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6831b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6831b-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6831b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6831b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6831b-133">CommonParameters</span></span>
<span data-ttu-id="6831b-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6831b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6831b-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6831b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6831b-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6831b-136">INPUTS</span></span>

### <span data-ttu-id="6831b-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="6831b-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="6831b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="6831b-138">System.String</span></span>

## <span data-ttu-id="6831b-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6831b-139">OUTPUTS</span></span>

### <span data-ttu-id="6831b-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="6831b-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="6831b-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6831b-141">NOTES</span></span>

## <span data-ttu-id="6831b-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6831b-142">RELATED LINKS</span></span>

[<span data-ttu-id="6831b-143">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="6831b-143">Get-AzRecoveryServicesBackupContainer</span></span>]()

[<span data-ttu-id="6831b-144">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="6831b-144">Get-AzRecoveryServicesBackupItem</span></span>]()

