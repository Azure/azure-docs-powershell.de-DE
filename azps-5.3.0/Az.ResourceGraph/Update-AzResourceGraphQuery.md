---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/update-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Update-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Update-AzResourceGraphQuery.md
ms.openlocfilehash: 6ae44183a368babb43a93063518dfbf4f3d15e18
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377893"
---
# <span data-ttu-id="cde77-101">Update-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="cde77-101">Update-AzResourceGraphQuery</span></span>

## <span data-ttu-id="cde77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cde77-102">SYNOPSIS</span></span>
<span data-ttu-id="cde77-103">Aktualisiert eine diagrammabfrage, die bereits hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="cde77-103">Updates a graph query that has already been added.</span></span>

## <span data-ttu-id="cde77-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cde77-104">SYNTAX</span></span>

### <span data-ttu-id="cde77-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="cde77-105">UpdateExpanded (Default)</span></span>
```
Update-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-File <String>] [-Query <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cde77-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="cde77-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-Description <String>] [-File <String>]
 [-Query <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cde77-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cde77-107">DESCRIPTION</span></span>
<span data-ttu-id="cde77-108">Aktualisiert eine diagrammabfrage, die bereits hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="cde77-108">Updates a graph query that has already been added.</span></span>

## <span data-ttu-id="cde77-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cde77-109">EXAMPLES</span></span>

### <span data-ttu-id="cde77-110">Beispiel 1: Aktualisieren der Parameterabfrage und des Tags nach Name</span><span class="sxs-lookup"><span data-stu-id="cde77-110">Example 1: Update the parameter query and tag by name</span></span>
```powershell
PS C:\>  Update-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t05 -Query "project id, name, type, location, tags"  -Tag @{'key1'=1;'key2'=2}

Location Name      Type
-------- ----      ----
     global   query-t05 microsoft.resourcegraph/queries
```

<span data-ttu-id="cde77-111">Mit diesem Befehl werden die Parameterabfrage und das Tag nach Name aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cde77-111">This command updates the parameter query and tag by name.</span></span>

### <span data-ttu-id="cde77-112">Beispiel 2: Aktualisieren der Parameterdatei nach Objekt</span><span class="sxs-lookup"><span data-stu-id="cde77-112">Example 2: Update the parameter file by object</span></span>
```powershell
PS C:\> $query =  Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t05 
PS C:\> Update-AzResourceGraphQuery -InputObject $query -File './Query.kql'

Location Name      Type
-------- ----      ----
     global   query-t05 microsoft.resourcegraph/queries
```

<span data-ttu-id="cde77-113">Mit diesem Befehl werden die Parameterabfrage und das Tag nach Objekt aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cde77-113">This command updates the parameter query and tag by object.</span></span>

## <span data-ttu-id="cde77-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cde77-114">PARAMETERS</span></span>

### <span data-ttu-id="cde77-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cde77-115">-DefaultProfile</span></span>
<span data-ttu-id="cde77-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cde77-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cde77-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cde77-117">-Description</span></span>
<span data-ttu-id="cde77-118">Die Beschreibung einer Diagrammabfrage.</span><span class="sxs-lookup"><span data-stu-id="cde77-118">The description of a graph query.</span></span>

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

### <span data-ttu-id="cde77-119">-File</span><span class="sxs-lookup"><span data-stu-id="cde77-119">-File</span></span>
<span data-ttu-id="cde77-120">Der Inhalt der Datei wird an den Abfrageparameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="cde77-120">The content of the file will be passed to the query parameter.</span></span>

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

### <span data-ttu-id="cde77-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cde77-121">-InputObject</span></span>
<span data-ttu-id="cde77-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="cde77-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cde77-123">-Name</span><span class="sxs-lookup"><span data-stu-id="cde77-123">-Name</span></span>
<span data-ttu-id="cde77-124">Der Name der Ressource "Diagrammabfrage".</span><span class="sxs-lookup"><span data-stu-id="cde77-124">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="cde77-125">-Query</span><span class="sxs-lookup"><span data-stu-id="cde77-125">-Query</span></span>
<span data-ttu-id="cde77-126">KQL-Abfrage, die grafisch dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cde77-126">KQL query that will be graph.</span></span>

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

### <span data-ttu-id="cde77-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cde77-127">-ResourceGroupName</span></span>
<span data-ttu-id="cde77-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cde77-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="cde77-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cde77-129">-SubscriptionId</span></span>
<span data-ttu-id="cde77-130">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="cde77-130">The Azure subscription Id.</span></span>

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

### <span data-ttu-id="cde77-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="cde77-131">-Tag</span></span>
<span data-ttu-id="cde77-132">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="cde77-132">Resource tags</span></span>

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

### <span data-ttu-id="cde77-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cde77-133">-Confirm</span></span>
<span data-ttu-id="cde77-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cde77-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cde77-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="cde77-135">-WhatIf</span></span>
<span data-ttu-id="cde77-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cde77-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cde77-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cde77-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cde77-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cde77-138">CommonParameters</span></span>
<span data-ttu-id="cde77-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cde77-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cde77-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cde77-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cde77-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cde77-141">INPUTS</span></span>

### <span data-ttu-id="cde77-142">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="cde77-142">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="cde77-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cde77-143">OUTPUTS</span></span>

### <span data-ttu-id="cde77-144">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="cde77-144">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="cde77-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cde77-145">NOTES</span></span>

<span data-ttu-id="cde77-146">ALIASE</span><span class="sxs-lookup"><span data-stu-id="cde77-146">ALIASES</span></span>

<span data-ttu-id="cde77-147">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="cde77-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cde77-148">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cde77-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cde77-149">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cde77-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cde77-150">INPUTOBJECT <IResourceGraphIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="cde77-150">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cde77-151">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="cde77-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cde77-152">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cde77-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="cde77-153">`[ResourceName <String>]`: Der Name der Ressource "Diagrammabfrage".</span><span class="sxs-lookup"><span data-stu-id="cde77-153">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="cde77-154">`[SubscriptionId <String>]`: Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="cde77-154">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="cde77-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cde77-155">RELATED LINKS</span></span>

