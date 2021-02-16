---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainconsortium
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
ms.openlocfilehash: d34e8257d6946476ff5b6a2356ba9b1b06d8a9f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149201"
---
# <span data-ttu-id="71164-101">Get-AzBlockchainConsortium</span><span class="sxs-lookup"><span data-stu-id="71164-101">Get-AzBlockchainConsortium</span></span>

## <span data-ttu-id="71164-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71164-102">SYNOPSIS</span></span>
<span data-ttu-id="71164-103">Listet die verfügbaren Consortiums für ein Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="71164-103">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="71164-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71164-104">SYNTAX</span></span>

```
Get-AzBlockchainConsortium -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="71164-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="71164-105">DESCRIPTION</span></span>
<span data-ttu-id="71164-106">Listet die verfügbaren Consortiums für ein Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="71164-106">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="71164-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="71164-107">EXAMPLES</span></span>

### <span data-ttu-id="71164-108">Beispiel 1: Get Consortiums.</span><span class="sxs-lookup"><span data-stu-id="71164-108">Example 1: Get Blockchain consortiums.</span></span>
```powershell
PS C:\> Get-AzBlockchainConsortium -Location eastus

```

<span data-ttu-id="71164-109">Mit diesem Befehl werden die Consortiums unter einem Abonnement für einen bestimmten Standort aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="71164-109">This command lists the consortiums under a subscription for a specific location.</span></span>

## <span data-ttu-id="71164-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71164-110">PARAMETERS</span></span>

### <span data-ttu-id="71164-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71164-111">-DefaultProfile</span></span>
<span data-ttu-id="71164-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="71164-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71164-113">-Location</span><span class="sxs-lookup"><span data-stu-id="71164-113">-Location</span></span>
<span data-ttu-id="71164-114">Standortname.</span><span class="sxs-lookup"><span data-stu-id="71164-114">Location Name.</span></span>

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

### <span data-ttu-id="71164-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="71164-115">-SubscriptionId</span></span>
<span data-ttu-id="71164-116">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="71164-116">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="71164-117">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="71164-117">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="71164-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71164-118">-Confirm</span></span>
<span data-ttu-id="71164-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="71164-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71164-120">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="71164-120">-WhatIf</span></span>
<span data-ttu-id="71164-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="71164-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71164-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="71164-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71164-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71164-123">CommonParameters</span></span>
<span data-ttu-id="71164-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71164-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71164-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71164-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71164-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="71164-126">INPUTS</span></span>

## <span data-ttu-id="71164-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="71164-127">OUTPUTS</span></span>

### <span data-ttu-id="71164-128">Microsoft.Azure.PowerShell.Cmdlets.Models.Api20180601Preview.IConsortium</span><span class="sxs-lookup"><span data-stu-id="71164-128">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortium</span></span>

## <span data-ttu-id="71164-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="71164-129">NOTES</span></span>

<span data-ttu-id="71164-130">ALIASE</span><span class="sxs-lookup"><span data-stu-id="71164-130">ALIASES</span></span>

## <span data-ttu-id="71164-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="71164-131">RELATED LINKS</span></span>

