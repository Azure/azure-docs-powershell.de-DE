---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 27b3565191d7de110a5ba3a1e37d204fe3301cbf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294371"
---
# <span data-ttu-id="018e2-101">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="018e2-101">Disable-AzDataCollection</span></span>

## <span data-ttu-id="018e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="018e2-102">SYNOPSIS</span></span>
<span data-ttu-id="018e2-103">Sie können das Sammeln von Daten nicht mehr nutzen, um die Azure PowerShell-Cmdlets zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="018e2-103">Opts out of collecting data to improve the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="018e2-104">Daten werden standardmäßig erfasst, sofern Sie dies nicht explizit melden.</span><span class="sxs-lookup"><span data-stu-id="018e2-104">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="018e2-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="018e2-105">SYNTAX</span></span>

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="018e2-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="018e2-106">DESCRIPTION</span></span>

<span data-ttu-id="018e2-107">Das `Disable-AzDataCollection` Cmdlet wird verwendet, um die Datensammlung zu melden.</span><span class="sxs-lookup"><span data-stu-id="018e2-107">The `Disable-AzDataCollection` cmdlet is used to opt out of data collection.</span></span> <span data-ttu-id="018e2-108">Azure PowerShell sammelt standardmäßig automatisch Telemetriedaten.</span><span class="sxs-lookup"><span data-stu-id="018e2-108">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="018e2-109">Um die Datensammlung zu deaktivieren, müssen Sie dies explizit deaktivieren. Microsoft aggregiert gesammelte Daten, um Verwendungsmuster zu identifizieren, häufige Probleme zu erkennen und die Benutzererfahrung mit Azure PowerShell zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="018e2-109">To disable data collection, you must explicitly opt-out. Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span> <span data-ttu-id="018e2-110">Microsoft Azure PowerShell sammelt keine privaten oder persönlichen Daten.</span><span class="sxs-lookup"><span data-stu-id="018e2-110">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="018e2-111">Wenn Sie sich zuvor abmelden, führen Sie das Cmdlet aus, um die Datensammlung für den aktuellen Benutzer auf dem `Enable-AzDataCollection` aktuellen Computer erneut zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="018e2-111">If you've previously opted out, run the `Enable-AzDataCollection` cmdlet to re-enable data collection for the current user on the current machine.</span></span>

## <span data-ttu-id="018e2-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="018e2-112">EXAMPLES</span></span>

### <span data-ttu-id="018e2-113">Beispiel 1: Deaktivieren der Datensammlung für den aktuellen Benutzer</span><span class="sxs-lookup"><span data-stu-id="018e2-113">Example 1: Disabling data collection for the current user</span></span>

<span data-ttu-id="018e2-114">Das folgende Beispiel zeigt, wie Die Datensammlung für den aktuellen Benutzer deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="018e2-114">The following example shows how to disable data collection for the current user.</span></span>

```powershell
Disable-AzDataCollection
```

## <span data-ttu-id="018e2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="018e2-115">PARAMETERS</span></span>

### <span data-ttu-id="018e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="018e2-116">-DefaultProfile</span></span>

<span data-ttu-id="018e2-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="018e2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="018e2-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="018e2-118">-Confirm</span></span>

<span data-ttu-id="018e2-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="018e2-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="018e2-120">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="018e2-120">-WhatIf</span></span>

<span data-ttu-id="018e2-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="018e2-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="018e2-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="018e2-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="018e2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="018e2-123">CommonParameters</span></span>

<span data-ttu-id="018e2-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="018e2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="018e2-125">Weitere Informationen finden Sie unter [about_CommonParameters.](/powershell/module/microsoft.powershell.core/about/about_commonparameters)</span><span class="sxs-lookup"><span data-stu-id="018e2-125">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="018e2-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="018e2-126">INPUTS</span></span>

### <span data-ttu-id="018e2-127">Keine</span><span class="sxs-lookup"><span data-stu-id="018e2-127">None</span></span>

## <span data-ttu-id="018e2-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="018e2-128">OUTPUTS</span></span>

### <span data-ttu-id="018e2-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="018e2-129">System.Void</span></span>

## <span data-ttu-id="018e2-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="018e2-130">NOTES</span></span>

## <span data-ttu-id="018e2-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="018e2-131">RELATED LINKS</span></span>

[<span data-ttu-id="018e2-132">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="018e2-132">Enable-AzDataCollection</span></span>](./Enable-AzDataCollection.md)
