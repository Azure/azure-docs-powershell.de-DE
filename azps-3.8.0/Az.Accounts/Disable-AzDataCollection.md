---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 27b3565191d7de110a5ba3a1e37d204fe3301cbf
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "94005286"
---
# <span data-ttu-id="ece04-101">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="ece04-101">Disable-AzDataCollection</span></span>

## <span data-ttu-id="ece04-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ece04-102">SYNOPSIS</span></span>
<span data-ttu-id="ece04-103">Entscheidet sich, Daten zu sammeln, um die Azure PowerShell-Cmdlets zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="ece04-103">Opts out of collecting data to improve the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="ece04-104">Daten werden standardmäßig erfasst, es sei denn, dass Sie sich ausdrücklich entscheiden.</span><span class="sxs-lookup"><span data-stu-id="ece04-104">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="ece04-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ece04-105">SYNTAX</span></span>

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ece04-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ece04-106">DESCRIPTION</span></span>

<span data-ttu-id="ece04-107">Das `Disable-AzDataCollection` Cmdlet wird verwendet, um die Datensammlung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="ece04-107">The `Disable-AzDataCollection` cmdlet is used to opt out of data collection.</span></span> <span data-ttu-id="ece04-108">Azure PowerShell sammelt standardmäßig Telemetrie-Daten automatisch.</span><span class="sxs-lookup"><span data-stu-id="ece04-108">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="ece04-109">Wenn Sie die Datensammlung deaktivieren möchten, müssen Sie explizit abmelden. Microsoft aggregiert gesammelte Daten, um Nutzungsmuster zu identifizieren, häufige Probleme zu erkennen und die Erfahrung von Azure PowerShell zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="ece04-109">To disable data collection, you must explicitly opt-out. Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span> <span data-ttu-id="ece04-110">Microsoft Azure PowerShell sammelt keine privaten oder persönlichen Daten.</span><span class="sxs-lookup"><span data-stu-id="ece04-110">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="ece04-111">Wenn Sie sich zuvor entschieden haben, führen Sie das Cmdlet aus, `Enable-AzDataCollection` um die Datensammlung für den aktuellen Benutzer auf dem aktuellen Computer erneut zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ece04-111">If you've previously opted out, run the `Enable-AzDataCollection` cmdlet to re-enable data collection for the current user on the current machine.</span></span>

## <span data-ttu-id="ece04-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ece04-112">EXAMPLES</span></span>

### <span data-ttu-id="ece04-113">Beispiel 1: Deaktivieren der Datensammlung für den aktuellen Benutzer</span><span class="sxs-lookup"><span data-stu-id="ece04-113">Example 1: Disabling data collection for the current user</span></span>

<span data-ttu-id="ece04-114">Im folgenden Beispiel wird gezeigt, wie Sie die Datensammlung für den aktuellen Benutzer deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="ece04-114">The following example shows how to disable data collection for the current user.</span></span>

```powershell
Disable-AzDataCollection
```

## <span data-ttu-id="ece04-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="ece04-115">PARAMETERS</span></span>

### <span data-ttu-id="ece04-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ece04-116">-DefaultProfile</span></span>

<span data-ttu-id="ece04-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ece04-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ece04-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ece04-118">-Confirm</span></span>

<span data-ttu-id="ece04-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ece04-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ece04-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ece04-120">-WhatIf</span></span>

<span data-ttu-id="ece04-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ece04-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ece04-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ece04-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ece04-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ece04-123">CommonParameters</span></span>

<span data-ttu-id="ece04-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ece04-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ece04-125">Weitere Informationen finden Sie unter [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span><span class="sxs-lookup"><span data-stu-id="ece04-125">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="ece04-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ece04-126">INPUTS</span></span>

### <span data-ttu-id="ece04-127">Keine</span><span class="sxs-lookup"><span data-stu-id="ece04-127">None</span></span>

## <span data-ttu-id="ece04-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ece04-128">OUTPUTS</span></span>

### <span data-ttu-id="ece04-129">System. void</span><span class="sxs-lookup"><span data-stu-id="ece04-129">System.Void</span></span>

## <span data-ttu-id="ece04-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="ece04-130">NOTES</span></span>

## <span data-ttu-id="ece04-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ece04-131">RELATED LINKS</span></span>

[<span data-ttu-id="ece04-132">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="ece04-132">Enable-AzDataCollection</span></span>](./Enable-AzDataCollection.md)
