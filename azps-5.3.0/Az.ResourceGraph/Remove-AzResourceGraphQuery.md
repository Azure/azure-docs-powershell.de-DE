---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/remove-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Remove-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Remove-AzResourceGraphQuery.md
ms.openlocfilehash: 3fc5c493f94b6da371a4249479e397ea6e2362f0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377920"
---
# <span data-ttu-id="261c5-101">Remove-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="261c5-101">Remove-AzResourceGraphQuery</span></span>

## <span data-ttu-id="261c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="261c5-102">SYNOPSIS</span></span>
<span data-ttu-id="261c5-103">Löschen einer Diagrammabfrage</span><span class="sxs-lookup"><span data-stu-id="261c5-103">Delete a graph query.</span></span>

## <span data-ttu-id="261c5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="261c5-104">SYNTAX</span></span>

### <span data-ttu-id="261c5-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="261c5-105">Delete (Default)</span></span>
```
Remove-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="261c5-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="261c5-106">DeleteViaIdentity</span></span>
```
Remove-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="261c5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="261c5-107">DESCRIPTION</span></span>
<span data-ttu-id="261c5-108">Löschen einer Diagrammabfrage</span><span class="sxs-lookup"><span data-stu-id="261c5-108">Delete a graph query.</span></span>

## <span data-ttu-id="261c5-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="261c5-109">EXAMPLES</span></span>

### <span data-ttu-id="261c5-110">Beispiel 1: Entfernen einer Ressourcendiagrammabfrage nach Name</span><span class="sxs-lookup"><span data-stu-id="261c5-110">Example 1: Remove a resource graph query by name</span></span>
```powershell
PS C:\> Remove-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03

```

<span data-ttu-id="261c5-111">Mit diesem Befehl wird eine Ressourcendiagrammabfrage nach Name entfernt.</span><span class="sxs-lookup"><span data-stu-id="261c5-111">This command removes a resource graph query by name.</span></span>

### <span data-ttu-id="261c5-112">Beispiel 2: Entfernen einer Ressourcendiagrammabfrage nach Objekt</span><span class="sxs-lookup"><span data-stu-id="261c5-112">Example 2: Remove a resource graph query by object</span></span>
```powershell
PS C:\> $query = Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t02
PS C:\> Remove-AzResourceGraphQuery -InputObject $query 

```

<span data-ttu-id="261c5-113">Mit diesem Befehl wird eine Ressourcendiagrammabfrage nach Objekt entfernt.</span><span class="sxs-lookup"><span data-stu-id="261c5-113">This command removes a resource graph query by object.</span></span>

## <span data-ttu-id="261c5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="261c5-114">PARAMETERS</span></span>

### <span data-ttu-id="261c5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="261c5-115">-DefaultProfile</span></span>
<span data-ttu-id="261c5-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="261c5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="261c5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="261c5-117">-InputObject</span></span>
<span data-ttu-id="261c5-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="261c5-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="261c5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="261c5-119">-Name</span></span>
<span data-ttu-id="261c5-120">Der Name der Ressource "Diagrammabfrage".</span><span class="sxs-lookup"><span data-stu-id="261c5-120">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="261c5-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="261c5-121">-PassThru</span></span>
<span data-ttu-id="261c5-122">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="261c5-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="261c5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="261c5-123">-ResourceGroupName</span></span>
<span data-ttu-id="261c5-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="261c5-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="261c5-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="261c5-125">-SubscriptionId</span></span>
<span data-ttu-id="261c5-126">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="261c5-126">The Azure subscription Id.</span></span>

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

### <span data-ttu-id="261c5-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="261c5-127">-Confirm</span></span>
<span data-ttu-id="261c5-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="261c5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="261c5-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="261c5-129">-WhatIf</span></span>
<span data-ttu-id="261c5-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="261c5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="261c5-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="261c5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="261c5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="261c5-132">CommonParameters</span></span>
<span data-ttu-id="261c5-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="261c5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="261c5-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="261c5-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="261c5-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="261c5-135">INPUTS</span></span>

### <span data-ttu-id="261c5-136">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="261c5-136">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="261c5-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="261c5-137">OUTPUTS</span></span>

### <span data-ttu-id="261c5-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="261c5-138">System.Boolean</span></span>

## <span data-ttu-id="261c5-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="261c5-139">NOTES</span></span>

<span data-ttu-id="261c5-140">ALIASE</span><span class="sxs-lookup"><span data-stu-id="261c5-140">ALIASES</span></span>

<span data-ttu-id="261c5-141">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="261c5-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="261c5-142">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="261c5-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="261c5-143">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="261c5-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="261c5-144">INPUTOBJECT <IResourceGraphIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="261c5-144">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="261c5-145">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="261c5-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="261c5-146">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="261c5-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="261c5-147">`[ResourceName <String>]`: Der Name der Ressource "Diagrammabfrage".</span><span class="sxs-lookup"><span data-stu-id="261c5-147">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="261c5-148">`[SubscriptionId <String>]`: Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="261c5-148">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="261c5-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="261c5-149">RELATED LINKS</span></span>

