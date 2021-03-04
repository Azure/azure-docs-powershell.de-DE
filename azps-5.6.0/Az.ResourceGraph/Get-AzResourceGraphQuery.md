---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/powershell/module/az.resourcegraph/get-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
ms.openlocfilehash: 46f59df272a62ca9cd6b517d3672436a01a75ffb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943643"
---
# <span data-ttu-id="54931-101">Get-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="54931-101">Get-AzResourceGraphQuery</span></span>

## <span data-ttu-id="54931-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54931-102">SYNOPSIS</span></span>
<span data-ttu-id="54931-103">Holen Sie sich eine einzelne Diagrammabfrage nach resourceName.</span><span class="sxs-lookup"><span data-stu-id="54931-103">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="54931-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54931-104">SYNTAX</span></span>

### <span data-ttu-id="54931-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="54931-105">List (Default)</span></span>
```
Get-AzResourceGraphQuery -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="54931-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="54931-106">Get</span></span>
```
Get-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="54931-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="54931-107">GetViaIdentity</span></span>
```
Get-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="54931-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="54931-108">DESCRIPTION</span></span>
<span data-ttu-id="54931-109">Holen Sie sich eine einzelne Diagrammabfrage nach resourceName.</span><span class="sxs-lookup"><span data-stu-id="54931-109">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="54931-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="54931-110">EXAMPLES</span></span>

### <span data-ttu-id="54931-111">Beispiel 1: Alle Ressourcendiagrammabfragen unter einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="54931-111">Example 1: Get all resource graph queries under a resource group</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="54931-112">Dieser Befehl ruft alle Ressourcendiagrammabfragen unter einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="54931-112">This command gets all resource graph query under a resource group.</span></span>

### <span data-ttu-id="54931-113">Beispiel 2: Abfragen eines Ressourcendiagramms nach Name</span><span class="sxs-lookup"><span data-stu-id="54931-113">Example 2: Get a resource graph query by name</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name SharedQuery-t01

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="54931-114">Dieser Befehl ruft eine Ressourcendiagrammabfrage nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="54931-114">This command gets a resource graph query by name.</span></span>

### <span data-ttu-id="54931-115">Beispiel 2: Abfragen eines Ressourcendiagramms nach Objekt</span><span class="sxs-lookup"><span data-stu-id="54931-115">Example 2: Get a resource graph query by object</span></span>
```powershell
PS C:\> $query = New-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03 -Location 'global' -Query 'project id, name, type, location' -Description 'test'
PS C:\> Get-AzResourceGraphQuery -InputObject $query

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="54931-116">Dieser Befehl ruft eine Ressourcendiagrammabfrage nach Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="54931-116">This command gets a resource graph query by object.</span></span>

## <span data-ttu-id="54931-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="54931-117">PARAMETERS</span></span>

### <span data-ttu-id="54931-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54931-118">-DefaultProfile</span></span>
<span data-ttu-id="54931-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="54931-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54931-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54931-120">-InputObject</span></span>
<span data-ttu-id="54931-121">Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="54931-121">Identity Parameter</span></span>

<span data-ttu-id="54931-122">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="54931-122">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="54931-123">-Name</span><span class="sxs-lookup"><span data-stu-id="54931-123">-Name</span></span>
<span data-ttu-id="54931-124">Der Name der Graph Query-Ressource.</span><span class="sxs-lookup"><span data-stu-id="54931-124">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="54931-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54931-125">-ResourceGroupName</span></span>
<span data-ttu-id="54931-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="54931-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="54931-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="54931-127">-SubscriptionId</span></span>
<span data-ttu-id="54931-128">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="54931-128">The Azure subscription Id.</span></span>

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

### <span data-ttu-id="54931-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54931-129">CommonParameters</span></span>
<span data-ttu-id="54931-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54931-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54931-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54931-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54931-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="54931-132">INPUTS</span></span>

### <span data-ttu-id="54931-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="54931-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="54931-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="54931-134">OUTPUTS</span></span>

### <span data-ttu-id="54931-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="54931-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="54931-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="54931-136">NOTES</span></span>

<span data-ttu-id="54931-137">ALIASE</span><span class="sxs-lookup"><span data-stu-id="54931-137">ALIASES</span></span>

<span data-ttu-id="54931-138">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="54931-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="54931-139">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="54931-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="54931-140">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="54931-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="54931-141">INPUTOBJECT <IResourceGraphIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="54931-141">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="54931-142">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="54931-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="54931-143">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="54931-143">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="54931-144">`[ResourceName <String>]`: Der Name der Graph Query-Ressource.</span><span class="sxs-lookup"><span data-stu-id="54931-144">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="54931-145">`[SubscriptionId <String>]`: Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="54931-145">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="54931-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="54931-146">RELATED LINKS</span></span>

