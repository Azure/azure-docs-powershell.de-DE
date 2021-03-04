---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/powershell/module/az.subscription/update-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
ms.openlocfilehash: 0fe030e3ef4dfcb8e43ba436d37d582871e55a5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930683"
---
# <span data-ttu-id="d98cd-101">Update-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="d98cd-101">Update-AzSubscription</span></span>

## <span data-ttu-id="d98cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d98cd-102">SYNOPSIS</span></span>
<span data-ttu-id="d98cd-103">Aktualisiert ein Azure-Abonnement</span><span class="sxs-lookup"><span data-stu-id="d98cd-103">Updates an Azure Subscription</span></span>

## <span data-ttu-id="d98cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d98cd-104">SYNTAX</span></span>

```
Update-AzSubscription -SubscriptionId <String> -Action <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d98cd-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d98cd-105">DESCRIPTION</span></span>
<span data-ttu-id="d98cd-106">Das **Update-AzSubscription-Cmdlet** aktualisiert ein Azure-Abonnement</span><span class="sxs-lookup"><span data-stu-id="d98cd-106">The **Update-AzSubscription** cmdlet updates an Azure subscription</span></span>

## <span data-ttu-id="d98cd-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d98cd-107">EXAMPLES</span></span>

### <span data-ttu-id="d98cd-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d98cd-108">Example 1</span></span>
```powershell
PS C:\> Update-AzSubscription -SubscriptionId "86869d42-1782-4337-98b0-c905fb937d46" -Action "Cancel"

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled
```

<span data-ttu-id="d98cd-109">Aktualisiert das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d98cd-109">Updates the subscription</span></span>

## <span data-ttu-id="d98cd-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d98cd-110">PARAMETERS</span></span>

### <span data-ttu-id="d98cd-111">-Aktion</span><span class="sxs-lookup"><span data-stu-id="d98cd-111">-Action</span></span>
<span data-ttu-id="d98cd-112">Aktion, die im Abonnement durchzuführen ist</span><span class="sxs-lookup"><span data-stu-id="d98cd-112">Action to perform on subscription</span></span>

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

### <span data-ttu-id="d98cd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d98cd-113">-AsJob</span></span>
<span data-ttu-id="d98cd-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d98cd-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d98cd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d98cd-115">-DefaultProfile</span></span>
<span data-ttu-id="d98cd-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d98cd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d98cd-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d98cd-117">-Name</span></span>
<span data-ttu-id="d98cd-118">Name des Abonnements</span><span class="sxs-lookup"><span data-stu-id="d98cd-118">Name of the subscription</span></span>

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

### <span data-ttu-id="d98cd-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d98cd-119">-SubscriptionId</span></span>
<span data-ttu-id="d98cd-120">Zu aktualisierende Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="d98cd-120">Subscription Id to update</span></span>

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

### <span data-ttu-id="d98cd-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d98cd-121">-Confirm</span></span>
<span data-ttu-id="d98cd-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d98cd-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d98cd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d98cd-123">-WhatIf</span></span>
<span data-ttu-id="d98cd-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d98cd-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d98cd-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d98cd-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d98cd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d98cd-126">CommonParameters</span></span>
<span data-ttu-id="d98cd-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d98cd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d98cd-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d98cd-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d98cd-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d98cd-129">INPUTS</span></span>

### <span data-ttu-id="d98cd-130">Keine</span><span class="sxs-lookup"><span data-stu-id="d98cd-130">None</span></span>

## <span data-ttu-id="d98cd-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d98cd-131">OUTPUTS</span></span>

### <span data-ttu-id="d98cd-132">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="d98cd-132">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="d98cd-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d98cd-133">NOTES</span></span>

## <span data-ttu-id="d98cd-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d98cd-134">RELATED LINKS</span></span>
