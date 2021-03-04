---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/new-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentOrganization.md
ms.openlocfilehash: 546b4e56f2a932a6d7f17bda8484db8cd1c3c593
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948899"
---
# <span data-ttu-id="b7120-101">New-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="b7120-101">New-AzConfluentOrganization</span></span>

## <span data-ttu-id="b7120-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7120-102">SYNOPSIS</span></span>
<span data-ttu-id="b7120-103">Erstellen einer Organisationsressource</span><span class="sxs-lookup"><span data-stu-id="b7120-103">Create Organization resource</span></span>

## <span data-ttu-id="b7120-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b7120-104">SYNTAX</span></span>

```
New-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Location <String>] [-OfferDetailId <String>] [-OfferDetailPlanId <String>] [-OfferDetailPlanName <String>]
 [-OfferDetailPublisherId <String>] [-OfferDetailStatus <SaaSOfferStatus>] [-OfferDetailTermUnit <String>]
 [-Tag <Hashtable>] [-UserDetailEmailAddress <String>] [-UserDetailFirstName <String>]
 [-UserDetailLastName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="b7120-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b7120-105">DESCRIPTION</span></span>
<span data-ttu-id="b7120-106">Erstellen einer Organisationsressource</span><span class="sxs-lookup"><span data-stu-id="b7120-106">Create Organization resource</span></span>

## <span data-ttu-id="b7120-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b7120-107">EXAMPLES</span></span>

### <span data-ttu-id="b7120-108">Beispiel 1: Erstellen einer kongenenten Organisation</span><span class="sxs-lookup"><span data-stu-id="b7120-108">Example 1: Create a confluent organization</span></span>
```powershell
PS C:\> New-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh -Location eastus -OfferDetailId "confluent-cloud-azure-prod" -OfferDetailPlanId "confluent-cloud-azure-payg-prod" -OfferDetailPlanName "Confluent Cloud - Pay as you Go" -OfferDetailPublisherId "confluentinc" -OfferDetailTermUnit "P1M" -UserDetailEmailAddress "xxxx@microsoft.com"

Location Name                   Type
-------- ----                   ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="b7120-109">Mit diesem Befehl wird eine konfluente Organisation erstellt.</span><span class="sxs-lookup"><span data-stu-id="b7120-109">This command creates a confluent organization.</span></span>

## <span data-ttu-id="b7120-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b7120-110">PARAMETERS</span></span>

### <span data-ttu-id="b7120-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7120-111">-AsJob</span></span>
<span data-ttu-id="b7120-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="b7120-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7120-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7120-113">-DefaultProfile</span></span>
<span data-ttu-id="b7120-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b7120-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7120-115">-Location</span><span class="sxs-lookup"><span data-stu-id="b7120-115">-Location</span></span>
<span data-ttu-id="b7120-116">Speicherort der Organisationsressource</span><span class="sxs-lookup"><span data-stu-id="b7120-116">Location of Organization resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7120-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b7120-117">-Name</span></span>
<span data-ttu-id="b7120-118">Ressourcenname der Organisation</span><span class="sxs-lookup"><span data-stu-id="b7120-118">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7120-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b7120-119">-NoWait</span></span>
<span data-ttu-id="b7120-120">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="b7120-120">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7120-121">-OfferDetailId</span><span class="sxs-lookup"><span data-stu-id="b7120-121">-OfferDetailId</span></span>
<span data-ttu-id="b7120-122">Angebots-ID</span><span class="sxs-lookup"><span data-stu-id="b7120-122">Offer Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7120-123">-OfferDetailPlanId</span><span class="sxs-lookup"><span data-stu-id="b7120-123">-OfferDetailPlanId</span></span>
<span data-ttu-id="b7120-124">Angebotsplan-ID</span><span class="sxs-lookup"><span data-stu-id="b7120-124">Offer Plan Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7120-125">-OfferDetailPlanName</span><span class="sxs-lookup"><span data-stu-id="b7120-125">-OfferDetailPlanName</span></span>
<span data-ttu-id="b7120-126">Name des Angebotsplans</span><span class="sxs-lookup"><span data-stu-id="b7120-126">Offer Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7120-127">-OfferDetailPublisherId</span><span class="sxs-lookup"><span data-stu-id="b7120-127">-OfferDetailPublisherId</span></span>
<span data-ttu-id="b7120-128">Publisher-ID</span><span class="sxs-lookup"><span data-stu-id="b7120-128">Publisher Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7120-129">-OfferDetailStatus</span><span class="sxs-lookup"><span data-stu-id="b7120-129">-OfferDetailStatus</span></span>
<span data-ttu-id="b7120-130">Status des SaaS-Angebots</span><span class="sxs-lookup"><span data-stu-id="b7120-130">SaaS Offer Status</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Support.SaaSOfferStatus
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7120-131">-OfferDetailTermUnit</span><span class="sxs-lookup"><span data-stu-id="b7120-131">-OfferDetailTermUnit</span></span>
<span data-ttu-id="b7120-132">Angebotsplan-Ausdruckseinheit</span><span class="sxs-lookup"><span data-stu-id="b7120-132">Offer Plan Term unit</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7120-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7120-133">-ResourceGroupName</span></span>
<span data-ttu-id="b7120-134">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="b7120-134">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7120-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b7120-135">-SubscriptionId</span></span>
<span data-ttu-id="b7120-136">Microsoft Azure-Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="b7120-136">Microsoft Azure subscription id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7120-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="b7120-137">-Tag</span></span>
<span data-ttu-id="b7120-138">Ressourcentags der Organisation</span><span class="sxs-lookup"><span data-stu-id="b7120-138">Organization resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7120-139">-UserDetailEmailAddress</span><span class="sxs-lookup"><span data-stu-id="b7120-139">-UserDetailEmailAddress</span></span>
<span data-ttu-id="b7120-140">E-Mail-Adresse</span><span class="sxs-lookup"><span data-stu-id="b7120-140">Email address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7120-141">-UserDetailFirstName</span><span class="sxs-lookup"><span data-stu-id="b7120-141">-UserDetailFirstName</span></span>
<span data-ttu-id="b7120-142">Vorname</span><span class="sxs-lookup"><span data-stu-id="b7120-142">First name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7120-143">-UserDetailLastName</span><span class="sxs-lookup"><span data-stu-id="b7120-143">-UserDetailLastName</span></span>
<span data-ttu-id="b7120-144">Nachname</span><span class="sxs-lookup"><span data-stu-id="b7120-144">Last name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7120-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b7120-145">-Confirm</span></span>
<span data-ttu-id="b7120-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b7120-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7120-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7120-147">-WhatIf</span></span>
<span data-ttu-id="b7120-148">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b7120-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7120-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b7120-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7120-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7120-150">CommonParameters</span></span>
<span data-ttu-id="b7120-151">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7120-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7120-152">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7120-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7120-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b7120-153">INPUTS</span></span>

## <span data-ttu-id="b7120-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b7120-154">OUTPUTS</span></span>

### <span data-ttu-id="b7120-155">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span><span class="sxs-lookup"><span data-stu-id="b7120-155">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span></span>

## <span data-ttu-id="b7120-156">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b7120-156">NOTES</span></span>

<span data-ttu-id="b7120-157">ALIASE</span><span class="sxs-lookup"><span data-stu-id="b7120-157">ALIASES</span></span>

## <span data-ttu-id="b7120-158">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b7120-158">RELATED LINKS</span></span>

