---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/get-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentOrganization.md
ms.openlocfilehash: dcac6e7ce7e4c8daed2e2f8b43c44c2da82acd93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948912"
---
# <span data-ttu-id="3f9b4-101">Get-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="3f9b4-101">Get-AzConfluentOrganization</span></span>

## <span data-ttu-id="3f9b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f9b4-102">SYNOPSIS</span></span>
<span data-ttu-id="3f9b4-103">Hier erhalten Sie die Eigenschaften einer bestimmten Organisationsressource.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-103">Get the properties of a specific Organization resource.</span></span>

## <span data-ttu-id="3f9b4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f9b4-104">SYNTAX</span></span>

### <span data-ttu-id="3f9b4-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="3f9b4-105">List (Default)</span></span>
```
Get-AzConfluentOrganization [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3f9b4-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="3f9b4-106">Get</span></span>
```
Get-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3f9b4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3f9b4-107">GetViaIdentity</span></span>
```
Get-AzConfluentOrganization -InputObject <IConfluentIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f9b4-108">Liste1</span><span class="sxs-lookup"><span data-stu-id="3f9b4-108">List1</span></span>
```
Get-AzConfluentOrganization -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3f9b4-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f9b4-109">DESCRIPTION</span></span>
<span data-ttu-id="3f9b4-110">Hier erhalten Sie die Eigenschaften einer bestimmten Organisationsressource.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-110">Get the properties of a specific Organization resource.</span></span>

## <span data-ttu-id="3f9b4-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3f9b4-111">EXAMPLES</span></span>

### <span data-ttu-id="3f9b4-112">Beispiel 1: Auflisten aller kongenenten Organisationen unter einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="3f9b4-112">Example 1: List all confluent organizations under a subscription</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization

Location      Name                     Type
--------      ----                     ----
westus2       RegionTestWestUS2        Microsoft.Confluent/organizations
westus2       RohitWUS2                Microsoft.Confluent/organizations
westus2       Rohit-Secret             Microsoft.Confluent/organizations
westus2       Rohit-Secret-2           Microsoft.Confluent/organizations
westus2       Rohit-Secret-WUS2-0      Microsoft.Confluent/organizations
westus2       RohitWus200              Microsoft.Confluent/organizations
westus2       RohitWUS300              Microsoft.Confluent/organizations
westus2       WestUS2-SSOTest          Microsoft.Confluent/organizations
westus2       dri-01-02-postman-stable Microsoft.Confluent/organizations
westus2       dri-02-02                Microsoft.Confluent/organizations
westcentralus RohitWCUS88              Microsoft.Confluent/organizations
```

<span data-ttu-id="3f9b4-113">Mit diesem Befehl werden alle kongenenten Organisationen unter einem Abonnement aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-113">This command lists all confluent organizations under a subscription.</span></span>

### <span data-ttu-id="3f9b4-114">Beispiel 2: Auflisten aller kongenenten Organisationen unter einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="3f9b4-114">Example 2: List all confluent organizations under a resource group</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization -ResourceGroupName azure-rg-test

Location    Name          Type
--------    ----          ----
eastus2euap ppe-metrics-2 Microsoft.Confluent/organizations
```

<span data-ttu-id="3f9b4-115">Mit diesem Befehl werden alle sich zusammenfeinden Organisationen unter einer Ressourcengruppe aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-115">This command lists all confluent organizations under a resource group.</span></span>

### <span data-ttu-id="3f9b4-116">Beispiel 3: Erhalten einer kongenenten Organisation nach Name</span><span class="sxs-lookup"><span data-stu-id="3f9b4-116">Example 3: Get a confluent organization by name</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-01-portal

Location Name                   Type
-------- ----                   ----
eastus   confluentorg-01-portal Microsoft.Confluent/organizations
```

<span data-ttu-id="3f9b4-117">Dieser Befehl ruft eine konfluente Organisation nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-117">This command gets a confluent organization by name.</span></span>

### <span data-ttu-id="3f9b4-118">Beispiel 4: Erhalten einer kongenenten Organisation per Pipeline</span><span class="sxs-lookup"><span data-stu-id="3f9b4-118">Example 4: Get a confluent organization by pipeline</span></span>
```powershell
PS C:\> New-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh -Location eastus -OfferDetailId "confluent-cloud-azure-prod" -OfferDetailPlanId "confluent-cloud-azure-payg-prod" -OfferDetailPlanName "Confluent Cloud - Pay as you Go" -OfferDetailPublisherId "confluentinc" -OfferDetailTermUnit "P1M" | Get-AzConfluentOrganization

Location Name                   Type
-------- ----                   ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="3f9b4-119">Dieser Befehl ruft eine kongente Organisation per Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-119">This command gets a confluent organization by pipeline.</span></span>

## <span data-ttu-id="3f9b4-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3f9b4-120">PARAMETERS</span></span>

### <span data-ttu-id="3f9b4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f9b4-121">-DefaultProfile</span></span>
<span data-ttu-id="3f9b4-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f9b4-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f9b4-123">-InputObject</span></span>
<span data-ttu-id="3f9b4-124">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f9b4-125">-Name</span><span class="sxs-lookup"><span data-stu-id="3f9b4-125">-Name</span></span>
<span data-ttu-id="3f9b4-126">Ressourcenname der Organisation</span><span class="sxs-lookup"><span data-stu-id="3f9b4-126">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f9b4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f9b4-127">-ResourceGroupName</span></span>
<span data-ttu-id="3f9b4-128">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="3f9b4-128">Resource group name</span></span>

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

### <span data-ttu-id="3f9b4-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3f9b4-129">-SubscriptionId</span></span>
<span data-ttu-id="3f9b4-130">Microsoft Azure-Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="3f9b4-130">Microsoft Azure subscription id</span></span>

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

### <span data-ttu-id="3f9b4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f9b4-131">CommonParameters</span></span>
<span data-ttu-id="3f9b4-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f9b4-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f9b4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f9b4-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3f9b4-134">INPUTS</span></span>

### <span data-ttu-id="3f9b4-135">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span><span class="sxs-lookup"><span data-stu-id="3f9b4-135">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span></span>

## <span data-ttu-id="3f9b4-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3f9b4-136">OUTPUTS</span></span>

### <span data-ttu-id="3f9b4-137">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span><span class="sxs-lookup"><span data-stu-id="3f9b4-137">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span></span>

## <span data-ttu-id="3f9b4-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3f9b4-138">NOTES</span></span>

<span data-ttu-id="3f9b4-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="3f9b4-139">ALIASES</span></span>

<span data-ttu-id="3f9b4-140">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="3f9b4-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3f9b4-141">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3f9b4-142">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3f9b4-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3f9b4-143">INPUTOBJECT <IConfluentIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="3f9b4-143">INPUTOBJECT <IConfluentIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3f9b4-144">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="3f9b4-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3f9b4-145">`[OrganizationName <String>]`: Ressourcenname der Organisation</span><span class="sxs-lookup"><span data-stu-id="3f9b4-145">`[OrganizationName <String>]`: Organization resource name</span></span>
  - <span data-ttu-id="3f9b4-146">`[ResourceGroupName <String>]`: Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="3f9b4-146">`[ResourceGroupName <String>]`: Resource group name</span></span>
  - <span data-ttu-id="3f9b4-147">`[SubscriptionId <String>]`: Microsoft Azure-Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="3f9b4-147">`[SubscriptionId <String>]`: Microsoft Azure subscription id</span></span>

## <span data-ttu-id="3f9b4-148">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3f9b4-148">RELATED LINKS</span></span>

