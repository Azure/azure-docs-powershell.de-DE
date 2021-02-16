---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareAuthorization.md
ms.openlocfilehash: f4e4ea13f6e3fd46b1defa8dbf327024cb7557d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164492"
---
# <span data-ttu-id="d8d5e-101">Get-AzVMwareAuthorization</span><span class="sxs-lookup"><span data-stu-id="d8d5e-101">Get-AzVMwareAuthorization</span></span>

## <span data-ttu-id="d8d5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8d5e-102">SYNOPSIS</span></span>
<span data-ttu-id="d8d5e-103">Erhalten einer ExpressRoute-Schaltkreisautorisierung nach Name in einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="d8d5e-103">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="d8d5e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8d5e-104">SYNTAX</span></span>

### <span data-ttu-id="d8d5e-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="d8d5e-105">List (Default)</span></span>
```
Get-AzVMwareAuthorization -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d8d5e-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="d8d5e-106">Get</span></span>
```
Get-AzVMwareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d8d5e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d8d5e-107">GetViaIdentity</span></span>
```
Get-AzVMwareAuthorization -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d8d5e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d8d5e-108">DESCRIPTION</span></span>
<span data-ttu-id="d8d5e-109">Erhalten einer ExpressRoute-Schaltkreisautorisierung nach Name in einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="d8d5e-109">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="d8d5e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d8d5e-110">EXAMPLES</span></span>

### <span data-ttu-id="d8d5e-111">Beispiel 1: Autorisierung erhalten</span><span class="sxs-lookup"><span data-stu-id="d8d5e-111">Example 1: Get authorization</span></span>
```powershell
PS C:\> Get-AzVMwareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="d8d5e-112">Dieses Cmdlet erhält Autorisierung `azps-test-auth` in der privaten Cloud `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="d8d5e-112">This cmdlet gets authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

### <span data-ttu-id="d8d5e-113">Beispiel 2: Listenautorisierung</span><span class="sxs-lookup"><span data-stu-id="d8d5e-113">Example 2: List authorization</span></span>
```powershell
PS C:\> Get-AzVMwareAuthorization -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="d8d5e-114">Dieses Cmdlet listet die Autorisierung `azps-test-auth` in der privaten Cloud auf. `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="d8d5e-114">This cmdlet lists authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="d8d5e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8d5e-115">PARAMETERS</span></span>

### <span data-ttu-id="d8d5e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8d5e-116">-DefaultProfile</span></span>
<span data-ttu-id="d8d5e-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8d5e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8d5e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8d5e-118">-InputObject</span></span>
<span data-ttu-id="d8d5e-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d8d5e-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d8d5e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d8d5e-120">-Name</span></span>
<span data-ttu-id="d8d5e-121">Name der ExpressRoute-Schaltkreisautorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="d8d5e-121">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8d5e-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="d8d5e-122">-PrivateCloudName</span></span>
<span data-ttu-id="d8d5e-123">Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="d8d5e-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="d8d5e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8d5e-124">-ResourceGroupName</span></span>
<span data-ttu-id="d8d5e-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d8d5e-125">The name of the resource group.</span></span>
<span data-ttu-id="d8d5e-126">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="d8d5e-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d8d5e-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8d5e-127">-SubscriptionId</span></span>
<span data-ttu-id="d8d5e-128">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="d8d5e-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d8d5e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8d5e-129">CommonParameters</span></span>
<span data-ttu-id="d8d5e-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8d5e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8d5e-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8d5e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8d5e-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d8d5e-132">INPUTS</span></span>

### <span data-ttu-id="d8d5e-133">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span><span class="sxs-lookup"><span data-stu-id="d8d5e-133">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="d8d5e-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d8d5e-134">OUTPUTS</span></span>

### <span data-ttu-id="d8d5e-135">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="d8d5e-135">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="d8d5e-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d8d5e-136">NOTES</span></span>

<span data-ttu-id="d8d5e-137">ALIASE</span><span class="sxs-lookup"><span data-stu-id="d8d5e-137">ALIASES</span></span>

<span data-ttu-id="d8d5e-138">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="d8d5e-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d8d5e-139">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d8d5e-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d8d5e-140">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d8d5e-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d8d5e-141">INPUTOBJECT <IVMwareIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="d8d5e-141">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d8d5e-142">`[AuthorizationName <String>]`: Name der ExpressRoute-Schaltkreisautorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="d8d5e-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="d8d5e-143">`[ClusterName <String>]`: Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="d8d5e-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="d8d5e-144">`[HcxEnterpriseSiteName <String>]`: Name der HCX -Unternehmenswebsite in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="d8d5e-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="d8d5e-145">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="d8d5e-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d8d5e-146">`[Location <String>]`: Region Azure</span><span class="sxs-lookup"><span data-stu-id="d8d5e-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="d8d5e-147">`[PrivateCloudName <String>]`: Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="d8d5e-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="d8d5e-148">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d8d5e-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d8d5e-149">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="d8d5e-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="d8d5e-150">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="d8d5e-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="d8d5e-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d8d5e-151">RELATED LINKS</span></span>

