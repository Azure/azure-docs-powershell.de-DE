---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/update-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
ms.openlocfilehash: 77e7904a83b7d14fac1379532a619547888d5542
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150084"
---
# <span data-ttu-id="a2575-101">Update-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="a2575-101">Update-AzSubscription</span></span>

## <span data-ttu-id="a2575-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2575-102">SYNOPSIS</span></span>
<span data-ttu-id="a2575-103">Aktualisiert ein Azure-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a2575-103">Updates an Azure Subscription</span></span>

## <span data-ttu-id="a2575-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a2575-104">SYNTAX</span></span>

```
Update-AzSubscription -SubscriptionId <String> -Action <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2575-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a2575-105">DESCRIPTION</span></span>
<span data-ttu-id="a2575-106">Das **Cmdlet "Update-AzSubscription"** aktualisiert ein Azure-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a2575-106">The **Update-AzSubscription** cmdlet updates an Azure subscription</span></span>

## <span data-ttu-id="a2575-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a2575-107">EXAMPLES</span></span>

### <span data-ttu-id="a2575-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a2575-108">Example 1</span></span>
```powershell
PS C:\> Update-AzSubscription -SubscriptionId "86869d42-1782-4337-98b0-c905fb937d46" -Action "Cancel"

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled
```

<span data-ttu-id="a2575-109">Aktualisiert das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a2575-109">Updates the subscription</span></span>

## <span data-ttu-id="a2575-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2575-110">PARAMETERS</span></span>

### <span data-ttu-id="a2575-111">-Aktion</span><span class="sxs-lookup"><span data-stu-id="a2575-111">-Action</span></span>
<span data-ttu-id="a2575-112">Aktion, die für das Abonnement durchzuführen ist</span><span class="sxs-lookup"><span data-stu-id="a2575-112">Action to perform on subscription</span></span>

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

### <span data-ttu-id="a2575-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2575-113">-AsJob</span></span>
<span data-ttu-id="a2575-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a2575-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2575-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2575-115">-DefaultProfile</span></span>
<span data-ttu-id="a2575-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a2575-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2575-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a2575-117">-Name</span></span>
<span data-ttu-id="a2575-118">Name des Abonnements</span><span class="sxs-lookup"><span data-stu-id="a2575-118">Name of the subscription</span></span>

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

### <span data-ttu-id="a2575-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a2575-119">-SubscriptionId</span></span>
<span data-ttu-id="a2575-120">Zu aktualisierende Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="a2575-120">Subscription Id to update</span></span>

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

### <span data-ttu-id="a2575-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2575-121">-Confirm</span></span>
<span data-ttu-id="a2575-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a2575-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2575-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a2575-123">-WhatIf</span></span>
<span data-ttu-id="a2575-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a2575-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2575-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a2575-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2575-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2575-126">CommonParameters</span></span>
<span data-ttu-id="a2575-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2575-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2575-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2575-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2575-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a2575-129">INPUTS</span></span>

### <span data-ttu-id="a2575-130">Keine</span><span class="sxs-lookup"><span data-stu-id="a2575-130">None</span></span>

## <span data-ttu-id="a2575-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a2575-131">OUTPUTS</span></span>

### <span data-ttu-id="a2575-132">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="a2575-132">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="a2575-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a2575-133">NOTES</span></span>

## <span data-ttu-id="a2575-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a2575-134">RELATED LINKS</span></span>
