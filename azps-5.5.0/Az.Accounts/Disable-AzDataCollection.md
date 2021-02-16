---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 27b3565191d7de110a5ba3a1e37d204fe3301cbf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162689"
---
# <span data-ttu-id="d5d1d-101">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="d5d1d-101">Disable-AzDataCollection</span></span>

## <span data-ttu-id="d5d1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5d1d-102">SYNOPSIS</span></span>
<span data-ttu-id="d5d1d-103">Sie können das Sammeln von Daten nicht mehr nutzen, um die Azure PowerShell-Cmdlets zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="d5d1d-103">Opts out of collecting data to improve the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="d5d1d-104">Daten werden standardmäßig erfasst, sofern Sie dies nicht explizit melden.</span><span class="sxs-lookup"><span data-stu-id="d5d1d-104">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="d5d1d-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5d1d-105">SYNTAX</span></span>

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5d1d-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5d1d-106">DESCRIPTION</span></span>

<span data-ttu-id="d5d1d-107">Das `Disable-AzDataCollection` Cmdlet wird verwendet, um die Datensammlung zu melden.</span><span class="sxs-lookup"><span data-stu-id="d5d1d-107">The `Disable-AzDataCollection` cmdlet is used to opt out of data collection.</span></span> <span data-ttu-id="d5d1d-108">Azure PowerShell sammelt standardmäßig automatisch Telemetriedaten.</span><span class="sxs-lookup"><span data-stu-id="d5d1d-108">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="d5d1d-109">Um die Datensammlung zu deaktivieren, müssen Sie dies explizit deaktivieren. Microsoft aggregiert gesammelte Daten, um Verwendungsmuster zu identifizieren, häufige Probleme zu erkennen und die Benutzererfahrung mit Azure PowerShell zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="d5d1d-109">To disable data collection, you must explicitly opt-out. Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span> <span data-ttu-id="d5d1d-110">Microsoft Azure PowerShell sammelt keine privaten oder persönlichen Daten.</span><span class="sxs-lookup"><span data-stu-id="d5d1d-110">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="d5d1d-111">Wenn Sie sich zuvor abmelden, führen Sie das Cmdlet aus, um die Datensammlung für den aktuellen Benutzer auf dem `Enable-AzDataCollection` aktuellen Computer erneut zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d5d1d-111">If you've previously opted out, run the `Enable-AzDataCollection` cmdlet to re-enable data collection for the current user on the current machine.</span></span>

## <span data-ttu-id="d5d1d-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d5d1d-112">EXAMPLES</span></span>

### <span data-ttu-id="d5d1d-113">Beispiel 1: Deaktivieren der Datensammlung für den aktuellen Benutzer</span><span class="sxs-lookup"><span data-stu-id="d5d1d-113">Example 1: Disabling data collection for the current user</span></span>

<span data-ttu-id="d5d1d-114">Das folgende Beispiel zeigt, wie Die Datensammlung für den aktuellen Benutzer deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="d5d1d-114">The following example shows how to disable data collection for the current user.</span></span>

```powershell
Disable-AzDataCollection
```

## <span data-ttu-id="d5d1d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5d1d-115">PARAMETERS</span></span>

### <span data-ttu-id="d5d1d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5d1d-116">-DefaultProfile</span></span>

<span data-ttu-id="d5d1d-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d5d1d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5d1d-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d5d1d-118">-Confirm</span></span>

<span data-ttu-id="d5d1d-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d5d1d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5d1d-120">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d5d1d-120">-WhatIf</span></span>

<span data-ttu-id="d5d1d-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5d1d-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d5d1d-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5d1d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5d1d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5d1d-123">CommonParameters</span></span>

<span data-ttu-id="d5d1d-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5d1d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5d1d-125">Weitere Informationen finden Sie unter [about_CommonParameters.](/powershell/module/microsoft.powershell.core/about/about_commonparameters)</span><span class="sxs-lookup"><span data-stu-id="d5d1d-125">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="d5d1d-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d5d1d-126">INPUTS</span></span>

### <span data-ttu-id="d5d1d-127">Keine</span><span class="sxs-lookup"><span data-stu-id="d5d1d-127">None</span></span>

## <span data-ttu-id="d5d1d-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d5d1d-128">OUTPUTS</span></span>

### <span data-ttu-id="d5d1d-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="d5d1d-129">System.Void</span></span>

## <span data-ttu-id="d5d1d-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d5d1d-130">NOTES</span></span>

## <span data-ttu-id="d5d1d-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d5d1d-131">RELATED LINKS</span></span>

[<span data-ttu-id="d5d1d-132">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="d5d1d-132">Enable-AzDataCollection</span></span>](./Enable-AzDataCollection.md)
