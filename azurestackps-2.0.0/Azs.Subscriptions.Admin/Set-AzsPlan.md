---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsplan
schema: 2.0.0
ms.openlocfilehash: 2e78b28705b625836d9020c5ddf1652f4bdc7a7d
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/22/2020
ms.locfileid: "94005306"
---
# <span data-ttu-id="5955d-101">Set-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="5955d-101">Set-AzsPlan</span></span>

## <span data-ttu-id="5955d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5955d-102">SYNOPSIS</span></span>
<span data-ttu-id="5955d-103">Erstellen oder aktualisieren Sie den Plan.</span><span class="sxs-lookup"><span data-stu-id="5955d-103">Create or update the plan.</span></span>

## <span data-ttu-id="5955d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5955d-104">SYNTAX</span></span>

### <span data-ttu-id="5955d-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="5955d-105">UpdateExpanded (Default)</span></span>
```
Set-AzsPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Description <String>]
 [-DisplayName <String>] [-ExternalReferenceId <String>] [-Location <String>] [-PropertiesName <String>]
 [-QuotaIds <String[]>] [-SkuIds <String[]>] [-SubscriptionCount <Int32>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5955d-106">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="5955d-106">Update</span></span>
```
Set-AzsPlan -PlanDefinition <IPlan> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5955d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5955d-107">DESCRIPTION</span></span>
<span data-ttu-id="5955d-108">Erstellen oder aktualisieren Sie den Plan.</span><span class="sxs-lookup"><span data-stu-id="5955d-108">Create or update the plan.</span></span>

## <span data-ttu-id="5955d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5955d-109">EXAMPLES</span></span>

### <span data-ttu-id="5955d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5955d-110">Example 1</span></span>
```powershell
PS C:\> $Plan = Get-AzsPlan | Select-Object -First 1
$Plan.Description = 'update plan'
$Plan | Set-AzsPlan

Description         : update plan
DisplayName         : DRPTestPlan5056-test-test-test
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/plans/DRPTestPlan5056
Location            : redmond
Name                : DRPTestPlan5056
PropertiesName      : DRPTestPlan5056
QuotaIds            : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Storage.Admin/locations/redmond/quotas/Default Quota, 
                      /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Compute.Admin/locations/redmond/quotas/Default Quota}
SkuIds              : 
SubscriptionCount   : 5
Tags                : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                : Microsoft.Subscriptions.Admin/plans
```

<span data-ttu-id="5955d-111">Aktualisiert den angegebenen Plan</span><span class="sxs-lookup"><span data-stu-id="5955d-111">Updates the specified plan</span></span>

## <span data-ttu-id="5955d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5955d-112">PARAMETERS</span></span>

### <span data-ttu-id="5955d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5955d-113">-DefaultProfile</span></span>
<span data-ttu-id="5955d-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5955d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5955d-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5955d-115">-Description</span></span>
<span data-ttu-id="5955d-116">Beschreibung des Plans</span><span class="sxs-lookup"><span data-stu-id="5955d-116">Description of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5955d-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5955d-117">-DisplayName</span></span>
<span data-ttu-id="5955d-118">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="5955d-118">Display name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5955d-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="5955d-119">-ExternalReferenceId</span></span>
<span data-ttu-id="5955d-120">Externer Verweisbezeichner.</span><span class="sxs-lookup"><span data-stu-id="5955d-120">External reference identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5955d-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="5955d-121">-Location</span></span>
<span data-ttu-id="5955d-122">Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="5955d-122">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5955d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5955d-123">-Name</span></span>
<span data-ttu-id="5955d-124">Der Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="5955d-124">Name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5955d-125">-PlanDefinition</span><span class="sxs-lookup"><span data-stu-id="5955d-125">-PlanDefinition</span></span>
<span data-ttu-id="5955d-126">Ein Plan steht für ein Paket von Kontingenten und Funktionen, die Mandanten angeboten werden.</span><span class="sxs-lookup"><span data-stu-id="5955d-126">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="5955d-127">Ein Mandant kann diesen Plan über ein Angebot erwerben, um seinen Zugriff auf die zugrunde liegenden Cloud-Services zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5955d-127">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>
<span data-ttu-id="5955d-128">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für PLANDEFINITION-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="5955d-128">To construct, see NOTES section for PLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="5955d-129">-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="5955d-129">-PropertiesName</span></span>
<span data-ttu-id="5955d-130">Der Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="5955d-130">Name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5955d-131">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="5955d-131">-QuotaIds</span></span>
<span data-ttu-id="5955d-132">Kontingent Bezeichner im Plan.</span><span class="sxs-lookup"><span data-stu-id="5955d-132">Quota identifiers under the plan.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5955d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5955d-133">-ResourceGroupName</span></span>
<span data-ttu-id="5955d-134">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="5955d-134">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5955d-135">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="5955d-135">-SkuIds</span></span>
<span data-ttu-id="5955d-136">SKU-IDs.</span><span class="sxs-lookup"><span data-stu-id="5955d-136">SKU identifiers.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5955d-137">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="5955d-137">-SubscriptionCount</span></span>
<span data-ttu-id="5955d-138">Anzahl der Abonnements</span><span class="sxs-lookup"><span data-stu-id="5955d-138">Subscription count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5955d-139">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="5955d-139">-SubscriptionId</span></span>
<span data-ttu-id="5955d-140">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="5955d-140">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5955d-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5955d-141">-Confirm</span></span>
<span data-ttu-id="5955d-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5955d-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5955d-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5955d-143">-WhatIf</span></span>
<span data-ttu-id="5955d-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5955d-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5955d-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5955d-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5955d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5955d-146">CommonParameters</span></span>
<span data-ttu-id="5955d-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5955d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5955d-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5955d-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5955d-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5955d-149">INPUTS</span></span>

### <span data-ttu-id="5955d-150">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IPlan</span><span class="sxs-lookup"><span data-stu-id="5955d-150">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

## <span data-ttu-id="5955d-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5955d-151">OUTPUTS</span></span>

### <span data-ttu-id="5955d-152">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IPlan</span><span class="sxs-lookup"><span data-stu-id="5955d-152">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

<span data-ttu-id="5955d-153">Aliase</span><span class="sxs-lookup"><span data-stu-id="5955d-153">ALIASES</span></span>

## <span data-ttu-id="5955d-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="5955d-154">NOTES</span></span>

<span data-ttu-id="5955d-155">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5955d-155">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5955d-156">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="5955d-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5955d-157">PLANDEFINITION <IPlan> : ein Plan stellt ein Paket von Kontingenten und Funktionen dar, die Mandanten angeboten werden.</span><span class="sxs-lookup"><span data-stu-id="5955d-157">PLANDEFINITION <IPlan>: A plan represents a package of quotas and capabilities that are offered tenants.</span></span> <span data-ttu-id="5955d-158">Ein Mandant kann diesen Plan über ein Angebot erwerben, um seinen Zugriff auf die zugrunde liegenden Cloud-Services zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5955d-158">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>
  - <span data-ttu-id="5955d-159">`[Location <String>]`: Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="5955d-159">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="5955d-160">`[Description <String>]`: Beschreibung des Plans.</span><span class="sxs-lookup"><span data-stu-id="5955d-160">`[Description <String>]`: Description of the plan.</span></span>
  - <span data-ttu-id="5955d-161">`[DisplayName <String>]`: Anzeigename.</span><span class="sxs-lookup"><span data-stu-id="5955d-161">`[DisplayName <String>]`: Display name.</span></span>
  - <span data-ttu-id="5955d-162">`[ExternalReferenceId <String>]`: Externer Verweisbezeichner.</span><span class="sxs-lookup"><span data-stu-id="5955d-162">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="5955d-163">`[PropertiesName <String>]`: Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="5955d-163">`[PropertiesName <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="5955d-164">`[QuotaIds <String[]>]`: Kontingent-IDs unter dem Plan.</span><span class="sxs-lookup"><span data-stu-id="5955d-164">`[QuotaIds <String[]>]`: Quota identifiers under the plan.</span></span>
  - <span data-ttu-id="5955d-165">`[SkuIds <String[]>]`: SKU-IDs.</span><span class="sxs-lookup"><span data-stu-id="5955d-165">`[SkuIds <String[]>]`: SKU identifiers.</span></span>
  - <span data-ttu-id="5955d-166">`[SubscriptionCount <Int32?>]`: Anzahl der Abonnements.</span><span class="sxs-lookup"><span data-stu-id="5955d-166">`[SubscriptionCount <Int32?>]`: Subscription count.</span></span>

## <span data-ttu-id="5955d-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5955d-167">RELATED LINKS</span></span>

