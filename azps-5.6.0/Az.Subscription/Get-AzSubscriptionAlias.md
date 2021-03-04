---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/powershell/module/az.subscription/get-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
ms.openlocfilehash: 0cce48f38b669c713f0d3a193deec64cfce649e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937264"
---
# <span data-ttu-id="8f50f-101">Get-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="8f50f-101">Get-AzSubscriptionAlias</span></span>

## <span data-ttu-id="8f50f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f50f-102">SYNOPSIS</span></span>
<span data-ttu-id="8f50f-103">Ruft Abonnementaliasdetails ab</span><span class="sxs-lookup"><span data-stu-id="8f50f-103">Gets subscription alias details</span></span>

## <span data-ttu-id="8f50f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f50f-104">SYNTAX</span></span>

```
Get-AzSubscriptionAlias [-AliasName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f50f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f50f-105">DESCRIPTION</span></span>
<span data-ttu-id="8f50f-106">Das **Get-AzSubscriptionAlias-Cmdlet** erhält Abonnementaliasdetails.</span><span class="sxs-lookup"><span data-stu-id="8f50f-106">The **Get-AzSubscriptionAlias** cmdlet gets subscription alias details.</span></span>

## <span data-ttu-id="8f50f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8f50f-107">EXAMPLES</span></span>

### <span data-ttu-id="8f50f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8f50f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="8f50f-109">Ruft Abonnementaliasdetails ab</span><span class="sxs-lookup"><span data-stu-id="8f50f-109">Gets subscription alias details</span></span>

## <span data-ttu-id="8f50f-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8f50f-110">PARAMETERS</span></span>

### <span data-ttu-id="8f50f-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="8f50f-111">-AliasName</span></span>
<span data-ttu-id="8f50f-112">Alias für das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8f50f-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="8f50f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f50f-113">-AsJob</span></span>
<span data-ttu-id="8f50f-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8f50f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8f50f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f50f-115">-DefaultProfile</span></span>
<span data-ttu-id="8f50f-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8f50f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f50f-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8f50f-117">-Confirm</span></span>
<span data-ttu-id="8f50f-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8f50f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f50f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f50f-119">-WhatIf</span></span>
<span data-ttu-id="8f50f-120">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8f50f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f50f-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8f50f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f50f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f50f-122">CommonParameters</span></span>
<span data-ttu-id="8f50f-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f50f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f50f-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f50f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f50f-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8f50f-125">INPUTS</span></span>

### <span data-ttu-id="8f50f-126">Keine</span><span class="sxs-lookup"><span data-stu-id="8f50f-126">None</span></span>

## <span data-ttu-id="8f50f-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8f50f-127">OUTPUTS</span></span>

### <span data-ttu-id="8f50f-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="8f50f-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="8f50f-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8f50f-129">NOTES</span></span>

## <span data-ttu-id="8f50f-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8f50f-130">RELATED LINKS</span></span>
