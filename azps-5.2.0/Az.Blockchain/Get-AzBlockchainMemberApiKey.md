---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 646d07646ff7530dc805d4c516a1cf981aafe915
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294761"
---
# <span data-ttu-id="a07df-101">Get-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="a07df-101">Get-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="a07df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a07df-102">SYNOPSIS</span></span>
<span data-ttu-id="a07df-103">Listet die API-Schlüssel für ein Mitglied auf.</span><span class="sxs-lookup"><span data-stu-id="a07df-103">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="a07df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a07df-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a07df-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a07df-105">DESCRIPTION</span></span>
<span data-ttu-id="a07df-106">Listet die API-Schlüssel für ein Mitglied auf.</span><span class="sxs-lookup"><span data-stu-id="a07df-106">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="a07df-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a07df-107">EXAMPLES</span></span>

### <span data-ttu-id="a07df-108">Beispiel 1: Auflisten der api-Schlüssel</span><span class="sxs-lookup"><span data-stu-id="a07df-108">Example 1: List blockchain Api keys</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

KeyName Value
------- -----
key1    72_8u5HPZJxtZmtvm4Y4W9o-
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="a07df-109">Dieser Befehl listet die API-Schlüssel für ein Mitglied auf.</span><span class="sxs-lookup"><span data-stu-id="a07df-109">This command lists Api keys for a blockchain member.</span></span>

## <span data-ttu-id="a07df-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a07df-110">PARAMETERS</span></span>

### <span data-ttu-id="a07df-111">-DestemberName</span><span class="sxs-lookup"><span data-stu-id="a07df-111">-BlockchainMemberName</span></span>
<span data-ttu-id="a07df-112">Name des Mitgliedes.</span><span class="sxs-lookup"><span data-stu-id="a07df-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="a07df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a07df-113">-DefaultProfile</span></span>
<span data-ttu-id="a07df-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a07df-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a07df-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a07df-115">-ResourceGroupName</span></span>
<span data-ttu-id="a07df-116">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="a07df-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a07df-117">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="a07df-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a07df-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a07df-118">-SubscriptionId</span></span>
<span data-ttu-id="a07df-119">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a07df-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a07df-120">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="a07df-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a07df-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a07df-121">-Confirm</span></span>
<span data-ttu-id="a07df-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a07df-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a07df-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a07df-123">-WhatIf</span></span>
<span data-ttu-id="a07df-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a07df-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a07df-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a07df-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a07df-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a07df-126">CommonParameters</span></span>
<span data-ttu-id="a07df-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a07df-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a07df-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a07df-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a07df-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a07df-129">INPUTS</span></span>

## <span data-ttu-id="a07df-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a07df-130">OUTPUTS</span></span>

### <span data-ttu-id="a07df-131">Microsoft.Azure.PowerShell.Cmdlets.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="a07df-131">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="a07df-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a07df-132">NOTES</span></span>

<span data-ttu-id="a07df-133">ALIASE</span><span class="sxs-lookup"><span data-stu-id="a07df-133">ALIASES</span></span>

## <span data-ttu-id="a07df-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a07df-134">RELATED LINKS</span></span>

