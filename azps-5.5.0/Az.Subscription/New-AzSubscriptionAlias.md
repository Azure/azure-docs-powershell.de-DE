---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/new-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
ms.openlocfilehash: 2e957f3a149c4aac30ac83c03997611125aa7870
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150100"
---
# <span data-ttu-id="8b5bc-101">New-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="8b5bc-101">New-AzSubscriptionAlias</span></span>

## <span data-ttu-id="8b5bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b5bc-102">SYNOPSIS</span></span>
<span data-ttu-id="8b5bc-103">Erstellt einen neuen Alias und ein neues Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8b5bc-103">Creates new alias and subscription</span></span>

## <span data-ttu-id="8b5bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b5bc-104">SYNTAX</span></span>

```
New-AzSubscriptionAlias -AliasName <String> [-BillingScope <String>] [-Workload <String>]
 [-SubscriptionName <String>] [-ResellerId <String>] [-SubscriptionId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b5bc-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b5bc-105">DESCRIPTION</span></span>
<span data-ttu-id="8b5bc-106">Das **Cmdlet "New-AzSubscriptionAlias"** erstellt einen neuen Alias und ein neues Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8b5bc-106">The **New-AzSubscriptionAlias** cmdlet creates new alias and subscription</span></span>

## <span data-ttu-id="8b5bc-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8b5bc-107">EXAMPLES</span></span>

### <span data-ttu-id="8b5bc-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8b5bc-108">Example 1</span></span>
```powershell
PS C:\> New-AzSubscriptionAlias -AliasName "NewAliasName" -SubscriptionName "SubscriptionName" -BillingScope "BillingScope" -Workload "WorkloadType"
```

<span data-ttu-id="8b5bc-109">Erstellt einen neuen Alias und ein neues Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8b5bc-109">Creates new alias and subscription</span></span>

## <span data-ttu-id="8b5bc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b5bc-110">PARAMETERS</span></span>

### <span data-ttu-id="8b5bc-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="8b5bc-111">-AliasName</span></span>
<span data-ttu-id="8b5bc-112">Alias für das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8b5bc-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="8b5bc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b5bc-113">-AsJob</span></span>
<span data-ttu-id="8b5bc-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8b5bc-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8b5bc-115">-BillingScope</span><span class="sxs-lookup"><span data-stu-id="8b5bc-115">-BillingScope</span></span>
<span data-ttu-id="8b5bc-116">Abrechnungsbereich</span><span class="sxs-lookup"><span data-stu-id="8b5bc-116">Billing Scope</span></span>

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

### <span data-ttu-id="8b5bc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b5bc-117">-DefaultProfile</span></span>
<span data-ttu-id="8b5bc-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8b5bc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b5bc-119">-ResellerId</span><span class="sxs-lookup"><span data-stu-id="8b5bc-119">-ResellerId</span></span>
<span data-ttu-id="8b5bc-120">Händler-ID</span><span class="sxs-lookup"><span data-stu-id="8b5bc-120">Reseller Id</span></span>

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

### <span data-ttu-id="8b5bc-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8b5bc-121">-SubscriptionId</span></span>
<span data-ttu-id="8b5bc-122">Vorhandene Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="8b5bc-122">Existing Subscription Id</span></span>

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

### <span data-ttu-id="8b5bc-123">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="8b5bc-123">-SubscriptionName</span></span>
<span data-ttu-id="8b5bc-124">Name des Abonnements</span><span class="sxs-lookup"><span data-stu-id="8b5bc-124">Name of the subscription</span></span>

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

### <span data-ttu-id="8b5bc-125">-Workload</span><span class="sxs-lookup"><span data-stu-id="8b5bc-125">-Workload</span></span>
<span data-ttu-id="8b5bc-126">Arbeitsauslastungstyp</span><span class="sxs-lookup"><span data-stu-id="8b5bc-126">Type of Workload</span></span>

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

### <span data-ttu-id="8b5bc-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b5bc-127">-Confirm</span></span>
<span data-ttu-id="8b5bc-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8b5bc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b5bc-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8b5bc-129">-WhatIf</span></span>
<span data-ttu-id="8b5bc-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8b5bc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b5bc-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8b5bc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b5bc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b5bc-132">CommonParameters</span></span>
<span data-ttu-id="8b5bc-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b5bc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b5bc-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b5bc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b5bc-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8b5bc-135">INPUTS</span></span>

### <span data-ttu-id="8b5bc-136">Keine</span><span class="sxs-lookup"><span data-stu-id="8b5bc-136">None</span></span>

## <span data-ttu-id="8b5bc-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8b5bc-137">OUTPUTS</span></span>

### <span data-ttu-id="8b5bc-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="8b5bc-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="8b5bc-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8b5bc-139">NOTES</span></span>

## <span data-ttu-id="8b5bc-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8b5bc-140">RELATED LINKS</span></span>
