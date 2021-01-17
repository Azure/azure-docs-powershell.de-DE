---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainconsortium
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
ms.openlocfilehash: d34e8257d6946476ff5b6a2356ba9b1b06d8a9f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471062"
---
# <span data-ttu-id="81fed-101">Get-AzBlockchainConsortium</span><span class="sxs-lookup"><span data-stu-id="81fed-101">Get-AzBlockchainConsortium</span></span>

## <span data-ttu-id="81fed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81fed-102">SYNOPSIS</span></span>
<span data-ttu-id="81fed-103">Listet die verfügbaren Consortiums für ein Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="81fed-103">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="81fed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81fed-104">SYNTAX</span></span>

```
Get-AzBlockchainConsortium -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="81fed-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="81fed-105">DESCRIPTION</span></span>
<span data-ttu-id="81fed-106">Listet die verfügbaren Consortiums für ein Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="81fed-106">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="81fed-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="81fed-107">EXAMPLES</span></span>

### <span data-ttu-id="81fed-108">Beispiel 1: Get Consortiums.</span><span class="sxs-lookup"><span data-stu-id="81fed-108">Example 1: Get Blockchain consortiums.</span></span>
```powershell
PS C:\> Get-AzBlockchainConsortium -Location eastus

```

<span data-ttu-id="81fed-109">Mit diesem Befehl werden die Consortiums unter einem Abonnement für einen bestimmten Standort aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="81fed-109">This command lists the consortiums under a subscription for a specific location.</span></span>

## <span data-ttu-id="81fed-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81fed-110">PARAMETERS</span></span>

### <span data-ttu-id="81fed-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81fed-111">-DefaultProfile</span></span>
<span data-ttu-id="81fed-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="81fed-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81fed-113">-Location</span><span class="sxs-lookup"><span data-stu-id="81fed-113">-Location</span></span>
<span data-ttu-id="81fed-114">Standortname.</span><span class="sxs-lookup"><span data-stu-id="81fed-114">Location Name.</span></span>

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

### <span data-ttu-id="81fed-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="81fed-115">-SubscriptionId</span></span>
<span data-ttu-id="81fed-116">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="81fed-116">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="81fed-117">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="81fed-117">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81fed-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81fed-118">-Confirm</span></span>
<span data-ttu-id="81fed-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="81fed-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81fed-120">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="81fed-120">-WhatIf</span></span>
<span data-ttu-id="81fed-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="81fed-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81fed-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="81fed-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81fed-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81fed-123">CommonParameters</span></span>
<span data-ttu-id="81fed-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81fed-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81fed-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81fed-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81fed-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="81fed-126">INPUTS</span></span>

## <span data-ttu-id="81fed-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="81fed-127">OUTPUTS</span></span>

### <span data-ttu-id="81fed-128">Microsoft.Azure.PowerShell.Cmdlets.Feeds.Models.Api20180601Preview.IConsortium</span><span class="sxs-lookup"><span data-stu-id="81fed-128">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortium</span></span>

## <span data-ttu-id="81fed-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="81fed-129">NOTES</span></span>

<span data-ttu-id="81fed-130">ALIASE</span><span class="sxs-lookup"><span data-stu-id="81fed-130">ALIASES</span></span>

## <span data-ttu-id="81fed-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="81fed-131">RELATED LINKS</span></span>

