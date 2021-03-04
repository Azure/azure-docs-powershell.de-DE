---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/get-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
ms.openlocfilehash: b94a7158830530be9df31531101c9c9c5be90df1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938992"
---
# <span data-ttu-id="5dc24-101">Get-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="5dc24-101">Get-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="5dc24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5dc24-102">SYNOPSIS</span></span>
<span data-ttu-id="5dc24-103">Listet die API-Schlüssel für ein Mitglied der Blockkette auf.</span><span class="sxs-lookup"><span data-stu-id="5dc24-103">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="5dc24-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5dc24-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5dc24-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5dc24-105">DESCRIPTION</span></span>
<span data-ttu-id="5dc24-106">Listet die API-Schlüssel für ein Mitglied der Blockkette auf.</span><span class="sxs-lookup"><span data-stu-id="5dc24-106">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="5dc24-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5dc24-107">EXAMPLES</span></span>

### <span data-ttu-id="5dc24-108">Beispiel 1: Auflisten von Schlüsseln für die Blockkette</span><span class="sxs-lookup"><span data-stu-id="5dc24-108">Example 1: List blockchain Api keys</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

KeyName Value
------- -----
key1    72_8u5HPZJxtZmtvm4Y4W9o-
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="5dc24-109">In diesem Befehl werden die Api-Schlüssel für ein Element der Blockkette aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="5dc24-109">This command lists Api keys for a blockchain member.</span></span>

## <span data-ttu-id="5dc24-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5dc24-110">PARAMETERS</span></span>

### <span data-ttu-id="5dc24-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="5dc24-111">-BlockchainMemberName</span></span>
<span data-ttu-id="5dc24-112">Name des Mitgliedes der Blockkette.</span><span class="sxs-lookup"><span data-stu-id="5dc24-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="5dc24-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dc24-113">-DefaultProfile</span></span>
<span data-ttu-id="5dc24-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5dc24-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5dc24-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dc24-115">-ResourceGroupName</span></span>
<span data-ttu-id="5dc24-116">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="5dc24-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="5dc24-117">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="5dc24-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="5dc24-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5dc24-118">-SubscriptionId</span></span>
<span data-ttu-id="5dc24-119">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5dc24-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="5dc24-120">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="5dc24-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5dc24-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5dc24-121">-Confirm</span></span>
<span data-ttu-id="5dc24-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5dc24-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5dc24-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5dc24-123">-WhatIf</span></span>
<span data-ttu-id="5dc24-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5dc24-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5dc24-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5dc24-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5dc24-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dc24-126">CommonParameters</span></span>
<span data-ttu-id="5dc24-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dc24-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dc24-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5dc24-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dc24-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5dc24-129">INPUTS</span></span>

## <span data-ttu-id="5dc24-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5dc24-130">OUTPUTS</span></span>

### <span data-ttu-id="5dc24-131">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="5dc24-131">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="5dc24-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5dc24-132">NOTES</span></span>

<span data-ttu-id="5dc24-133">ALIASE</span><span class="sxs-lookup"><span data-stu-id="5dc24-133">ALIASES</span></span>

## <span data-ttu-id="5dc24-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5dc24-134">RELATED LINKS</span></span>

