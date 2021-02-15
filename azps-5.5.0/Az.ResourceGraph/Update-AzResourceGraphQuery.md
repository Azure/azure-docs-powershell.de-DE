---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/update-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Update-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Update-AzResourceGraphQuery.md
ms.openlocfilehash: 6ae44183a368babb43a93063518dfbf4f3d15e18
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143601"
---
# <span data-ttu-id="7344a-101">Update-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="7344a-101">Update-AzResourceGraphQuery</span></span>

## <span data-ttu-id="7344a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7344a-102">SYNOPSIS</span></span>
<span data-ttu-id="7344a-103">Aktualisiert eine diagrammabfrage, die bereits hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="7344a-103">Updates a graph query that has already been added.</span></span>

## <span data-ttu-id="7344a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7344a-104">SYNTAX</span></span>

### <span data-ttu-id="7344a-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="7344a-105">UpdateExpanded (Default)</span></span>
```
Update-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-File <String>] [-Query <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7344a-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7344a-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-Description <String>] [-File <String>]
 [-Query <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7344a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7344a-107">DESCRIPTION</span></span>
<span data-ttu-id="7344a-108">Aktualisiert eine diagrammabfrage, die bereits hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="7344a-108">Updates a graph query that has already been added.</span></span>

## <span data-ttu-id="7344a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7344a-109">EXAMPLES</span></span>

### <span data-ttu-id="7344a-110">Beispiel 1: Aktualisieren der Parameterabfrage und des Tags nach Name</span><span class="sxs-lookup"><span data-stu-id="7344a-110">Example 1: Update the parameter query and tag by name</span></span>
```powershell
PS C:\>  Update-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t05 -Query "project id, name, type, location, tags"  -Tag @{'key1'=1;'key2'=2}

Location Name      Type
-------- ----      ----
     global   query-t05 microsoft.resourcegraph/queries
```

<span data-ttu-id="7344a-111">Mit diesem Befehl werden die Parameterabfrage und das Tag nach Name aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7344a-111">This command updates the parameter query and tag by name.</span></span>

### <span data-ttu-id="7344a-112">Beispiel 2: Aktualisieren der Parameterdatei nach Objekt</span><span class="sxs-lookup"><span data-stu-id="7344a-112">Example 2: Update the parameter file by object</span></span>
```powershell
PS C:\> $query =  Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t05 
PS C:\> Update-AzResourceGraphQuery -InputObject $query -File './Query.kql'

Location Name      Type
-------- ----      ----
     global   query-t05 microsoft.resourcegraph/queries
```

<span data-ttu-id="7344a-113">Mit diesem Befehl werden die Parameterabfrage und das Tag nach Objekt aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7344a-113">This command updates the parameter query and tag by object.</span></span>

## <span data-ttu-id="7344a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7344a-114">PARAMETERS</span></span>

### <span data-ttu-id="7344a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7344a-115">-DefaultProfile</span></span>
<span data-ttu-id="7344a-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7344a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7344a-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7344a-117">-Description</span></span>
<span data-ttu-id="7344a-118">Die Beschreibung einer Diagrammabfrage.</span><span class="sxs-lookup"><span data-stu-id="7344a-118">The description of a graph query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7344a-119">-File</span><span class="sxs-lookup"><span data-stu-id="7344a-119">-File</span></span>
<span data-ttu-id="7344a-120">Der Inhalt der Datei wird an den Abfrageparameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="7344a-120">The content of the file will be passed to the query parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7344a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7344a-121">-InputObject</span></span>
<span data-ttu-id="7344a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="7344a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7344a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="7344a-123">-Name</span></span>
<span data-ttu-id="7344a-124">Der Name der Ressource "Diagrammabfrage".</span><span class="sxs-lookup"><span data-stu-id="7344a-124">The name of the Graph Query resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7344a-125">-Query</span><span class="sxs-lookup"><span data-stu-id="7344a-125">-Query</span></span>
<span data-ttu-id="7344a-126">KQL-Abfrage, die graphisch dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7344a-126">KQL query that will be graph.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7344a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7344a-127">-ResourceGroupName</span></span>
<span data-ttu-id="7344a-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7344a-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7344a-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7344a-129">-SubscriptionId</span></span>
<span data-ttu-id="7344a-130">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="7344a-130">The Azure subscription Id.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7344a-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="7344a-131">-Tag</span></span>
<span data-ttu-id="7344a-132">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="7344a-132">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7344a-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7344a-133">-Confirm</span></span>
<span data-ttu-id="7344a-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7344a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7344a-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7344a-135">-WhatIf</span></span>
<span data-ttu-id="7344a-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7344a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7344a-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7344a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7344a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7344a-138">CommonParameters</span></span>
<span data-ttu-id="7344a-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7344a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7344a-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7344a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7344a-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7344a-141">INPUTS</span></span>

### <span data-ttu-id="7344a-142">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="7344a-142">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="7344a-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7344a-143">OUTPUTS</span></span>

### <span data-ttu-id="7344a-144">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="7344a-144">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="7344a-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7344a-145">NOTES</span></span>

<span data-ttu-id="7344a-146">ALIASE</span><span class="sxs-lookup"><span data-stu-id="7344a-146">ALIASES</span></span>

<span data-ttu-id="7344a-147">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="7344a-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7344a-148">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7344a-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7344a-149">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7344a-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7344a-150">INPUTOBJECT <IResourceGraphIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="7344a-150">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7344a-151">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="7344a-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7344a-152">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7344a-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="7344a-153">`[ResourceName <String>]`: Der Name der Ressource "Diagrammabfrage".</span><span class="sxs-lookup"><span data-stu-id="7344a-153">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="7344a-154">`[SubscriptionId <String>]`: Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="7344a-154">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="7344a-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7344a-155">RELATED LINKS</span></span>

