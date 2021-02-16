---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/update-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Update-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Update-AzBotService.md
ms.openlocfilehash: f7dd02a214fa32223e052c1999329699f1c653e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168073"
---
# <span data-ttu-id="02054-101">Update-AzBotService</span><span class="sxs-lookup"><span data-stu-id="02054-101">Update-AzBotService</span></span>

## <span data-ttu-id="02054-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02054-102">SYNOPSIS</span></span>
<span data-ttu-id="02054-103">Aktualisiert einen Botdienst</span><span class="sxs-lookup"><span data-stu-id="02054-103">Updates a Bot Service</span></span>

## <span data-ttu-id="02054-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02054-104">SYNTAX</span></span>

### <span data-ttu-id="02054-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="02054-105">UpdateExpanded (Default)</span></span>
```
Update-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-DeveloperAppInsightKey <String>] [-DeveloperAppInsightsApiKey <String>]
 [-DeveloperAppInsightsApplicationId <String>] [-DisplayName <String>] [-Endpoint <String>] [-Etag <String>]
 [-IconUrl <String>] [-Kind <Kind>] [-Location <String>] [-LuisAppId <String[]>] [-LuisKey <String>]
 [-MsaAppId <String>] [-SkuName <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="02054-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="02054-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBotService -InputObject <IBotServiceIdentity> [-Description <String>]
 [-DeveloperAppInsightKey <String>] [-DeveloperAppInsightsApiKey <String>]
 [-DeveloperAppInsightsApplicationId <String>] [-DisplayName <String>] [-Endpoint <String>] [-Etag <String>]
 [-IconUrl <String>] [-Kind <Kind>] [-Location <String>] [-LuisAppId <String[]>] [-LuisKey <String>]
 [-MsaAppId <String>] [-SkuName <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="02054-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="02054-107">DESCRIPTION</span></span>
<span data-ttu-id="02054-108">Aktualisiert einen Botdienst</span><span class="sxs-lookup"><span data-stu-id="02054-108">Updates a Bot Service</span></span>

## <span data-ttu-id="02054-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="02054-109">EXAMPLES</span></span>

### <span data-ttu-id="02054-110">Beispiel 1: Aktualisieren des Bots nach Name und ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02054-110">Example 1: Update the Bot by Name and ResourceGroupName</span></span>
```powershell
PS C:\> Update-AzBotService -Name 'youri-apptest' -ResourceGroupName 'youriBotTest' -kind Bot

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"0700e71b-0000-1800-0000-5fd73ed80000" Bot  global   youri-apptest                 Microsoft.BotService/botServices
```

<span data-ttu-id="02054-111">Aktualisieren des Bots nach Name und ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02054-111">Update the Bot by Name and ResourceGroupName</span></span>

### <span data-ttu-id="02054-112">Beispiel 2: Aktualisieren des Bots von InputObject</span><span class="sxs-lookup"><span data-stu-id="02054-112">Example 2: Update the Bot by InputObject</span></span>
```powershell
PS C:\> $getAzbot = Get-AzBotService -Name 'youri-apptest' -ResourceGroupName 'youriBotTest'
Update-AzBotService -InputObject $getAzbot -kind sdk

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"07008b1c-0000-1800-0000-5fd73f9e0000" sdk  global   youri-apptest                 Microsoft.BotService/botServices
```

<span data-ttu-id="02054-113">Aktualisieren des Bots von InputObject</span><span class="sxs-lookup"><span data-stu-id="02054-113">Update the Bot by InputObject</span></span>

## <span data-ttu-id="02054-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02054-114">PARAMETERS</span></span>

### <span data-ttu-id="02054-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02054-115">-DefaultProfile</span></span>
<span data-ttu-id="02054-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="02054-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02054-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="02054-117">-Description</span></span>
<span data-ttu-id="02054-118">Beschreibung des Bots</span><span class="sxs-lookup"><span data-stu-id="02054-118">The description of the bot</span></span>

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

### <span data-ttu-id="02054-119">-DeveloperAppInsightKey</span><span class="sxs-lookup"><span data-stu-id="02054-119">-DeveloperAppInsightKey</span></span>
<span data-ttu-id="02054-120">Der Schlüssel "Anwendungserkenntnisse"</span><span class="sxs-lookup"><span data-stu-id="02054-120">The Application Insights key</span></span>

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

### <span data-ttu-id="02054-121">-DeveloperAppInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="02054-121">-DeveloperAppInsightsApiKey</span></span>
<span data-ttu-id="02054-122">Der Application Insights-API-Schlüssel</span><span class="sxs-lookup"><span data-stu-id="02054-122">The Application Insights Api Key</span></span>

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

### <span data-ttu-id="02054-123">-DeveloperAppInsightsApplicationId</span><span class="sxs-lookup"><span data-stu-id="02054-123">-DeveloperAppInsightsApplicationId</span></span>
<span data-ttu-id="02054-124">Anwendungseinblicke-App-ID</span><span class="sxs-lookup"><span data-stu-id="02054-124">The Application Insights App Id</span></span>

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

### <span data-ttu-id="02054-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="02054-125">-DisplayName</span></span>
<span data-ttu-id="02054-126">Der Name des Bots</span><span class="sxs-lookup"><span data-stu-id="02054-126">The Name of the bot</span></span>

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

### <span data-ttu-id="02054-127">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="02054-127">-Endpoint</span></span>
<span data-ttu-id="02054-128">Endpunkt des Bots</span><span class="sxs-lookup"><span data-stu-id="02054-128">The bot's endpoint</span></span>

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

### <span data-ttu-id="02054-129">-Etag</span><span class="sxs-lookup"><span data-stu-id="02054-129">-Etag</span></span>
<span data-ttu-id="02054-130">Entity Tag</span><span class="sxs-lookup"><span data-stu-id="02054-130">Entity Tag</span></span>

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

### <span data-ttu-id="02054-131">-IconUrl</span><span class="sxs-lookup"><span data-stu-id="02054-131">-IconUrl</span></span>
<span data-ttu-id="02054-132">Die Symbol-URL des Bots</span><span class="sxs-lookup"><span data-stu-id="02054-132">The Icon Url of the bot</span></span>

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

### <span data-ttu-id="02054-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02054-133">-InputObject</span></span>
<span data-ttu-id="02054-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="02054-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02054-135">-Kind</span><span class="sxs-lookup"><span data-stu-id="02054-135">-Kind</span></span>
<span data-ttu-id="02054-136">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="02054-136">Required.</span></span>
<span data-ttu-id="02054-137">Ruft die Art der Ressource ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="02054-137">Gets or sets the Kind of the resource.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Support.Kind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02054-138">-Location</span><span class="sxs-lookup"><span data-stu-id="02054-138">-Location</span></span>
<span data-ttu-id="02054-139">Gibt den Speicherort der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="02054-139">Specifies the location of the resource.</span></span>

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

### <span data-ttu-id="02054-140">-LuisAppId</span><span class="sxs-lookup"><span data-stu-id="02054-140">-LuisAppId</span></span>
<span data-ttu-id="02054-141">Sammlung von LUIS-App-Ids</span><span class="sxs-lookup"><span data-stu-id="02054-141">Collection of LUIS App Ids</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02054-142">-LuisKey</span><span class="sxs-lookup"><span data-stu-id="02054-142">-LuisKey</span></span>
<span data-ttu-id="02054-143">Der LUIS-Schlüssel</span><span class="sxs-lookup"><span data-stu-id="02054-143">The LUIS Key</span></span>

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

### <span data-ttu-id="02054-144">-MsaAppId</span><span class="sxs-lookup"><span data-stu-id="02054-144">-MsaAppId</span></span>
<span data-ttu-id="02054-145">Microsoft-App-ID für den Bot</span><span class="sxs-lookup"><span data-stu-id="02054-145">Microsoft App Id for the bot</span></span>

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

### <span data-ttu-id="02054-146">-Name</span><span class="sxs-lookup"><span data-stu-id="02054-146">-Name</span></span>
<span data-ttu-id="02054-147">Der Name der Bot-Ressource.</span><span class="sxs-lookup"><span data-stu-id="02054-147">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="02054-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02054-148">-ResourceGroupName</span></span>
<span data-ttu-id="02054-149">Der Name der Ressourcengruppe "Bot" im Benutzerabonnement.</span><span class="sxs-lookup"><span data-stu-id="02054-149">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="02054-150">-SkuName</span><span class="sxs-lookup"><span data-stu-id="02054-150">-SkuName</span></span>
<span data-ttu-id="02054-151">Der Name der SKU</span><span class="sxs-lookup"><span data-stu-id="02054-151">The sku name</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02054-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="02054-152">-SubscriptionId</span></span>
<span data-ttu-id="02054-153">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="02054-153">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="02054-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="02054-154">-Tag</span></span>
<span data-ttu-id="02054-155">Enthält Ressourcentags, die als Schlüssel-Wert-Paare definiert sind.</span><span class="sxs-lookup"><span data-stu-id="02054-155">Contains resource tags defined as key/value pairs.</span></span>

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

### <span data-ttu-id="02054-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02054-156">-Confirm</span></span>
<span data-ttu-id="02054-157">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="02054-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02054-158">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="02054-158">-WhatIf</span></span>
<span data-ttu-id="02054-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="02054-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02054-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="02054-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02054-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02054-161">CommonParameters</span></span>
<span data-ttu-id="02054-162">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02054-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02054-163">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02054-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02054-164">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="02054-164">INPUTS</span></span>

### <span data-ttu-id="02054-165">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="02054-165">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="02054-166">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="02054-166">OUTPUTS</span></span>

### <span data-ttu-id="02054-167">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="02054-167">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="02054-168">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="02054-168">NOTES</span></span>

<span data-ttu-id="02054-169">ALIASE</span><span class="sxs-lookup"><span data-stu-id="02054-169">ALIASES</span></span>

<span data-ttu-id="02054-170">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="02054-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="02054-171">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="02054-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="02054-172">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="02054-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="02054-173">INPUTOBJECT <IBotServiceIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="02054-173">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="02054-174">`[ChannelName <ChannelName?>]`: Der Name der Kanalressource.</span><span class="sxs-lookup"><span data-stu-id="02054-174">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="02054-175">`[ConnectionName <String>]`: Der Name der Ressource "Bot Service Connection Setting"</span><span class="sxs-lookup"><span data-stu-id="02054-175">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="02054-176">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="02054-176">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="02054-177">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe "Bot" im Benutzerabonnement.</span><span class="sxs-lookup"><span data-stu-id="02054-177">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="02054-178">`[ResourceName <String>]`: Der Name der Bot-Ressource.</span><span class="sxs-lookup"><span data-stu-id="02054-178">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="02054-179">`[SubscriptionId <String>]`: Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="02054-179">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="02054-180">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="02054-180">RELATED LINKS</span></span>

