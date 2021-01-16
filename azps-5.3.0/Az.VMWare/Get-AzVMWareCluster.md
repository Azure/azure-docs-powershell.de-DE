---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareCluster.md
ms.openlocfilehash: bf763e152c482c4a3fda4951715b01008a730533
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470244"
---
# <span data-ttu-id="dd5d3-101">Get-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="dd5d3-101">Get-AzVMWareCluster</span></span>

## <span data-ttu-id="dd5d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd5d3-102">SYNOPSIS</span></span>
<span data-ttu-id="dd5d3-103">Clustern nach Namen in einer privaten Cloud erhalten</span><span class="sxs-lookup"><span data-stu-id="dd5d3-103">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="dd5d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd5d3-104">SYNTAX</span></span>

### <span data-ttu-id="dd5d3-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="dd5d3-105">List (Default)</span></span>
```
Get-AzVMWareCluster -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dd5d3-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="dd5d3-106">Get</span></span>
```
Get-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dd5d3-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dd5d3-107">GetViaIdentity</span></span>
```
Get-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="dd5d3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd5d3-108">DESCRIPTION</span></span>
<span data-ttu-id="dd5d3-109">Clustern nach Namen in einer privaten Cloud erhalten</span><span class="sxs-lookup"><span data-stu-id="dd5d3-109">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="dd5d3-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dd5d3-110">EXAMPLES</span></span>

### <span data-ttu-id="dd5d3-111">Beispiel 1: Cluster erhalten</span><span class="sxs-lookup"><span data-stu-id="dd5d3-111">Example 1: Get cluster</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="dd5d3-112">Cluster erhalten</span><span class="sxs-lookup"><span data-stu-id="dd5d3-112">Get cluster</span></span>

### <span data-ttu-id="dd5d3-113">Beispiel 2: Listenclustere</span><span class="sxs-lookup"><span data-stu-id="dd5d3-113">Example 2: List clusters</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="dd5d3-114">Listenclustere</span><span class="sxs-lookup"><span data-stu-id="dd5d3-114">List clusters</span></span>

## <span data-ttu-id="dd5d3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd5d3-115">PARAMETERS</span></span>

### <span data-ttu-id="dd5d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd5d3-116">-DefaultProfile</span></span>
<span data-ttu-id="dd5d3-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dd5d3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd5d3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd5d3-118">-InputObject</span></span>
<span data-ttu-id="dd5d3-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="dd5d3-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd5d3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="dd5d3-120">-Name</span></span>
<span data-ttu-id="dd5d3-121">Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="dd5d3-121">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd5d3-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="dd5d3-122">-PrivateCloudName</span></span>
<span data-ttu-id="dd5d3-123">Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="dd5d3-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="dd5d3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd5d3-124">-ResourceGroupName</span></span>
<span data-ttu-id="dd5d3-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dd5d3-125">The name of the resource group.</span></span>
<span data-ttu-id="dd5d3-126">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="dd5d3-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="dd5d3-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dd5d3-127">-SubscriptionId</span></span>
<span data-ttu-id="dd5d3-128">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="dd5d3-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="dd5d3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd5d3-129">CommonParameters</span></span>
<span data-ttu-id="dd5d3-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd5d3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd5d3-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd5d3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd5d3-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dd5d3-132">INPUTS</span></span>

### <span data-ttu-id="dd5d3-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="dd5d3-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="dd5d3-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dd5d3-134">OUTPUTS</span></span>

### <span data-ttu-id="dd5d3-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="dd5d3-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="dd5d3-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dd5d3-136">NOTES</span></span>

<span data-ttu-id="dd5d3-137">ALIASE</span><span class="sxs-lookup"><span data-stu-id="dd5d3-137">ALIASES</span></span>

<span data-ttu-id="dd5d3-138">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="dd5d3-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dd5d3-139">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dd5d3-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dd5d3-140">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dd5d3-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dd5d3-141">INPUTOBJECT <IVMWareIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="dd5d3-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dd5d3-142">`[AuthorizationName <String>]`: Name der ExpressRoute-Schaltkreisautorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="dd5d3-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="dd5d3-143">`[ClusterName <String>]`: Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="dd5d3-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="dd5d3-144">`[HcxEnterpriseSiteName <String>]`: Name der HCX -Unternehmenswebsite in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="dd5d3-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="dd5d3-145">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="dd5d3-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dd5d3-146">`[Location <String>]`: Region Azure</span><span class="sxs-lookup"><span data-stu-id="dd5d3-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="dd5d3-147">`[PrivateCloudName <String>]`: Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="dd5d3-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="dd5d3-148">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dd5d3-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="dd5d3-149">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="dd5d3-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="dd5d3-150">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="dd5d3-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="dd5d3-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dd5d3-151">RELATED LINKS</span></span>

