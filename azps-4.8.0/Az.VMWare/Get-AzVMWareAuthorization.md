---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareAuthorization.md
ms.openlocfilehash: fc89f62711744ad1e6bd7182eeb61fffd0478eaf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166714"
---
# <span data-ttu-id="c597f-101">Get-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="c597f-101">Get-AzVMWareAuthorization</span></span>

## <span data-ttu-id="c597f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c597f-102">SYNOPSIS</span></span>
<span data-ttu-id="c597f-103">Abrufen einer Express Route-Schaltkreis Autorisierung nach Namen in einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="c597f-103">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="c597f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c597f-104">SYNTAX</span></span>

### <span data-ttu-id="c597f-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="c597f-105">List (Default)</span></span>
```
Get-AzVMWareAuthorization -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c597f-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="c597f-106">Get</span></span>
```
Get-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c597f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c597f-107">GetViaIdentity</span></span>
```
Get-AzVMWareAuthorization -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c597f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c597f-108">DESCRIPTION</span></span>
<span data-ttu-id="c597f-109">Abrufen einer Express Route-Schaltkreis Autorisierung nach Namen in einer privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="c597f-109">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="c597f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c597f-110">EXAMPLES</span></span>

### <span data-ttu-id="c597f-111">Beispiel 1: Abrufen der Autorisierung</span><span class="sxs-lookup"><span data-stu-id="c597f-111">Example 1: Get authorization</span></span>
```powershell
PS C:\> Get-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="c597f-112">Dieses Cmdlet erhält die Autorisierung `azps-test-auth` unter privater Cloud. `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="c597f-112">This cmdlet gets authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

### <span data-ttu-id="c597f-113">Beispiel 2: Listen Autorisierung</span><span class="sxs-lookup"><span data-stu-id="c597f-113">Example 2: List authorization</span></span>
```powershell
PS C:\> Get-AzVMWareAuthorization -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="c597f-114">Dieses Cmdlet listet die Autorisierung `azps-test-auth` unter privater Cloud auf. `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="c597f-114">This cmdlet lists authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="c597f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="c597f-115">PARAMETERS</span></span>

### <span data-ttu-id="c597f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c597f-116">-DefaultProfile</span></span>
<span data-ttu-id="c597f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c597f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c597f-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c597f-118">-InputObject</span></span>
<span data-ttu-id="c597f-119">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c597f-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c597f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c597f-120">-Name</span></span>
<span data-ttu-id="c597f-121">Name der Express Route-Schaltkreis Autorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="c597f-121">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

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

### <span data-ttu-id="c597f-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="c597f-122">-PrivateCloudName</span></span>
<span data-ttu-id="c597f-123">Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="c597f-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="c597f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c597f-124">-ResourceGroupName</span></span>
<span data-ttu-id="c597f-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c597f-125">The name of the resource group.</span></span>
<span data-ttu-id="c597f-126">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="c597f-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c597f-127">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="c597f-127">-SubscriptionId</span></span>
<span data-ttu-id="c597f-128">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="c597f-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c597f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c597f-129">CommonParameters</span></span>
<span data-ttu-id="c597f-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c597f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c597f-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c597f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c597f-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c597f-132">INPUTS</span></span>

### <span data-ttu-id="c597f-133">Microsoft. Azure. PowerShell. Cmdlets. VMware. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="c597f-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="c597f-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c597f-134">OUTPUTS</span></span>

### <span data-ttu-id="c597f-135">Microsoft. Azure. PowerShell. Cmdlets. VMware. Models. Api20200320. IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="c597f-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="c597f-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="c597f-136">NOTES</span></span>

<span data-ttu-id="c597f-137">Aliase</span><span class="sxs-lookup"><span data-stu-id="c597f-137">ALIASES</span></span>

<span data-ttu-id="c597f-138">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c597f-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c597f-139">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c597f-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c597f-140">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="c597f-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c597f-141">Inputobject <IVMWareIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="c597f-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c597f-142">`[AuthorizationName <String>]`: Name der Express Route-Schaltkreis Autorisierung in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="c597f-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="c597f-143">`[ClusterName <String>]`: Name des Clusters in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="c597f-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="c597f-144">`[HcxEnterpriseSiteName <String>]`: Name der HCx Enterprise-Website in der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="c597f-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="c597f-145">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="c597f-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c597f-146">`[Location <String>]`: Azure-Bereich</span><span class="sxs-lookup"><span data-stu-id="c597f-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="c597f-147">`[PrivateCloudName <String>]`: Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="c597f-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="c597f-148">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c597f-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c597f-149">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="c597f-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="c597f-150">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="c597f-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="c597f-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c597f-151">RELATED LINKS</span></span>

