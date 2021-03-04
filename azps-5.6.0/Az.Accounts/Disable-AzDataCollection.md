---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 54af80b230c3cb031e8927a82ec3536cc1a81ec0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943208"
---
# <span data-ttu-id="938fa-101">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="938fa-101">Disable-AzDataCollection</span></span>

## <span data-ttu-id="938fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="938fa-102">SYNOPSIS</span></span>
<span data-ttu-id="938fa-103">Opts out of collecting data to improve the Azure PowerShell cmdlets.</span><span class="sxs-lookup"><span data-stu-id="938fa-103">Opts out of collecting data to improve the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="938fa-104">Die Daten werden standardmäßig erfasst, es sei denn, Sie melde sich explizit ab.</span><span class="sxs-lookup"><span data-stu-id="938fa-104">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="938fa-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="938fa-105">SYNTAX</span></span>

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="938fa-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="938fa-106">DESCRIPTION</span></span>

<span data-ttu-id="938fa-107">Das `Disable-AzDataCollection` Cmdlet wird zum Abmelden der Datensammlung verwendet.</span><span class="sxs-lookup"><span data-stu-id="938fa-107">The `Disable-AzDataCollection` cmdlet is used to opt out of data collection.</span></span> <span data-ttu-id="938fa-108">Azure PowerShell sammelt standardmäßig automatisch Telemetriedaten.</span><span class="sxs-lookup"><span data-stu-id="938fa-108">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="938fa-109">Um die Datensammlung zu deaktivieren, müssen Sie die Datensammlung explizit deaktivieren. Microsoft aggregiert gesammelte Daten, um Nutzungsmuster zu identifizieren, häufige Probleme zu identifizieren und die Benutzererfahrung von Azure PowerShell zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="938fa-109">To disable data collection, you must explicitly opt-out. Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span> <span data-ttu-id="938fa-110">Microsoft Azure PowerShell sammelt keine privaten oder persönlichen Daten.</span><span class="sxs-lookup"><span data-stu-id="938fa-110">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="938fa-111">Wenn Sie sich zuvor entschieden haben, führen Sie das Cmdlet aus, um die Datensammlung für den aktuellen Benutzer auf dem `Enable-AzDataCollection` aktuellen Computer erneut zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="938fa-111">If you've previously opted out, run the `Enable-AzDataCollection` cmdlet to re-enable data collection for the current user on the current machine.</span></span>

## <span data-ttu-id="938fa-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="938fa-112">EXAMPLES</span></span>

### <span data-ttu-id="938fa-113">Beispiel 1: Deaktivieren der Datensammlung für den aktuellen Benutzer</span><span class="sxs-lookup"><span data-stu-id="938fa-113">Example 1: Disabling data collection for the current user</span></span>

<span data-ttu-id="938fa-114">Das folgende Beispiel zeigt, wie Sie die Datensammlung für den aktuellen Benutzer deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="938fa-114">The following example shows how to disable data collection for the current user.</span></span>

```powershell
Disable-AzDataCollection
```

## <span data-ttu-id="938fa-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="938fa-115">PARAMETERS</span></span>

### <span data-ttu-id="938fa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="938fa-116">-DefaultProfile</span></span>

<span data-ttu-id="938fa-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="938fa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="938fa-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="938fa-118">-Confirm</span></span>

<span data-ttu-id="938fa-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="938fa-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="938fa-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="938fa-120">-WhatIf</span></span>

<span data-ttu-id="938fa-121">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="938fa-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="938fa-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="938fa-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="938fa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="938fa-123">CommonParameters</span></span>
<span data-ttu-id="938fa-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="938fa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="938fa-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="938fa-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="938fa-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="938fa-126">INPUTS</span></span>

### <span data-ttu-id="938fa-127">Keine</span><span class="sxs-lookup"><span data-stu-id="938fa-127">None</span></span>

## <span data-ttu-id="938fa-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="938fa-128">OUTPUTS</span></span>

### <span data-ttu-id="938fa-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="938fa-129">System.Void</span></span>

## <span data-ttu-id="938fa-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="938fa-130">NOTES</span></span>

## <span data-ttu-id="938fa-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="938fa-131">RELATED LINKS</span></span>

[<span data-ttu-id="938fa-132">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="938fa-132">Enable-AzDataCollection</span></span>](./Enable-AzDataCollection.md)
