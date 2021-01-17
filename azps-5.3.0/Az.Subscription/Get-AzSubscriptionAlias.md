---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/get-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
ms.openlocfilehash: a76c993abb254b1e24200267bf0195cb613d8207
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471661"
---
# <span data-ttu-id="6ec25-101">Get-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="6ec25-101">Get-AzSubscriptionAlias</span></span>

## <span data-ttu-id="6ec25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ec25-102">SYNOPSIS</span></span>
<span data-ttu-id="6ec25-103">Ruft Abonnementaliasdetails ab</span><span class="sxs-lookup"><span data-stu-id="6ec25-103">Gets subscription alias details</span></span>

## <span data-ttu-id="6ec25-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ec25-104">SYNTAX</span></span>

```
Get-AzSubscriptionAlias [-AliasName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ec25-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec25-105">DESCRIPTION</span></span>
<span data-ttu-id="6ec25-106">Das **Get-AzSubscriptionAlias-Cmdlet** ruft Details zum Abonnementalias ab.</span><span class="sxs-lookup"><span data-stu-id="6ec25-106">The **Get-AzSubscriptionAlias** cmdlet gets subscription alias details.</span></span>

## <span data-ttu-id="6ec25-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6ec25-107">EXAMPLES</span></span>

### <span data-ttu-id="6ec25-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6ec25-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="6ec25-109">Ruft Abonnementaliasdetails ab</span><span class="sxs-lookup"><span data-stu-id="6ec25-109">Gets subscription alias details</span></span>

## <span data-ttu-id="6ec25-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ec25-110">PARAMETERS</span></span>

### <span data-ttu-id="6ec25-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="6ec25-111">-AliasName</span></span>
<span data-ttu-id="6ec25-112">Alias für das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6ec25-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="6ec25-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ec25-113">-AsJob</span></span>
<span data-ttu-id="6ec25-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6ec25-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6ec25-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ec25-115">-DefaultProfile</span></span>
<span data-ttu-id="6ec25-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6ec25-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ec25-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ec25-117">-Confirm</span></span>
<span data-ttu-id="6ec25-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6ec25-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ec25-119">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6ec25-119">-WhatIf</span></span>
<span data-ttu-id="6ec25-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6ec25-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ec25-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6ec25-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ec25-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ec25-122">CommonParameters</span></span>
<span data-ttu-id="6ec25-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ec25-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ec25-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ec25-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ec25-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6ec25-125">INPUTS</span></span>

### <span data-ttu-id="6ec25-126">Keine</span><span class="sxs-lookup"><span data-stu-id="6ec25-126">None</span></span>

## <span data-ttu-id="6ec25-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6ec25-127">OUTPUTS</span></span>

### <span data-ttu-id="6ec25-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="6ec25-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="6ec25-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6ec25-129">NOTES</span></span>

## <span data-ttu-id="6ec25-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6ec25-130">RELATED LINKS</span></span>
