---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
ms.openlocfilehash: e8988f5dd6e2e37cc98c31ceab244693eae1941e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175844"
---
# <span data-ttu-id="ca881-101">Remove-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="ca881-101">Remove-AzConnectedMachine</span></span>

## <span data-ttu-id="ca881-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca881-102">SYNOPSIS</span></span>
<span data-ttu-id="ca881-103">Der Vorgang zum Entfernen einer Hybridcomputeridentität in Azure.</span><span class="sxs-lookup"><span data-stu-id="ca881-103">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="ca881-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca881-104">SYNTAX</span></span>

### <span data-ttu-id="ca881-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="ca881-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ca881-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ca881-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachine -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ca881-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ca881-107">DESCRIPTION</span></span>
<span data-ttu-id="ca881-108">Der Vorgang zum Entfernen einer Hybridcomputeridentität in Azure.</span><span class="sxs-lookup"><span data-stu-id="ca881-108">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="ca881-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ca881-109">EXAMPLES</span></span>

### <span data-ttu-id="ca881-110">Beispiel 1: Entfernen eines verbundenen Computers</span><span class="sxs-lookup"><span data-stu-id="ca881-110">Example 1: Remove a connected machine</span></span>
```powershell
PS C:\> Remove-AzConnectedMachine -Name myMachine -ResourceGroupName myRG

```

<span data-ttu-id="ca881-111">Löscht den verbundenen Computer.</span><span class="sxs-lookup"><span data-stu-id="ca881-111">Deletes the connected machine.</span></span>

### <span data-ttu-id="ca881-112">Beispiel 2: Entfernen verbundener Computer über die Pipeline</span><span class="sxs-lookup"><span data-stu-id="ca881-112">Example 2: Remove connected machines via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines | Remove-AzConnectedMachine

```

<span data-ttu-id="ca881-113">Entfernt alle Computer in der `contoso-connected-machines` Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ca881-113">Removes all machines in the `contoso-connected-machines` resource group.</span></span>

## <span data-ttu-id="ca881-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca881-114">PARAMETERS</span></span>

### <span data-ttu-id="ca881-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca881-115">-DefaultProfile</span></span>
<span data-ttu-id="ca881-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ca881-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca881-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca881-117">-InputObject</span></span>
<span data-ttu-id="ca881-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="ca881-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca881-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ca881-119">-Name</span></span>
<span data-ttu-id="ca881-120">Der Name des Hybridcomputers.</span><span class="sxs-lookup"><span data-stu-id="ca881-120">The name of the hybrid machine.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca881-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca881-121">-PassThru</span></span>
<span data-ttu-id="ca881-122">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="ca881-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ca881-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca881-123">-ResourceGroupName</span></span>
<span data-ttu-id="ca881-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ca881-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca881-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ca881-125">-SubscriptionId</span></span>
<span data-ttu-id="ca881-126">Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ca881-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ca881-127">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="ca881-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca881-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca881-128">-Confirm</span></span>
<span data-ttu-id="ca881-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ca881-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca881-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ca881-130">-WhatIf</span></span>
<span data-ttu-id="ca881-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ca881-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca881-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ca881-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca881-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca881-133">CommonParameters</span></span>
<span data-ttu-id="ca881-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca881-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca881-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca881-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca881-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ca881-136">INPUTS</span></span>

### <span data-ttu-id="ca881-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="ca881-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="ca881-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ca881-138">OUTPUTS</span></span>

### <span data-ttu-id="ca881-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ca881-139">System.Boolean</span></span>

## <span data-ttu-id="ca881-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ca881-140">NOTES</span></span>

<span data-ttu-id="ca881-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="ca881-141">ALIASES</span></span>

<span data-ttu-id="ca881-142">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="ca881-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ca881-143">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ca881-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ca881-144">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ca881-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ca881-145">INPUTOBJECT <IConnectedMachineIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="ca881-145">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ca881-146">`[ExtensionName <String>]`: Der Name der Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="ca881-146">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="ca881-147">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="ca881-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ca881-148">`[Name <String>]`: Der Name des Hybridcomputers.</span><span class="sxs-lookup"><span data-stu-id="ca881-148">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="ca881-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ca881-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="ca881-150">`[SubscriptionId <String>]`: Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ca881-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ca881-151">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="ca881-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ca881-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ca881-152">RELATED LINKS</span></span>

