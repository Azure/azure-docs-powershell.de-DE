---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/undo-azrecoveryservicesbackupitemdeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
ms.openlocfilehash: 62d8dc302dc5819272034cfdd1c3fd0c0c79f54c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009565"
---
# <span data-ttu-id="32078-101">Undo-AzRecoveryServicesBackupItemDeletion</span><span class="sxs-lookup"><span data-stu-id="32078-101">Undo-AzRecoveryServicesBackupItemDeletion</span></span>

## <span data-ttu-id="32078-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="32078-102">SYNOPSIS</span></span>
<span data-ttu-id="32078-103">Wenn ein Backup-Element gelöscht und in einem Zustand mit weichem Löschstatus vorhanden ist, wird das Element wieder in einen Zustand versetzt, in dem die Daten für immer aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="32078-103">If a backup item is deleted and present in a soft-deleted state, this command brings the item back to a state where the data is retained forever</span></span> 

## <span data-ttu-id="32078-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="32078-104">SYNTAX</span></span>

```
Undo-AzRecoveryServicesBackupItemDeletion [-Item] <ItemBase> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32078-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="32078-105">DESCRIPTION</span></span>
<span data-ttu-id="32078-106">Mit dem Undo-AzRecoveryServicesBackupItemDeletion-Cmdlet wird ein Soft-Deleted-Element in einen Zustand zurückgesetzt, in dem der Schutz beendet wird, die Daten jedoch für immer aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="32078-106">The Undo-AzRecoveryServicesBackupItemDeletion cmdlet reverts a soft-deleted item to a state where the protection is stopped but data is retained forever.</span></span>

## <span data-ttu-id="32078-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="32078-107">EXAMPLES</span></span>

### <span data-ttu-id="32078-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="32078-108">Example 1</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM | Where-Object {$_.DeleteState -eq "ToBeDeleted"}
PS C:\> Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0]
```

<span data-ttu-id="32078-109">Der erste Befehl ruft ein Array von Sicherungs Containern ab und speichert es dann im $CONT-Array.</span><span class="sxs-lookup"><span data-stu-id="32078-109">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="32078-110">Der zweite Befehl ruft das Sicherungselement ab, das dem ersten Containerelement entspricht, und speichert es dann in der $Pi Variablen.</span><span class="sxs-lookup"><span data-stu-id="32078-110">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="32078-111">Der dritte Befehl deaktiviert den Sicherungsschutz für das Element in $Pi \[ 0 \] und platziert das Element in einem softdeleted-Zustand.</span><span class="sxs-lookup"><span data-stu-id="32078-111">The third command disables Backup protection for the item in $PI\[0\] and puts the item in a softdeleted state.</span></span>
<span data-ttu-id="32078-112">Der vierte Befehl ruft das Element ab, das sich in einem softdeleted-Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="32078-112">The fourth command gets the item which is in a softdeleted state.</span></span>
<span data-ttu-id="32078-113">Der letzte Befehl bewirkt, dass der softdeleted-VM in einen Zustand versetzt wird, in dem der Schutz beendet wird, die Daten jedoch für immer aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="32078-113">The last command brings the softdeleted VM to a state where the protection is stopped but data is retained forever.</span></span>

### <span data-ttu-id="32078-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="32078-114">Example 2</span></span>

<span data-ttu-id="32078-115">Pausiert ein Soft-Deleted-Element.</span><span class="sxs-lookup"><span data-stu-id="32078-115">Rehydrates a soft-deleted Item.</span></span> <span data-ttu-id="32078-116">automatisch</span><span class="sxs-lookup"><span data-stu-id="32078-116">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0] -VaultId $vault.ID
```

## <span data-ttu-id="32078-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="32078-117">PARAMETERS</span></span>

### <span data-ttu-id="32078-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32078-118">-DefaultProfile</span></span>
<span data-ttu-id="32078-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="32078-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32078-120">-Force</span><span class="sxs-lookup"><span data-stu-id="32078-120">-Force</span></span>
<span data-ttu-id="32078-121">Force deaktiviert den Sicherungsschutz (verhindert das Bestätigungsdialogfeld).</span><span class="sxs-lookup"><span data-stu-id="32078-121">Force disables backup protection (prevents confirmation dialog).</span></span>
<span data-ttu-id="32078-122">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="32078-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="32078-123">-Item</span><span class="sxs-lookup"><span data-stu-id="32078-123">-Item</span></span>
<span data-ttu-id="32078-124">Gibt das Sicherungselement an, für das dieses Cmdlet den Löschvorgang wieder herstellt.</span><span class="sxs-lookup"><span data-stu-id="32078-124">Specifies the backup item for which this cmdlet reverts the deletion.</span></span>
<span data-ttu-id="32078-125">Verwenden Sie zum Abrufen eines AzureRmRecoveryServicesBackupItem das Get-AzRecoveryServicesBackupItem-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32078-125">To obtain an AzureRmRecoveryServicesBackupItem , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="32078-126">-Tresor</span><span class="sxs-lookup"><span data-stu-id="32078-126">-VaultId</span></span>
<span data-ttu-id="32078-127">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="32078-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="32078-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="32078-128">-Confirm</span></span>
<span data-ttu-id="32078-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="32078-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32078-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32078-130">-WhatIf</span></span>
<span data-ttu-id="32078-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="32078-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32078-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="32078-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32078-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32078-133">CommonParameters</span></span>
<span data-ttu-id="32078-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32078-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32078-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32078-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32078-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="32078-136">INPUTS</span></span>

### <span data-ttu-id="32078-137">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="32078-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="32078-138">System. String</span><span class="sxs-lookup"><span data-stu-id="32078-138">System.String</span></span>

## <span data-ttu-id="32078-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="32078-139">OUTPUTS</span></span>

### <span data-ttu-id="32078-140">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="32078-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="32078-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="32078-141">NOTES</span></span>

## <span data-ttu-id="32078-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="32078-142">RELATED LINKS</span></span>

[<span data-ttu-id="32078-143">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="32078-143">Get-AzRecoveryServicesBackupContainer</span></span>]()

[<span data-ttu-id="32078-144">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="32078-144">Get-AzRecoveryServicesBackupItem</span></span>]()

