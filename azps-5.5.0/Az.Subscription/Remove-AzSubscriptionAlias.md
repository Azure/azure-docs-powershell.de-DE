---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/remove-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
ms.openlocfilehash: 02a32b3e6c39ae66aea8efc37213a6fb3bca0848
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150097"
---
# <span data-ttu-id="4caaa-101">Remove-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="4caaa-101">Remove-AzSubscriptionAlias</span></span>

## <span data-ttu-id="4caaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4caaa-102">SYNOPSIS</span></span>
<span data-ttu-id="4caaa-103">Löscht den Abonnementalias.</span><span class="sxs-lookup"><span data-stu-id="4caaa-103">Deletes the subscription alias</span></span>

## <span data-ttu-id="4caaa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4caaa-104">SYNTAX</span></span>

```
Remove-AzSubscriptionAlias -AliasName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4caaa-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4caaa-105">DESCRIPTION</span></span>
<span data-ttu-id="4caaa-106">Das **Cmdlet "Remove-AzSubscriptionAlias"** entfernt den Abonnementalias</span><span class="sxs-lookup"><span data-stu-id="4caaa-106">The **Remove-AzSubscriptionAlias** cmdlet removes the subscription alias</span></span>

## <span data-ttu-id="4caaa-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4caaa-107">EXAMPLES</span></span>

### <span data-ttu-id="4caaa-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4caaa-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="4caaa-109">Löscht den Abonnementalias.</span><span class="sxs-lookup"><span data-stu-id="4caaa-109">Deletes the subscription alias</span></span>

## <span data-ttu-id="4caaa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4caaa-110">PARAMETERS</span></span>

### <span data-ttu-id="4caaa-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="4caaa-111">-AliasName</span></span>
<span data-ttu-id="4caaa-112">Alias für das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4caaa-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="4caaa-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4caaa-113">-AsJob</span></span>
<span data-ttu-id="4caaa-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4caaa-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4caaa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4caaa-115">-DefaultProfile</span></span>
<span data-ttu-id="4caaa-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4caaa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4caaa-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4caaa-117">-Confirm</span></span>
<span data-ttu-id="4caaa-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4caaa-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4caaa-119">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4caaa-119">-WhatIf</span></span>
<span data-ttu-id="4caaa-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4caaa-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4caaa-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4caaa-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4caaa-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4caaa-122">CommonParameters</span></span>
<span data-ttu-id="4caaa-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4caaa-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4caaa-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4caaa-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4caaa-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4caaa-125">INPUTS</span></span>

### <span data-ttu-id="4caaa-126">Keine</span><span class="sxs-lookup"><span data-stu-id="4caaa-126">None</span></span>

## <span data-ttu-id="4caaa-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4caaa-127">OUTPUTS</span></span>

### <span data-ttu-id="4caaa-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="4caaa-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="4caaa-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4caaa-129">NOTES</span></span>

## <span data-ttu-id="4caaa-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4caaa-130">RELATED LINKS</span></span>
