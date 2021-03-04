---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.addomainservices/get-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Get-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Get-AzADDomainService.md
ms.openlocfilehash: 19ae45bf50c9ae54075e46a8db8fc66cc08e488a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942040"
---
# <span data-ttu-id="18b5a-101">Get-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="18b5a-101">Get-AzADDomainService</span></span>

## <span data-ttu-id="18b5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="18b5a-103">Der Vorgang "Domänendienst abrufen" ruft eine json-Darstellung des Domänendiensts ab.</span><span class="sxs-lookup"><span data-stu-id="18b5a-103">The Get Domain Service operation retrieves a json representation of the Domain Service.</span></span>

## <span data-ttu-id="18b5a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18b5a-104">SYNTAX</span></span>

### <span data-ttu-id="18b5a-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="18b5a-105">List (Default)</span></span>
```
Get-AzADDomainService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="18b5a-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="18b5a-106">Get</span></span>
```
Get-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="18b5a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="18b5a-107">GetViaIdentity</span></span>
```
Get-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="18b5a-108">Liste1</span><span class="sxs-lookup"><span data-stu-id="18b5a-108">List1</span></span>
```
Get-AzADDomainService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="18b5a-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="18b5a-109">DESCRIPTION</span></span>
<span data-ttu-id="18b5a-110">Der Vorgang "Domänendienst abrufen" ruft eine json-Darstellung des Domänendiensts ab.</span><span class="sxs-lookup"><span data-stu-id="18b5a-110">The Get Domain Service operation retrieves a json representation of the Domain Service.</span></span>

## <span data-ttu-id="18b5a-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="18b5a-111">EXAMPLES</span></span>

### <span data-ttu-id="18b5a-112">Beispiel 1: Standardmäßig alle ADDomainService-Informationen</span><span class="sxs-lookup"><span data-stu-id="18b5a-112">Example 1: Get All ADDomainService By default</span></span>
```powershell
PS C:\> Get-AzADDomainService

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="18b5a-113">Alle ADDomainService standardmäßig erhalten</span><span class="sxs-lookup"><span data-stu-id="18b5a-113">Get All ADDomainService By default</span></span>

### <span data-ttu-id="18b5a-114">Beispiel 2: Anzeigen von ADDomainService nach Ressourcengruppe und Name</span><span class="sxs-lookup"><span data-stu-id="18b5a-114">Example 2: Get ADDomainService By ResourceGroup and name</span></span>
```powershell
PS C:\> Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="18b5a-115">Anzeigen von ADDomainService nach Ressourcengruppe und Name</span><span class="sxs-lookup"><span data-stu-id="18b5a-115">Get ADDomainService By ResourceGroup and name</span></span>

### <span data-ttu-id="18b5a-116">Beispiel 3: Alle ADDomainService von ResourceGroup erhalten</span><span class="sxs-lookup"><span data-stu-id="18b5a-116">Example 3: Get all ADDomainService By ResourceGroup</span></span>
```powershell
PS C:\> Get-AzADDomainService -ResourceGroupName youriADdomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="18b5a-117">Alle ADDomainService By ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="18b5a-117">Get all ADDomainService By ResourceGroup</span></span>

### <span data-ttu-id="18b5a-118">Beispiel 4: Anzeigen von ADDomainService by InputObject</span><span class="sxs-lookup"><span data-stu-id="18b5a-118">Example 4: Get ADDomainService By InputObject</span></span>
```powershell
PS C:\> $getAzAddomain = Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain
Get-AzADDomainService -InputObject $getAzAddomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="18b5a-119">Anzeigen von ADDomainService by InputObject</span><span class="sxs-lookup"><span data-stu-id="18b5a-119">Get ADDomainService By InputObject</span></span>

## <span data-ttu-id="18b5a-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="18b5a-120">PARAMETERS</span></span>

### <span data-ttu-id="18b5a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18b5a-121">-DefaultProfile</span></span>
<span data-ttu-id="18b5a-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="18b5a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18b5a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18b5a-123">-InputObject</span></span>
<span data-ttu-id="18b5a-124">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="18b5a-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="18b5a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="18b5a-125">-Name</span></span>
<span data-ttu-id="18b5a-126">Der Name des Domänendiensts.</span><span class="sxs-lookup"><span data-stu-id="18b5a-126">The name of the domain service.</span></span>

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

### <span data-ttu-id="18b5a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18b5a-127">-ResourceGroupName</span></span>
<span data-ttu-id="18b5a-128">Der Name der Ressourcengruppe im Abonnement des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="18b5a-128">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="18b5a-129">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="18b5a-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="18b5a-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="18b5a-130">-SubscriptionId</span></span>
<span data-ttu-id="18b5a-131">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="18b5a-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="18b5a-132">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="18b5a-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="18b5a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18b5a-133">CommonParameters</span></span>
<span data-ttu-id="18b5a-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18b5a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18b5a-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18b5a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18b5a-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="18b5a-136">INPUTS</span></span>

### <span data-ttu-id="18b5a-137">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="18b5a-137">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span></span>

## <span data-ttu-id="18b5a-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="18b5a-138">OUTPUTS</span></span>

### <span data-ttu-id="18b5a-139">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span><span class="sxs-lookup"><span data-stu-id="18b5a-139">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span></span>

## <span data-ttu-id="18b5a-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="18b5a-140">NOTES</span></span>

<span data-ttu-id="18b5a-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="18b5a-141">ALIASES</span></span>

<span data-ttu-id="18b5a-142">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="18b5a-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="18b5a-143">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="18b5a-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="18b5a-144">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="18b5a-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="18b5a-145">INPUTOBJECT <IAdDomainServicesIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="18b5a-145">INPUTOBJECT <IAdDomainServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="18b5a-146">`[DomainServiceName <String>]`: Der Name des Domänendiensts.</span><span class="sxs-lookup"><span data-stu-id="18b5a-146">`[DomainServiceName <String>]`: The name of the domain service.</span></span>
  - <span data-ttu-id="18b5a-147">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="18b5a-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="18b5a-148">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe im Abonnement des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="18b5a-148">`[ResourceGroupName <String>]`: The name of the resource group within the user's subscription.</span></span> <span data-ttu-id="18b5a-149">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="18b5a-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="18b5a-150">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="18b5a-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="18b5a-151">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="18b5a-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="18b5a-152">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="18b5a-152">RELATED LINKS</span></span>

