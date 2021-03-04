---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/powershell/module/az.healthbot/new-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/New-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/New-AzHealthBot.md
ms.openlocfilehash: b9c4e4cd55f81449497b0d397574c3eeec64d2d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949227"
---
# <span data-ttu-id="f834e-101">New-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="f834e-101">New-AzHealthBot</span></span>

## <span data-ttu-id="f834e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f834e-102">SYNOPSIS</span></span>
<span data-ttu-id="f834e-103">Erstellen Sie einen neuen HealthBot.</span><span class="sxs-lookup"><span data-stu-id="f834e-103">Create a new HealthBot.</span></span>

## <span data-ttu-id="f834e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f834e-104">SYNTAX</span></span>

```
New-AzHealthBot -Name <String> -ResourceGroupName <String> -Location <String> -Sku <SkuName>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f834e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f834e-105">DESCRIPTION</span></span>
<span data-ttu-id="f834e-106">Erstellen Sie einen neuen HealthBot.</span><span class="sxs-lookup"><span data-stu-id="f834e-106">Create a new HealthBot.</span></span>

## <span data-ttu-id="f834e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f834e-107">EXAMPLES</span></span>

### <span data-ttu-id="f834e-108">Beispiel 1: Erstellen eines neuen HealthBots</span><span class="sxs-lookup"><span data-stu-id="f834e-108">Example 1: Create new HealthBot</span></span>
```powershell
PS C:\> New-AzHealthBot -Name yourihealthbot1 -ResourceGroupName youriTest -Location eastus -Sku F0

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/29 8:19:14       6db4d6bb-6649-4dc2-84b7-0b5c6894031e Application                  Microsoft.Heal…
```

<span data-ttu-id="f834e-109">Erstellen eines neuen HealthBot Standardmäßig</span><span class="sxs-lookup"><span data-stu-id="f834e-109">Create new HealthBot By default</span></span>

## <span data-ttu-id="f834e-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f834e-110">PARAMETERS</span></span>

### <span data-ttu-id="f834e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f834e-111">-AsJob</span></span>
<span data-ttu-id="f834e-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="f834e-112">Run the command as a job</span></span>

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

### <span data-ttu-id="f834e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f834e-113">-DefaultProfile</span></span>
<span data-ttu-id="f834e-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f834e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f834e-115">-Location</span><span class="sxs-lookup"><span data-stu-id="f834e-115">-Location</span></span>
<span data-ttu-id="f834e-116">Der Geospeicherort, an dem sich die Ressource befindet</span><span class="sxs-lookup"><span data-stu-id="f834e-116">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="f834e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f834e-117">-Name</span></span>
<span data-ttu-id="f834e-118">Der Name der Bot-Ressource.</span><span class="sxs-lookup"><span data-stu-id="f834e-118">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f834e-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f834e-119">-NoWait</span></span>
<span data-ttu-id="f834e-120">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="f834e-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f834e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f834e-121">-ResourceGroupName</span></span>
<span data-ttu-id="f834e-122">Der Name der Bot-Ressourcengruppe im Benutzerabonnement.</span><span class="sxs-lookup"><span data-stu-id="f834e-122">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="f834e-123">-Sku</span><span class="sxs-lookup"><span data-stu-id="f834e-123">-Sku</span></span>
<span data-ttu-id="f834e-124">Der Name der HealthBot-SKU</span><span class="sxs-lookup"><span data-stu-id="f834e-124">The name of the HealthBot SKU</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f834e-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f834e-125">-SubscriptionId</span></span>
<span data-ttu-id="f834e-126">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="f834e-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="f834e-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="f834e-127">-Tag</span></span>
<span data-ttu-id="f834e-128">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="f834e-128">Resource tags.</span></span>

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

### <span data-ttu-id="f834e-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f834e-129">-Confirm</span></span>
<span data-ttu-id="f834e-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f834e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f834e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f834e-131">-WhatIf</span></span>
<span data-ttu-id="f834e-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f834e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f834e-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f834e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f834e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f834e-134">CommonParameters</span></span>
<span data-ttu-id="f834e-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f834e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f834e-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f834e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f834e-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f834e-137">INPUTS</span></span>

## <span data-ttu-id="f834e-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f834e-138">OUTPUTS</span></span>

### <span data-ttu-id="f834e-139">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="f834e-139">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="f834e-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f834e-140">NOTES</span></span>

<span data-ttu-id="f834e-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="f834e-141">ALIASES</span></span>

## <span data-ttu-id="f834e-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f834e-142">RELATED LINKS</span></span>

