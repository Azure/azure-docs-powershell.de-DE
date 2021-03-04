---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/get-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareCluster.md
ms.openlocfilehash: 842d0c26d4034a8c07415dfe8524b32623c07e89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936416"
---
# <span data-ttu-id="43d47-101">Get-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="43d47-101">Get-AzVMWareCluster</span></span>

## <span data-ttu-id="43d47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43d47-102">SYNOPSIS</span></span>
<span data-ttu-id="43d47-103">Einen Cluster nach Name in einer privaten Cloud erhalten</span><span class="sxs-lookup"><span data-stu-id="43d47-103">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="43d47-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43d47-104">SYNTAX</span></span>

### <span data-ttu-id="43d47-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="43d47-105">List (Default)</span></span>
```
Get-AzVMWareCluster -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="43d47-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="43d47-106">Get</span></span>
```
Get-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="43d47-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="43d47-107">GetViaIdentity</span></span>
```
Get-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="43d47-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43d47-108">DESCRIPTION</span></span>
<span data-ttu-id="43d47-109">Einen Cluster nach Name in einer privaten Cloud erhalten</span><span class="sxs-lookup"><span data-stu-id="43d47-109">Get a cluster by name in a private cloud</span></span>

## <span data-ttu-id="43d47-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="43d47-110">EXAMPLES</span></span>

### <span data-ttu-id="43d47-111">Beispiel 1: Cluster erhalten</span><span class="sxs-lookup"><span data-stu-id="43d47-111">Example 1: Get cluster</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="43d47-112">Cluster erhalten</span><span class="sxs-lookup"><span data-stu-id="43d47-112">Get cluster</span></span>

### <span data-ttu-id="43d47-113">Beispiel 2: Listencluster</span><span class="sxs-lookup"><span data-stu-id="43d47-113">Example 2: List clusters</span></span>
```powershell
PS C:\> Get-AzVMWareCluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

Name              Type
----              ----
azps-test-cluster Microsoft.AVS/privateClouds/clusters
```

<span data-ttu-id="43d47-114">Listencluster</span><span class="sxs-lookup"><span data-stu-id="43d47-114">List clusters</span></span>

## <span data-ttu-id="43d47-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="43d47-115">PARAMETERS</span></span>

### <span data-ttu-id="43d47-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43d47-116">-DefaultProfile</span></span>
<span data-ttu-id="43d47-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="43d47-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43d47-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43d47-118">-InputObject</span></span>
<span data-ttu-id="43d47-119">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="43d47-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="43d47-120">-Name</span><span class="sxs-lookup"><span data-stu-id="43d47-120">-Name</span></span>
<span data-ttu-id="43d47-121">Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="43d47-121">Name of the cluster in the private cloud</span></span>

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

### <span data-ttu-id="43d47-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="43d47-122">-PrivateCloudName</span></span>
<span data-ttu-id="43d47-123">Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="43d47-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="43d47-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43d47-124">-ResourceGroupName</span></span>
<span data-ttu-id="43d47-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="43d47-125">The name of the resource group.</span></span>
<span data-ttu-id="43d47-126">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="43d47-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="43d47-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="43d47-127">-SubscriptionId</span></span>
<span data-ttu-id="43d47-128">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="43d47-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="43d47-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43d47-129">CommonParameters</span></span>
<span data-ttu-id="43d47-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43d47-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43d47-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43d47-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43d47-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="43d47-132">INPUTS</span></span>

### <span data-ttu-id="43d47-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="43d47-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="43d47-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="43d47-134">OUTPUTS</span></span>

### <span data-ttu-id="43d47-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span><span class="sxs-lookup"><span data-stu-id="43d47-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ICluster</span></span>

## <span data-ttu-id="43d47-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="43d47-136">NOTES</span></span>

<span data-ttu-id="43d47-137">ALIASE</span><span class="sxs-lookup"><span data-stu-id="43d47-137">ALIASES</span></span>

<span data-ttu-id="43d47-138">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="43d47-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="43d47-139">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="43d47-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="43d47-140">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="43d47-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="43d47-141">INPUTOBJECT <IVMWareIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="43d47-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="43d47-142">`[AuthorizationName <String>]`: Name der ExpressRoute-Schaltkreisautorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="43d47-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="43d47-143">`[ClusterName <String>]`: Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="43d47-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="43d47-144">`[HcxEnterpriseSiteName <String>]`: Name der HCX Enterprise-Website in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="43d47-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="43d47-145">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="43d47-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="43d47-146">`[Location <String>]`: Azure Region</span><span class="sxs-lookup"><span data-stu-id="43d47-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="43d47-147">`[PrivateCloudName <String>]`: Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="43d47-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="43d47-148">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="43d47-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="43d47-149">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="43d47-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="43d47-150">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="43d47-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="43d47-151">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="43d47-151">RELATED LINKS</span></span>

