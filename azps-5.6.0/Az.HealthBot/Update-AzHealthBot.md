---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/powershell/module/az.healthbot/update-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Update-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Update-AzHealthBot.md
ms.openlocfilehash: a0dc204bb6dc1a91031a87fd113c525f282f090e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949219"
---
# <span data-ttu-id="66f55-101">Update-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="66f55-101">Update-AzHealthBot</span></span>

## <span data-ttu-id="66f55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66f55-102">SYNOPSIS</span></span>
<span data-ttu-id="66f55-103">Patchen Sie einen HealthBot.</span><span class="sxs-lookup"><span data-stu-id="66f55-103">Patch a HealthBot.</span></span>

## <span data-ttu-id="66f55-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66f55-104">SYNTAX</span></span>

### <span data-ttu-id="66f55-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="66f55-105">UpdateExpanded (Default)</span></span>
```
Update-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Sku <SkuName>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="66f55-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="66f55-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzHealthBot -InputObject <IHealthBotIdentity> [-Sku <SkuName>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="66f55-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="66f55-107">DESCRIPTION</span></span>
<span data-ttu-id="66f55-108">Patchen Sie einen HealthBot.</span><span class="sxs-lookup"><span data-stu-id="66f55-108">Patch a HealthBot.</span></span>

## <span data-ttu-id="66f55-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="66f55-109">EXAMPLES</span></span>

### <span data-ttu-id="66f55-110">Beispiel 1: Aktualisieren von HealthBot nach Ressourcengruppenname und Name</span><span class="sxs-lookup"><span data-stu-id="66f55-110">Example 1: update HealthBot by Resourcegroupname and Name</span></span>
```powershell
PS C:\> update-AzHealthBot -ResourceGroupName youriTest -Name yourihealthbot -Sku S1

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------ ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/30 6:12:33       test@microsoft.com    User                         Microsoft.HealthBot/health…
```

<span data-ttu-id="66f55-111">Aktualisieren von HealthBot nach Ressourcengruppenname und Name</span><span class="sxs-lookup"><span data-stu-id="66f55-111">update HealthBot by Resourcegroupname and Name</span></span>

### <span data-ttu-id="66f55-112">Beispiel 2: Aktualisieren von HealthBot nach InputObject</span><span class="sxs-lookup"><span data-stu-id="66f55-112">Example 2: update HealthBot by InputObject</span></span>
```powershell
PS C:\> $getHealth = Get-AzHealthBot -ResourceGroupName youriTest -Name yourihealthbot
Update-AzHealthBot -InputObject $getHealth -Sku F0

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------ ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/30 6:12:33       test@microsoft.com    User                         Microsoft.HealthBot/health…
```

<span data-ttu-id="66f55-113">Aktualisieren von HealthBot von InputObject</span><span class="sxs-lookup"><span data-stu-id="66f55-113">update HealthBot by InputObject</span></span>

## <span data-ttu-id="66f55-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="66f55-114">PARAMETERS</span></span>

### <span data-ttu-id="66f55-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66f55-115">-DefaultProfile</span></span>
<span data-ttu-id="66f55-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="66f55-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66f55-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66f55-117">-InputObject</span></span>
<span data-ttu-id="66f55-118">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="66f55-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="66f55-119">-Name</span><span class="sxs-lookup"><span data-stu-id="66f55-119">-Name</span></span>
<span data-ttu-id="66f55-120">Der Name der Bot-Ressource.</span><span class="sxs-lookup"><span data-stu-id="66f55-120">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="66f55-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66f55-121">-ResourceGroupName</span></span>
<span data-ttu-id="66f55-122">Der Name der Bot-Ressourcengruppe im Benutzerabonnement.</span><span class="sxs-lookup"><span data-stu-id="66f55-122">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="66f55-123">-Sku</span><span class="sxs-lookup"><span data-stu-id="66f55-123">-Sku</span></span>
<span data-ttu-id="66f55-124">Der Name der HealthBot-SKU</span><span class="sxs-lookup"><span data-stu-id="66f55-124">The name of the HealthBot SKU</span></span>

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

### <span data-ttu-id="66f55-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="66f55-125">-SubscriptionId</span></span>
<span data-ttu-id="66f55-126">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="66f55-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="66f55-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="66f55-127">-Tag</span></span>
<span data-ttu-id="66f55-128">Tags für einen HealthBot.</span><span class="sxs-lookup"><span data-stu-id="66f55-128">Tags for a HealthBot.</span></span>

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

### <span data-ttu-id="66f55-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="66f55-129">-Confirm</span></span>
<span data-ttu-id="66f55-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="66f55-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66f55-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66f55-131">-WhatIf</span></span>
<span data-ttu-id="66f55-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66f55-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66f55-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="66f55-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66f55-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66f55-134">CommonParameters</span></span>
<span data-ttu-id="66f55-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66f55-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66f55-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66f55-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66f55-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="66f55-137">INPUTS</span></span>

### <span data-ttu-id="66f55-138">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="66f55-138">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="66f55-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="66f55-139">OUTPUTS</span></span>

### <span data-ttu-id="66f55-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="66f55-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="66f55-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="66f55-141">NOTES</span></span>

<span data-ttu-id="66f55-142">ALIASE</span><span class="sxs-lookup"><span data-stu-id="66f55-142">ALIASES</span></span>

<span data-ttu-id="66f55-143">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="66f55-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="66f55-144">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="66f55-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="66f55-145">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="66f55-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="66f55-146">INPUTOBJECT <IHealthBotIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="66f55-146">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="66f55-147">`[BotName <String>]`: Der Name der Bot-Ressource.</span><span class="sxs-lookup"><span data-stu-id="66f55-147">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="66f55-148">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="66f55-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="66f55-149">`[ResourceGroupName <String>]`: Der Name der Bot-Ressourcengruppe im Benutzerabonnement.</span><span class="sxs-lookup"><span data-stu-id="66f55-149">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="66f55-150">`[SubscriptionId <String>]`: Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="66f55-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="66f55-151">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="66f55-151">RELATED LINKS</span></span>

