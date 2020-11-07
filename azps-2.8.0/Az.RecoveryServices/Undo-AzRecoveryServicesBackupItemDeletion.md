---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/undo-azrecoveryservicesbackupitemdeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
ms.openlocfilehash: 36b93041a2dfa4ba64779b2a92aeee50da53ce44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825191"
---
# <span data-ttu-id="584d7-101">Undo-AzRecoveryServicesBackupItemDeletion</span><span class="sxs-lookup"><span data-stu-id="584d7-101">Undo-AzRecoveryServicesBackupItemDeletion</span></span>

## <span data-ttu-id="584d7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="584d7-102">SYNOPSIS</span></span>
<span data-ttu-id="584d7-103">Pausiert ein Soft-Deleted-Element</span><span class="sxs-lookup"><span data-stu-id="584d7-103">Rehydrates a soft-deleted Item</span></span>

## <span data-ttu-id="584d7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="584d7-104">SYNTAX</span></span>

```
Undo-AzRecoveryServicesBackupItemDeletion [-Item] <ItemBase> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="584d7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="584d7-105">DESCRIPTION</span></span>
<span data-ttu-id="584d7-106">Mit dem Undo-AzRecoveryServicesBackupItemDeletion-Cmdlet wird ein Soft-Deleted-Element pausiert.</span><span class="sxs-lookup"><span data-stu-id="584d7-106">The Undo-AzRecoveryServicesBackupItemDeletion cmdlet rehydrates a soft-deleted item.</span></span>
<span data-ttu-id="584d7-107">Setzen Sie den Vault-Kontext mithilfe des Set-AzRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="584d7-107">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="584d7-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="584d7-108">EXAMPLES</span></span>

### <span data-ttu-id="584d7-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="584d7-109">Example 1</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0]
```

<span data-ttu-id="584d7-110">Der erste Befehl ruft ein Array von Sicherungs Containern ab und speichert es dann im $CONT-Array.</span><span class="sxs-lookup"><span data-stu-id="584d7-110">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="584d7-111">Der zweite Befehl ruft das Sicherungselement ab, das dem ersten Containerelement entspricht, und speichert es dann in der $Pi Variablen.</span><span class="sxs-lookup"><span data-stu-id="584d7-111">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="584d7-112">Der dritte Befehl deaktiviert den Sicherungsschutz für das Element in $Pi \[ 0 \] und platziert das Element in einem softdeleted-Zustand.</span><span class="sxs-lookup"><span data-stu-id="584d7-112">The third command disables Backup protection for the item in $PI\[0\] and puts the item in a softdeleted state.</span></span>
<span data-ttu-id="584d7-113">Der vierte Befehl das neue Element, das sich in einem softdeleted-Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="584d7-113">The fourth command the new item which is in a softdeleted state.</span></span>
<span data-ttu-id="584d7-114">Mit dem letzten Befehl wird die softdeleted-VM rehydriert.</span><span class="sxs-lookup"><span data-stu-id="584d7-114">The last command rehydrates the softdeleted VM.</span></span>


## <span data-ttu-id="584d7-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="584d7-115">PARAMETERS</span></span>

### <span data-ttu-id="584d7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="584d7-116">-DefaultProfile</span></span>
<span data-ttu-id="584d7-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="584d7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="584d7-118">-Force</span><span class="sxs-lookup"><span data-stu-id="584d7-118">-Force</span></span>
<span data-ttu-id="584d7-119">Force deaktiviert den Sicherungsschutz (verhindert das Bestätigungsdialogfeld).</span><span class="sxs-lookup"><span data-stu-id="584d7-119">Force disables backup protection (prevents confirmation dialog).</span></span>
<span data-ttu-id="584d7-120">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="584d7-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="584d7-121">-Item</span><span class="sxs-lookup"><span data-stu-id="584d7-121">-Item</span></span>
<span data-ttu-id="584d7-122">Gibt das Sicherungselement an, für das dieses Cmdlet den Schutz deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="584d7-122">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="584d7-123">Verwenden Sie zum Abrufen eines AzureRmRecoveryServicesBackupItem das Get-AzRecoveryServicesBackupItem-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="584d7-123">To obtain an AzureRmRecoveryServicesBackupItem , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="584d7-124">-Tresor</span><span class="sxs-lookup"><span data-stu-id="584d7-124">-VaultId</span></span>
<span data-ttu-id="584d7-125">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="584d7-125">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="584d7-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="584d7-126">-Confirm</span></span>
<span data-ttu-id="584d7-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="584d7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="584d7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="584d7-128">-WhatIf</span></span>
<span data-ttu-id="584d7-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="584d7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="584d7-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="584d7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="584d7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="584d7-131">CommonParameters</span></span>
<span data-ttu-id="584d7-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="584d7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="584d7-133">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="584d7-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="584d7-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="584d7-134">INPUTS</span></span>

### <span data-ttu-id="584d7-135">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="584d7-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="584d7-136">System. String</span><span class="sxs-lookup"><span data-stu-id="584d7-136">System.String</span></span>

## <span data-ttu-id="584d7-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="584d7-137">OUTPUTS</span></span>

### <span data-ttu-id="584d7-138">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="584d7-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="584d7-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="584d7-139">NOTES</span></span>

## <span data-ttu-id="584d7-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="584d7-140">RELATED LINKS</span></span>

[<span data-ttu-id="584d7-141">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="584d7-141">Get-AzRecoveryServicesBackupContainer</span></span>]()

[<span data-ttu-id="584d7-142">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="584d7-142">Get-AzRecoveryServicesBackupItem</span></span>]()

