---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.addomainservices/get-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Get-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Get-AzADDomainService.md
ms.openlocfilehash: ec52bea37eed3bb785da80beb8dfba02d0a426cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143836"
---
# <span data-ttu-id="a9911-101">Get-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="a9911-101">Get-AzADDomainService</span></span>

## <span data-ttu-id="a9911-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9911-102">SYNOPSIS</span></span>
<span data-ttu-id="a9911-103">Der Get Domain Service-Vorgang ruft eine json-Darstellung des Domain Service ab.</span><span class="sxs-lookup"><span data-stu-id="a9911-103">The Get Domain Service operation retrieves a json representation of the Domain Service.</span></span>

## <span data-ttu-id="a9911-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9911-104">SYNTAX</span></span>

### <span data-ttu-id="a9911-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="a9911-105">List (Default)</span></span>
```
Get-AzADDomainService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a9911-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="a9911-106">Get</span></span>
```
Get-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a9911-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a9911-107">GetViaIdentity</span></span>
```
Get-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="a9911-108">Liste1</span><span class="sxs-lookup"><span data-stu-id="a9911-108">List1</span></span>
```
Get-AzADDomainService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9911-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a9911-109">DESCRIPTION</span></span>
<span data-ttu-id="a9911-110">Der Get Domain Service-Vorgang ruft eine json-Darstellung des Domain Service ab.</span><span class="sxs-lookup"><span data-stu-id="a9911-110">The Get Domain Service operation retrieves a json representation of the Domain Service.</span></span>

## <span data-ttu-id="a9911-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a9911-111">EXAMPLES</span></span>

### <span data-ttu-id="a9911-112">Beispiel 1: Standardmäßiges "Get All ADDomainService"</span><span class="sxs-lookup"><span data-stu-id="a9911-112">Example 1: Get All ADDomainService By default</span></span>
```powershell
PS C:\> Get-AzADDomainService

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="a9911-113">Standardmäßiges "Get All ADDomainService"</span><span class="sxs-lookup"><span data-stu-id="a9911-113">Get All ADDomainService By default</span></span>

### <span data-ttu-id="a9911-114">Beispiel 2: "ADDomainService by ResourceGroup" und den Namen</span><span class="sxs-lookup"><span data-stu-id="a9911-114">Example 2: Get ADDomainService By ResourceGroup and name</span></span>
```powershell
PS C:\> Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="a9911-115">ADDomainService nach ResourceGroup und Name</span><span class="sxs-lookup"><span data-stu-id="a9911-115">Get ADDomainService By ResourceGroup and name</span></span>

### <span data-ttu-id="a9911-116">Beispiel 3: "Get all ADDomainService By ResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="a9911-116">Example 3: Get all ADDomainService By ResourceGroup</span></span>
```powershell
PS C:\> Get-AzADDomainService -ResourceGroupName youriADdomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="a9911-117">"Get all ADDomainService By ResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="a9911-117">Get all ADDomainService By ResourceGroup</span></span>

### <span data-ttu-id="a9911-118">Beispiel 4: Erhalten von ADDomainService von InputObject</span><span class="sxs-lookup"><span data-stu-id="a9911-118">Example 4: Get ADDomainService By InputObject</span></span>
```powershell
PS C:\> $getAzAddomain = Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain
Get-AzADDomainService -InputObject $getAzAddomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="a9911-119">ADDomainService von InputObject erhalten</span><span class="sxs-lookup"><span data-stu-id="a9911-119">Get ADDomainService By InputObject</span></span>

## <span data-ttu-id="a9911-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9911-120">PARAMETERS</span></span>

### <span data-ttu-id="a9911-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9911-121">-DefaultProfile</span></span>
<span data-ttu-id="a9911-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a9911-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9911-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9911-123">-InputObject</span></span>
<span data-ttu-id="a9911-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="a9911-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9911-125">-Name</span><span class="sxs-lookup"><span data-stu-id="a9911-125">-Name</span></span>
<span data-ttu-id="a9911-126">Der Name des Domänendiensts.</span><span class="sxs-lookup"><span data-stu-id="a9911-126">The name of the domain service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9911-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9911-127">-ResourceGroupName</span></span>
<span data-ttu-id="a9911-128">Der Name der Ressourcengruppe im Abonnement des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="a9911-128">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="a9911-129">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="a9911-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9911-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a9911-130">-SubscriptionId</span></span>
<span data-ttu-id="a9911-131">Ruft Abonnementanmeldeinformationen ab, mit denen das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="a9911-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a9911-132">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="a9911-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9911-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9911-133">CommonParameters</span></span>
<span data-ttu-id="a9911-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9911-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9911-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9911-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9911-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a9911-136">INPUTS</span></span>

### <span data-ttu-id="a9911-137">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="a9911-137">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span></span>

## <span data-ttu-id="a9911-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a9911-138">OUTPUTS</span></span>

### <span data-ttu-id="a9911-139">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span><span class="sxs-lookup"><span data-stu-id="a9911-139">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span></span>

## <span data-ttu-id="a9911-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a9911-140">NOTES</span></span>

<span data-ttu-id="a9911-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="a9911-141">ALIASES</span></span>

<span data-ttu-id="a9911-142">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="a9911-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a9911-143">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a9911-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a9911-144">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a9911-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a9911-145">INPUTOBJECT <IAdDomainServicesIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="a9911-145">INPUTOBJECT <IAdDomainServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a9911-146">`[DomainServiceName <String>]`: Der Name des Domänendiensts.</span><span class="sxs-lookup"><span data-stu-id="a9911-146">`[DomainServiceName <String>]`: The name of the domain service.</span></span>
  - <span data-ttu-id="a9911-147">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="a9911-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a9911-148">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe im Abonnement des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="a9911-148">`[ResourceGroupName <String>]`: The name of the resource group within the user's subscription.</span></span> <span data-ttu-id="a9911-149">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="a9911-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="a9911-150">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen das Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="a9911-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="a9911-151">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="a9911-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a9911-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a9911-152">RELATED LINKS</span></span>

