---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/get-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
ms.openlocfilehash: 6d7dbb9acbcc03f266d698d1f9d8ce89f320d04b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143652"
---
# <span data-ttu-id="c1fc5-101">Get-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="c1fc5-101">Get-AzResourceGraphQuery</span></span>

## <span data-ttu-id="c1fc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1fc5-102">SYNOPSIS</span></span>
<span data-ttu-id="c1fc5-103">Sie können eine Abfrage für einen einzelnen Diagrammtyp nach dem Ressourcennamen (resourceName) erhalten.</span><span class="sxs-lookup"><span data-stu-id="c1fc5-103">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="c1fc5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1fc5-104">SYNTAX</span></span>

### <span data-ttu-id="c1fc5-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="c1fc5-105">List (Default)</span></span>
```
Get-AzResourceGraphQuery -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1fc5-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="c1fc5-106">Get</span></span>
```
Get-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c1fc5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c1fc5-107">GetViaIdentity</span></span>
```
Get-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c1fc5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c1fc5-108">DESCRIPTION</span></span>
<span data-ttu-id="c1fc5-109">Sie können eine Abfrage für einen einzelnen Diagrammtyp nach dem Ressourcennamen (resourceName) erhalten.</span><span class="sxs-lookup"><span data-stu-id="c1fc5-109">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="c1fc5-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c1fc5-110">EXAMPLES</span></span>

### <span data-ttu-id="c1fc5-111">Beispiel 1: Alle Ressourcendiagrammabfragen unter einer Ressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="c1fc5-111">Example 1: Get all resource graph query under a resource group</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="c1fc5-112">Dieser Befehl ruft alle Ressourcendiagrammabfragen unter einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="c1fc5-112">This command gets all resource graph query under a resource group.</span></span>

### <span data-ttu-id="c1fc5-113">Beispiel 2: Erhalten einer Ressourcendiagrammabfrage nach Name</span><span class="sxs-lookup"><span data-stu-id="c1fc5-113">Example 2: Get a resource graph query by name</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name SharedQuery-t01

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="c1fc5-114">Dieser Befehl ruft eine Ressourcendiagrammabfrage nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="c1fc5-114">This command gets a resource graph query by name.</span></span>

### <span data-ttu-id="c1fc5-115">Beispiel 2: Abfragen von Ressourcendiagrammen per Objek</span><span class="sxs-lookup"><span data-stu-id="c1fc5-115">Example 2: Get a resource graph query by objecy</span></span>
```powershell
PS C:\> $query = New-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03 -Location 'global' -Query 'project id, name, type, location' -Description 'test'
PS C:\> Get-AzResourceGraphQuery -InputObject $query

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="c1fc5-116">Dieser Befehl ruft eine Ressourcendiagrammabfrage nach Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="c1fc5-116">This command gets a resource graph query by object.</span></span>

## <span data-ttu-id="c1fc5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1fc5-117">PARAMETERS</span></span>

### <span data-ttu-id="c1fc5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1fc5-118">-DefaultProfile</span></span>
<span data-ttu-id="c1fc5-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c1fc5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1fc5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1fc5-120">-InputObject</span></span>
<span data-ttu-id="c1fc5-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="c1fc5-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1fc5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c1fc5-122">-Name</span></span>
<span data-ttu-id="c1fc5-123">Der Name der Ressource "Diagrammabfrage".</span><span class="sxs-lookup"><span data-stu-id="c1fc5-123">The name of the Graph Query resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1fc5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1fc5-124">-ResourceGroupName</span></span>
<span data-ttu-id="c1fc5-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c1fc5-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1fc5-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c1fc5-126">-SubscriptionId</span></span>
<span data-ttu-id="c1fc5-127">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="c1fc5-127">The Azure subscription Id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1fc5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1fc5-128">CommonParameters</span></span>
<span data-ttu-id="c1fc5-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1fc5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1fc5-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1fc5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1fc5-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c1fc5-131">INPUTS</span></span>

### <span data-ttu-id="c1fc5-132">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="c1fc5-132">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="c1fc5-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c1fc5-133">OUTPUTS</span></span>

### <span data-ttu-id="c1fc5-134">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="c1fc5-134">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="c1fc5-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c1fc5-135">NOTES</span></span>

<span data-ttu-id="c1fc5-136">ALIASE</span><span class="sxs-lookup"><span data-stu-id="c1fc5-136">ALIASES</span></span>

<span data-ttu-id="c1fc5-137">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="c1fc5-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c1fc5-138">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c1fc5-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c1fc5-139">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c1fc5-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c1fc5-140">INPUTOBJECT <IResourceGraphIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="c1fc5-140">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c1fc5-141">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="c1fc5-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c1fc5-142">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c1fc5-142">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="c1fc5-143">`[ResourceName <String>]`: Der Name der Ressource "Diagrammabfrage".</span><span class="sxs-lookup"><span data-stu-id="c1fc5-143">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="c1fc5-144">`[SubscriptionId <String>]`: Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="c1fc5-144">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="c1fc5-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c1fc5-145">RELATED LINKS</span></span>

