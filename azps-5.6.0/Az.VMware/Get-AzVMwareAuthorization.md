---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/get-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareAuthorization.md
ms.openlocfilehash: dad73292e6875e2cf38244ed74e0519490860c4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939059"
---
# <span data-ttu-id="9e7cf-101">Get-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="9e7cf-101">Get-AzVMWareAuthorization</span></span>

## <span data-ttu-id="9e7cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e7cf-102">SYNOPSIS</span></span>
<span data-ttu-id="9e7cf-103">Erhalten einer ExpressRoute-Schaltungsautorisierung nach Name in einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="9e7cf-103">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="9e7cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e7cf-104">SYNTAX</span></span>

### <span data-ttu-id="9e7cf-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="9e7cf-105">List (Default)</span></span>
```
Get-AzVMWareAuthorization -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9e7cf-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="9e7cf-106">Get</span></span>
```
Get-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9e7cf-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9e7cf-107">GetViaIdentity</span></span>
```
Get-AzVMWareAuthorization -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9e7cf-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e7cf-108">DESCRIPTION</span></span>
<span data-ttu-id="9e7cf-109">Erhalten einer ExpressRoute-Schaltungsautorisierung nach Name in einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="9e7cf-109">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="9e7cf-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9e7cf-110">EXAMPLES</span></span>

### <span data-ttu-id="9e7cf-111">Beispiel 1: Autorisierung erhalten</span><span class="sxs-lookup"><span data-stu-id="9e7cf-111">Example 1: Get authorization</span></span>
```powershell
PS C:\> Get-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="9e7cf-112">Dieses Cmdlet erhält Autorisierung `azps-test-auth` in der privaten Cloud `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="9e7cf-112">This cmdlet gets authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

### <span data-ttu-id="9e7cf-113">Beispiel 2: Listenautorisierung</span><span class="sxs-lookup"><span data-stu-id="9e7cf-113">Example 2: List authorization</span></span>
```powershell
PS C:\> Get-AzVMWareAuthorization -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="9e7cf-114">Dieses Cmdlet listet die Autorisierung `azps-test-auth` in der privaten Cloud auf. `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="9e7cf-114">This cmdlet lists authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="9e7cf-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9e7cf-115">PARAMETERS</span></span>

### <span data-ttu-id="9e7cf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e7cf-116">-DefaultProfile</span></span>
<span data-ttu-id="9e7cf-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e7cf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e7cf-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e7cf-118">-InputObject</span></span>
<span data-ttu-id="9e7cf-119">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="9e7cf-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9e7cf-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9e7cf-120">-Name</span></span>
<span data-ttu-id="9e7cf-121">Name der ExpressRoute-Schaltkreisautorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="9e7cf-121">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

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

### <span data-ttu-id="9e7cf-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="9e7cf-122">-PrivateCloudName</span></span>
<span data-ttu-id="9e7cf-123">Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="9e7cf-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="9e7cf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e7cf-124">-ResourceGroupName</span></span>
<span data-ttu-id="9e7cf-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9e7cf-125">The name of the resource group.</span></span>
<span data-ttu-id="9e7cf-126">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="9e7cf-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9e7cf-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9e7cf-127">-SubscriptionId</span></span>
<span data-ttu-id="9e7cf-128">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="9e7cf-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9e7cf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e7cf-129">CommonParameters</span></span>
<span data-ttu-id="9e7cf-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e7cf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e7cf-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e7cf-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e7cf-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9e7cf-132">INPUTS</span></span>

### <span data-ttu-id="9e7cf-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="9e7cf-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="9e7cf-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9e7cf-134">OUTPUTS</span></span>

### <span data-ttu-id="9e7cf-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="9e7cf-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="9e7cf-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9e7cf-136">NOTES</span></span>

<span data-ttu-id="9e7cf-137">ALIASE</span><span class="sxs-lookup"><span data-stu-id="9e7cf-137">ALIASES</span></span>

<span data-ttu-id="9e7cf-138">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="9e7cf-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9e7cf-139">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="9e7cf-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9e7cf-140">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9e7cf-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9e7cf-141">INPUTOBJECT <IVMWareIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="9e7cf-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9e7cf-142">`[AuthorizationName <String>]`: Name der ExpressRoute-Schaltkreisautorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="9e7cf-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="9e7cf-143">`[ClusterName <String>]`: Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="9e7cf-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="9e7cf-144">`[HcxEnterpriseSiteName <String>]`: Name der HCX Enterprise-Website in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="9e7cf-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="9e7cf-145">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="9e7cf-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9e7cf-146">`[Location <String>]`: Azure Region</span><span class="sxs-lookup"><span data-stu-id="9e7cf-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="9e7cf-147">`[PrivateCloudName <String>]`: Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="9e7cf-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="9e7cf-148">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9e7cf-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9e7cf-149">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="9e7cf-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="9e7cf-150">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="9e7cf-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="9e7cf-151">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9e7cf-151">RELATED LINKS</span></span>

