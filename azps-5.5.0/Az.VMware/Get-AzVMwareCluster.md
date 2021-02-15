---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareCluster.md
ms.openlocfilehash: 51a889abe0d1842f66a0ed9b17f3b07acd85a54b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174833"
---
# <span data-ttu-id="480b0-101">Get-AzVMwareCluster</span><span class="sxs-lookup"><span data-stu-id="480b0-101">Get-AzVMwareCluster</span></span>

## <span data-ttu-id="480b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="480b0-102">SYNOPSIS</span></span>
<span data-ttu-id="480b0-103">Clustern nach Namen in einer privaten Cloud erhalten</span><span class="sxs-lookup"><span data-stu-id="480b0-103">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="480b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="480b0-104">SYNTAX</span></span>

### <span data-ttu-id="480b0-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="480b0-105">List (Default)</span></span>
```
Get-AzVMwareCluster -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="480b0-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="480b0-106">Get</span></span>
```
Get-AzVMwareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="480b0-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="480b0-107">GetViaIdentity</span></span>
```
Get-AzVMwareCluster -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="480b0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="480b0-108">DESCRIPTION</span></span>
<span data-ttu-id="480b0-109">Clustern nach Namen in einer privaten Cloud erhalten</span><span class="sxs-lookup"><span data-stu-id="480b0-109">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="480b0-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="480b0-110">EXAMPLES</span></span>

### <span data-ttu-id="480b0-111">Beispiel 1: Cluster erhalten</span><span class="sxs-lookup"><span data-stu-id="480b0-111">Example 1: Get cluster</span></span>
```powershell
PS C:\> Get-AzVMwareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="480b0-112">Cluster erhalten</span><span class="sxs-lookup"><span data-stu-id="480b0-112">Get cluster</span></span>

### <span data-ttu-id="480b0-113">Beispiel 2: Listenclustere</span><span class="sxs-lookup"><span data-stu-id="480b0-113">Example 2: List clusters</span></span>
```powershell
PS C:\> Get-AzVMwareCluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="480b0-114">Listenclustere</span><span class="sxs-lookup"><span data-stu-id="480b0-114">List clusters</span></span>

## <span data-ttu-id="480b0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="480b0-115">PARAMETERS</span></span>

### <span data-ttu-id="480b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="480b0-116">-DefaultProfile</span></span>
<span data-ttu-id="480b0-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="480b0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="480b0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="480b0-118">-InputObject</span></span>
<span data-ttu-id="480b0-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="480b0-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="480b0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="480b0-120">-Name</span></span>
<span data-ttu-id="480b0-121">Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="480b0-121">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="480b0-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="480b0-122">-PrivateCloudName</span></span>
<span data-ttu-id="480b0-123">Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="480b0-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="480b0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="480b0-124">-ResourceGroupName</span></span>
<span data-ttu-id="480b0-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="480b0-125">The name of the resource group.</span></span>
<span data-ttu-id="480b0-126">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="480b0-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="480b0-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="480b0-127">-SubscriptionId</span></span>
<span data-ttu-id="480b0-128">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="480b0-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="480b0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="480b0-129">CommonParameters</span></span>
<span data-ttu-id="480b0-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="480b0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="480b0-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="480b0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="480b0-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="480b0-132">INPUTS</span></span>

### <span data-ttu-id="480b0-133">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span><span class="sxs-lookup"><span data-stu-id="480b0-133">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="480b0-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="480b0-134">OUTPUTS</span></span>

### <span data-ttu-id="480b0-135">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="480b0-135">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="480b0-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="480b0-136">NOTES</span></span>

<span data-ttu-id="480b0-137">ALIASE</span><span class="sxs-lookup"><span data-stu-id="480b0-137">ALIASES</span></span>

<span data-ttu-id="480b0-138">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="480b0-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="480b0-139">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="480b0-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="480b0-140">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="480b0-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="480b0-141">INPUTOBJECT <IVMwareIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="480b0-141">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="480b0-142">`[AuthorizationName <String>]`: Name der ExpressRoute-Schaltkreisautorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="480b0-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="480b0-143">`[ClusterName <String>]`: Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="480b0-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="480b0-144">`[HcxEnterpriseSiteName <String>]`: Name der HCX -Unternehmenswebsite in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="480b0-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="480b0-145">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="480b0-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="480b0-146">`[Location <String>]`: Region Azure</span><span class="sxs-lookup"><span data-stu-id="480b0-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="480b0-147">`[PrivateCloudName <String>]`: Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="480b0-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="480b0-148">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="480b0-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="480b0-149">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="480b0-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="480b0-150">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="480b0-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="480b0-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="480b0-151">RELATED LINKS</span></span>

