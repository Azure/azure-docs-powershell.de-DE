---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: a8087f41c33dc3bb066609393a87986d5016d1ae
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "94005285"
---
# <span data-ttu-id="90223-101">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="90223-101">Enable-AzDataCollection</span></span>

## <span data-ttu-id="90223-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="90223-102">SYNOPSIS</span></span>
<span data-ttu-id="90223-103">Ermöglicht Azure PowerShell das Sammeln von Daten, um die Benutzerfreundlichkeit mit den Azure PowerShell-Cmdlets zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="90223-103">Enables Azure PowerShell to collect data to improve the user experience with the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="90223-104">Das Ausführen dieses Cmdlets entscheidet sich für die Datensammlung für den aktuellen Benutzer auf dem aktuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="90223-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span> <span data-ttu-id="90223-105">Daten werden standardmäßig erfasst, es sei denn, dass Sie sich ausdrücklich entscheiden.</span><span class="sxs-lookup"><span data-stu-id="90223-105">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="90223-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="90223-106">SYNTAX</span></span>

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90223-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="90223-107">DESCRIPTION</span></span>

<span data-ttu-id="90223-108">Das `Enable-AzDataCollection` Cmdlet wird verwendet, um sich für die Datensammlung zu entscheiden.</span><span class="sxs-lookup"><span data-stu-id="90223-108">The `Enable-AzDataCollection` cmdlet is used to opt in to data collection.</span></span> <span data-ttu-id="90223-109">Azure PowerShell sammelt standardmäßig Telemetrie-Daten automatisch.</span><span class="sxs-lookup"><span data-stu-id="90223-109">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="90223-110">Microsoft aggregiert gesammelte Daten, um Nutzungsmuster zu identifizieren, häufige Probleme zu erkennen und die Erfahrung von Azure PowerShell zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="90223-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span>
<span data-ttu-id="90223-111">Microsoft Azure PowerShell sammelt keine privaten oder persönlichen Daten.</span><span class="sxs-lookup"><span data-stu-id="90223-111">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="90223-112">Wenn Sie die Datensammlung deaktivieren möchten, müssen Sie die Ausführung explizit ablehnen `Disable-AzDataCollection` .</span><span class="sxs-lookup"><span data-stu-id="90223-112">To disable data collection, you must explicitly opt out by executing `Disable-AzDataCollection`.</span></span>

## <span data-ttu-id="90223-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="90223-113">EXAMPLES</span></span>

### <span data-ttu-id="90223-114">Beispiel 1: Aktivieren der Datensammlung für den aktuellen Benutzer</span><span class="sxs-lookup"><span data-stu-id="90223-114">Example 1: Enabling data collection for the current user</span></span>

<span data-ttu-id="90223-115">Im folgenden Beispiel wird gezeigt, wie Sie die Datensammlung für den aktuellen Benutzer aktivieren.</span><span class="sxs-lookup"><span data-stu-id="90223-115">The following example shows how to enable data collection for the current user.</span></span>

```powershell
Enable-AzDataCollection
```

## <span data-ttu-id="90223-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="90223-116">PARAMETERS</span></span>

### <span data-ttu-id="90223-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90223-117">-DefaultProfile</span></span>

<span data-ttu-id="90223-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="90223-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90223-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="90223-119">-Confirm</span></span>

<span data-ttu-id="90223-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="90223-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90223-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90223-121">-WhatIf</span></span>

<span data-ttu-id="90223-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90223-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90223-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="90223-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90223-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90223-124">CommonParameters</span></span>

<span data-ttu-id="90223-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90223-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90223-126">Weitere Informationen finden Sie unter [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span><span class="sxs-lookup"><span data-stu-id="90223-126">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="90223-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="90223-127">INPUTS</span></span>

### <span data-ttu-id="90223-128">Keine</span><span class="sxs-lookup"><span data-stu-id="90223-128">None</span></span>

## <span data-ttu-id="90223-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="90223-129">OUTPUTS</span></span>

### <span data-ttu-id="90223-130">System. void</span><span class="sxs-lookup"><span data-stu-id="90223-130">System.Void</span></span>

## <span data-ttu-id="90223-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="90223-131">NOTES</span></span>

## <span data-ttu-id="90223-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="90223-132">RELATED LINKS</span></span>

[<span data-ttu-id="90223-133">Deaktivieren-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="90223-133">Disable-AzDataCollection</span></span>](./Disable-AzDataCollection.md)
