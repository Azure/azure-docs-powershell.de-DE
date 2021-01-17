---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: a8087f41c33dc3bb066609393a87986d5016d1ae
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471595"
---
# <span data-ttu-id="aab6b-101">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="aab6b-101">Enable-AzDataCollection</span></span>

## <span data-ttu-id="aab6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aab6b-102">SYNOPSIS</span></span>
<span data-ttu-id="aab6b-103">Ermöglicht Azure PowerShell das Sammeln von Daten, um die Benutzererfahrung mit den Azure -PowerShell-Cmdlets zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="aab6b-103">Enables Azure PowerShell to collect data to improve the user experience with the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="aab6b-104">Beim Ausführen dieses Cmdlets wird die Datensammlung für den aktuellen Benutzer auf dem aktuellen Computer optdiert.</span><span class="sxs-lookup"><span data-stu-id="aab6b-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span> <span data-ttu-id="aab6b-105">Daten werden standardmäßig erfasst, sofern Sie dies nicht explizit melden.</span><span class="sxs-lookup"><span data-stu-id="aab6b-105">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="aab6b-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aab6b-106">SYNTAX</span></span>

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aab6b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aab6b-107">DESCRIPTION</span></span>

<span data-ttu-id="aab6b-108">Das `Enable-AzDataCollection` Cmdlet wird verwendet, um sich für die Datensammlung zu entscheiden.</span><span class="sxs-lookup"><span data-stu-id="aab6b-108">The `Enable-AzDataCollection` cmdlet is used to opt in to data collection.</span></span> <span data-ttu-id="aab6b-109">Azure PowerShell sammelt standardmäßig automatisch Telemetriedaten.</span><span class="sxs-lookup"><span data-stu-id="aab6b-109">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="aab6b-110">Microsoft aggregiert gesammelte Daten, um Verwendungsmuster zu identifizieren, häufige Probleme zu erkennen und die Benutzererfahrung mit Azure PowerShell zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="aab6b-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span>
<span data-ttu-id="aab6b-111">Microsoft Azure PowerShell sammelt keine privaten oder persönlichen Daten.</span><span class="sxs-lookup"><span data-stu-id="aab6b-111">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="aab6b-112">Zum Deaktivieren der Datensammlung müssen Sie die Ausführung explizit `Disable-AzDataCollection` deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="aab6b-112">To disable data collection, you must explicitly opt out by executing `Disable-AzDataCollection`.</span></span>

## <span data-ttu-id="aab6b-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aab6b-113">EXAMPLES</span></span>

### <span data-ttu-id="aab6b-114">Beispiel 1: Aktivieren der Datensammlung für den aktuellen Benutzer</span><span class="sxs-lookup"><span data-stu-id="aab6b-114">Example 1: Enabling data collection for the current user</span></span>

<span data-ttu-id="aab6b-115">Das folgende Beispiel zeigt, wie die Datensammlung für den aktuellen Benutzer aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="aab6b-115">The following example shows how to enable data collection for the current user.</span></span>

```powershell
Enable-AzDataCollection
```

## <span data-ttu-id="aab6b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aab6b-116">PARAMETERS</span></span>

### <span data-ttu-id="aab6b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aab6b-117">-DefaultProfile</span></span>

<span data-ttu-id="aab6b-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aab6b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aab6b-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aab6b-119">-Confirm</span></span>

<span data-ttu-id="aab6b-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aab6b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aab6b-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="aab6b-121">-WhatIf</span></span>

<span data-ttu-id="aab6b-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aab6b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aab6b-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aab6b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aab6b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aab6b-124">CommonParameters</span></span>

<span data-ttu-id="aab6b-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aab6b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aab6b-126">Weitere Informationen finden Sie unter [about_CommonParameters.](/powershell/module/microsoft.powershell.core/about/about_commonparameters)</span><span class="sxs-lookup"><span data-stu-id="aab6b-126">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="aab6b-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aab6b-127">INPUTS</span></span>

### <span data-ttu-id="aab6b-128">Keine</span><span class="sxs-lookup"><span data-stu-id="aab6b-128">None</span></span>

## <span data-ttu-id="aab6b-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aab6b-129">OUTPUTS</span></span>

### <span data-ttu-id="aab6b-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="aab6b-130">System.Void</span></span>

## <span data-ttu-id="aab6b-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="aab6b-131">NOTES</span></span>

## <span data-ttu-id="aab6b-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="aab6b-132">RELATED LINKS</span></span>

[<span data-ttu-id="aab6b-133">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="aab6b-133">Disable-AzDataCollection</span></span>](./Disable-AzDataCollection.md)
