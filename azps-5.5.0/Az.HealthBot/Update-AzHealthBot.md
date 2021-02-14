---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthbot/update-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Update-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Update-AzHealthBot.md
ms.openlocfilehash: b14ed0d682a6ba74eb557aae79a4fe151e952a73
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167417"
---
# <span data-ttu-id="08df1-101">Update-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="08df1-101">Update-AzHealthBot</span></span>

## <span data-ttu-id="08df1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08df1-102">SYNOPSIS</span></span>
<span data-ttu-id="08df1-103">Patchen Sie einen HealthBot.</span><span class="sxs-lookup"><span data-stu-id="08df1-103">Patch a HealthBot.</span></span>

## <span data-ttu-id="08df1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="08df1-104">SYNTAX</span></span>

### <span data-ttu-id="08df1-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="08df1-105">UpdateExpanded (Default)</span></span>
```
Update-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Sku <SkuName>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="08df1-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="08df1-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzHealthBot -InputObject <IHealthBotIdentity> [-Sku <SkuName>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="08df1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08df1-107">DESCRIPTION</span></span>
<span data-ttu-id="08df1-108">Patchen Sie einen HealthBot.</span><span class="sxs-lookup"><span data-stu-id="08df1-108">Patch a HealthBot.</span></span>

## <span data-ttu-id="08df1-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="08df1-109">EXAMPLES</span></span>

### <span data-ttu-id="08df1-110">Beispiel 1: Aktualisieren von HealthBot nach Ressourcengruppenname und Name</span><span class="sxs-lookup"><span data-stu-id="08df1-110">Example 1: update HealthBot by Resourcegroupname and Name</span></span>
```powershell
PS C:\> update-AzHealthBot -ResourceGroupName youriTest -Name yourihealthbot -Sku S1

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------ ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/30 6:12:33       test@microsoft.com    User                         Microsoft.HealthBot/health…
```

<span data-ttu-id="08df1-111">Aktualisieren von HealthBot nach Ressourcengruppenname und Name</span><span class="sxs-lookup"><span data-stu-id="08df1-111">update HealthBot by Resourcegroupname and Name</span></span>

### <span data-ttu-id="08df1-112">Beispiel 2: Aktualisieren von HealthBot von InputObject</span><span class="sxs-lookup"><span data-stu-id="08df1-112">Example 2: update HealthBot by InputObject</span></span>
```powershell
PS C:\> $getHealth = Get-AzHealthBot -ResourceGroupName youriTest -Name yourihealthbot
Update-AzHealthBot -InputObject $getHealth -Sku F0

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------ ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/30 6:12:33       test@microsoft.com    User                         Microsoft.HealthBot/health…
```

<span data-ttu-id="08df1-113">Aktualisieren von HealthBot von InputObject</span><span class="sxs-lookup"><span data-stu-id="08df1-113">update HealthBot by InputObject</span></span>

## <span data-ttu-id="08df1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08df1-114">PARAMETERS</span></span>

### <span data-ttu-id="08df1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08df1-115">-DefaultProfile</span></span>
<span data-ttu-id="08df1-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08df1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08df1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08df1-117">-InputObject</span></span>
<span data-ttu-id="08df1-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="08df1-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08df1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="08df1-119">-Name</span></span>
<span data-ttu-id="08df1-120">Der Name der Bot-Ressource.</span><span class="sxs-lookup"><span data-stu-id="08df1-120">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08df1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08df1-121">-ResourceGroupName</span></span>
<span data-ttu-id="08df1-122">Der Name der Ressourcengruppe "Bot" im Benutzerabonnement.</span><span class="sxs-lookup"><span data-stu-id="08df1-122">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="08df1-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="08df1-123">-Sku</span></span>
<span data-ttu-id="08df1-124">Der Name der HealthBot-SKU</span><span class="sxs-lookup"><span data-stu-id="08df1-124">The name of the HealthBot SKU</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08df1-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="08df1-125">-SubscriptionId</span></span>
<span data-ttu-id="08df1-126">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="08df1-126">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08df1-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="08df1-127">-Tag</span></span>
<span data-ttu-id="08df1-128">Tags für einen HealthBot.</span><span class="sxs-lookup"><span data-stu-id="08df1-128">Tags for a HealthBot.</span></span>

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

### <span data-ttu-id="08df1-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="08df1-129">-Confirm</span></span>
<span data-ttu-id="08df1-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="08df1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08df1-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="08df1-131">-WhatIf</span></span>
<span data-ttu-id="08df1-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="08df1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08df1-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="08df1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08df1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08df1-134">CommonParameters</span></span>
<span data-ttu-id="08df1-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08df1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08df1-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08df1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08df1-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="08df1-137">INPUTS</span></span>

### <span data-ttu-id="08df1-138">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="08df1-138">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="08df1-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="08df1-139">OUTPUTS</span></span>

### <span data-ttu-id="08df1-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="08df1-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="08df1-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="08df1-141">NOTES</span></span>

<span data-ttu-id="08df1-142">ALIASE</span><span class="sxs-lookup"><span data-stu-id="08df1-142">ALIASES</span></span>

<span data-ttu-id="08df1-143">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="08df1-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="08df1-144">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="08df1-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="08df1-145">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="08df1-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="08df1-146">INPUTOBJECT <IHealthBotIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="08df1-146">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="08df1-147">`[BotName <String>]`: Der Name der Bot-Ressource.</span><span class="sxs-lookup"><span data-stu-id="08df1-147">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="08df1-148">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="08df1-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="08df1-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe "Bot" im Benutzerabonnement.</span><span class="sxs-lookup"><span data-stu-id="08df1-149">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="08df1-150">`[SubscriptionId <String>]`: Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="08df1-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="08df1-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="08df1-151">RELATED LINKS</span></span>

