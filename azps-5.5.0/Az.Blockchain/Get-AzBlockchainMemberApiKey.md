---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 646d07646ff7530dc805d4c516a1cf981aafe915
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145193"
---
# <span data-ttu-id="e21c0-101">Get-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="e21c0-101">Get-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="e21c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e21c0-102">SYNOPSIS</span></span>
<span data-ttu-id="e21c0-103">Listet die API-Schlüssel für ein Mitglied auf.</span><span class="sxs-lookup"><span data-stu-id="e21c0-103">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="e21c0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e21c0-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e21c0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e21c0-105">DESCRIPTION</span></span>
<span data-ttu-id="e21c0-106">Listet die API-Schlüssel für ein Mitglied auf.</span><span class="sxs-lookup"><span data-stu-id="e21c0-106">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="e21c0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e21c0-107">EXAMPLES</span></span>

### <span data-ttu-id="e21c0-108">Beispiel 1: Auflisten der api-Schlüssel</span><span class="sxs-lookup"><span data-stu-id="e21c0-108">Example 1: List blockchain Api keys</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

KeyName Value
------- -----
key1    72_8u5HPZJxtZmtvm4Y4W9o-
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="e21c0-109">Dieser Befehl listet die API-Schlüssel für ein Mitglied auf.</span><span class="sxs-lookup"><span data-stu-id="e21c0-109">This command lists Api keys for a blockchain member.</span></span>

## <span data-ttu-id="e21c0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e21c0-110">PARAMETERS</span></span>

### <span data-ttu-id="e21c0-111">-DestemberName</span><span class="sxs-lookup"><span data-stu-id="e21c0-111">-BlockchainMemberName</span></span>
<span data-ttu-id="e21c0-112">Name des Mitgliedes.</span><span class="sxs-lookup"><span data-stu-id="e21c0-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="e21c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e21c0-113">-DefaultProfile</span></span>
<span data-ttu-id="e21c0-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e21c0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e21c0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e21c0-115">-ResourceGroupName</span></span>
<span data-ttu-id="e21c0-116">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="e21c0-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e21c0-117">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="e21c0-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e21c0-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e21c0-118">-SubscriptionId</span></span>
<span data-ttu-id="e21c0-119">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e21c0-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e21c0-120">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="e21c0-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e21c0-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e21c0-121">-Confirm</span></span>
<span data-ttu-id="e21c0-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e21c0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e21c0-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e21c0-123">-WhatIf</span></span>
<span data-ttu-id="e21c0-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e21c0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e21c0-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e21c0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e21c0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e21c0-126">CommonParameters</span></span>
<span data-ttu-id="e21c0-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e21c0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e21c0-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e21c0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e21c0-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e21c0-129">INPUTS</span></span>

## <span data-ttu-id="e21c0-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e21c0-130">OUTPUTS</span></span>

### <span data-ttu-id="e21c0-131">Microsoft.Azure.PowerShell.Cmdlets.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="e21c0-131">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="e21c0-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e21c0-132">NOTES</span></span>

<span data-ttu-id="e21c0-133">ALIASE</span><span class="sxs-lookup"><span data-stu-id="e21c0-133">ALIASES</span></span>

## <span data-ttu-id="e21c0-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e21c0-134">RELATED LINKS</span></span>

