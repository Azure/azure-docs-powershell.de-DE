---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/new-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/New-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/New-AzResourceGraphQuery.md
ms.openlocfilehash: 853c06c6179f25065efba71b2d148c36e2d74ef4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143649"
---
# <span data-ttu-id="f8619-101">New-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="f8619-101">New-AzResourceGraphQuery</span></span>

## <span data-ttu-id="f8619-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8619-102">SYNOPSIS</span></span>
<span data-ttu-id="f8619-103">Erstellen Sie eine neue Diagrammabfrage.</span><span class="sxs-lookup"><span data-stu-id="f8619-103">Create a new graph query.</span></span>

## <span data-ttu-id="f8619-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f8619-104">SYNTAX</span></span>

```
New-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-File <String>] [-Location <String>] [-Query <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f8619-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f8619-105">DESCRIPTION</span></span>
<span data-ttu-id="f8619-106">Erstellen Sie eine neue Diagrammabfrage.</span><span class="sxs-lookup"><span data-stu-id="f8619-106">Create a new graph query.</span></span>

## <span data-ttu-id="f8619-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f8619-107">EXAMPLES</span></span>

### <span data-ttu-id="f8619-108">Beispiel 1: Erstellen einer Ressourcendiagrammabfrage nach dem Abfrageparameter</span><span class="sxs-lookup"><span data-stu-id="f8619-108">Example 1: Create a resource graph query by the query parameter</span></span>
```powershell
PS C:\> New-AzResourceGraphQuery -Name query-t03 -ResourceGroupName azure-rg-test -Location "global" -Description "requesting a subset of resource fields." -Query "project id, name, type, location, tags" 


Location Name      Type
-------- ----      ----
     global   query-t03 microsoft.resourcegraph/queries
```

<span data-ttu-id="f8619-109">Mit diesem Befehl wird eine Ressourcendiagrammabfrage nach dem Abfrageparameter erstellt.</span><span class="sxs-lookup"><span data-stu-id="f8619-109">This command creates a resource graph query by the query parameter.</span></span>

### <span data-ttu-id="f8619-110">Beispiel 2: Erstellen einer Ressourcendiagrammabfrage nach dem Dateiparameter</span><span class="sxs-lookup"><span data-stu-id="f8619-110">Example 2: Create a resource graph query by the file parameter</span></span>
```powershell
PS C:\> New-AzResourceGraphQuery -Name query-t04 -ResourceGroupName azure-rg-test -Location "global" -Description "requesting a subset of resource fields." -File 'D:\azure-service\ResourceGraph.Autorest\azure-powershell\src\ResourceGraph\ResourceGraph.Autorest\test\Query.kql'

Location Name      Type
-------- ----      ----
     global   query-t04 microsoft.resourcegraph/queries
```

<span data-ttu-id="f8619-111">Mit diesem Befehl wird eine Ressourcendiagrammabfrage nach dem Dateiparameter erstellt.</span><span class="sxs-lookup"><span data-stu-id="f8619-111">This command creates a resource graph query by the file parameter.</span></span>

## <span data-ttu-id="f8619-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8619-112">PARAMETERS</span></span>

### <span data-ttu-id="f8619-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8619-113">-DefaultProfile</span></span>
<span data-ttu-id="f8619-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f8619-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8619-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f8619-115">-Description</span></span>
<span data-ttu-id="f8619-116">Die Beschreibung einer Diagrammabfrage.</span><span class="sxs-lookup"><span data-stu-id="f8619-116">The description of a graph query.</span></span>

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

### <span data-ttu-id="f8619-117">-File</span><span class="sxs-lookup"><span data-stu-id="f8619-117">-File</span></span>
<span data-ttu-id="f8619-118">Der Inhalt der Datei wird an den Abfrageparameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="f8619-118">The content of the file will be passed to the query parameter.</span></span>

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

### <span data-ttu-id="f8619-119">-Location</span><span class="sxs-lookup"><span data-stu-id="f8619-119">-Location</span></span>
<span data-ttu-id="f8619-120">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="f8619-120">The location of the resource</span></span>

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

### <span data-ttu-id="f8619-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f8619-121">-Name</span></span>
<span data-ttu-id="f8619-122">Der Name der Ressource "Diagrammabfrage".</span><span class="sxs-lookup"><span data-stu-id="f8619-122">The name of the Graph Query resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8619-123">-Query</span><span class="sxs-lookup"><span data-stu-id="f8619-123">-Query</span></span>
<span data-ttu-id="f8619-124">KQL-Abfrage, die graphisch dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f8619-124">KQL query that will be graph.</span></span>

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

### <span data-ttu-id="f8619-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8619-125">-ResourceGroupName</span></span>
<span data-ttu-id="f8619-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f8619-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8619-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f8619-127">-SubscriptionId</span></span>
<span data-ttu-id="f8619-128">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="f8619-128">The Azure subscription Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8619-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="f8619-129">-Tag</span></span>
<span data-ttu-id="f8619-130">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="f8619-130">Resource tags</span></span>

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

### <span data-ttu-id="f8619-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8619-131">-Confirm</span></span>
<span data-ttu-id="f8619-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f8619-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8619-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f8619-133">-WhatIf</span></span>
<span data-ttu-id="f8619-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f8619-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8619-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8619-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8619-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8619-136">CommonParameters</span></span>
<span data-ttu-id="f8619-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8619-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8619-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8619-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8619-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f8619-139">INPUTS</span></span>

### <span data-ttu-id="f8619-140">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="f8619-140">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

### <span data-ttu-id="f8619-141">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="f8619-141">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="f8619-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f8619-142">OUTPUTS</span></span>

### <span data-ttu-id="f8619-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="f8619-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="f8619-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f8619-144">NOTES</span></span>

<span data-ttu-id="f8619-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="f8619-145">ALIASES</span></span>

## <span data-ttu-id="f8619-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f8619-146">RELATED LINKS</span></span>

