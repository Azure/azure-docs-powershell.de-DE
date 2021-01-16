---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 401073a8d97affaec866486b19113373c001ae58
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98299059"
---
# <span data-ttu-id="b339a-101">Get-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="b339a-101">Get-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="b339a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b339a-102">SYNOPSIS</span></span>
<span data-ttu-id="b339a-103">Listen Sie die API-Schlüssel für den Transaktionsknoten auf.</span><span class="sxs-lookup"><span data-stu-id="b339a-103">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="b339a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b339a-104">SYNTAX</span></span>

```
Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="b339a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b339a-105">DESCRIPTION</span></span>
<span data-ttu-id="b339a-106">Listen Sie die API-Schlüssel für den Transaktionsknoten auf.</span><span class="sxs-lookup"><span data-stu-id="b339a-106">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="b339a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b339a-107">EXAMPLES</span></span>

### <span data-ttu-id="b339a-108">Beispiel 1: Listen-API-Schlüssel für einen Transaktionsknoten</span><span class="sxs-lookup"><span data-stu-id="b339a-108">Example 1: List Api keys for a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001

KeyName Value
------- -----
key1    H4_GPhxbqYENxwas4Vc4l5U9
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="b339a-109">Dieser Befehl listet die API-Schlüssel für einen Transaktionsknoten auf.</span><span class="sxs-lookup"><span data-stu-id="b339a-109">This command lists Api keys for a transaction node.</span></span>

## <span data-ttu-id="b339a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b339a-110">PARAMETERS</span></span>

### <span data-ttu-id="b339a-111">-DestemberName</span><span class="sxs-lookup"><span data-stu-id="b339a-111">-BlockchainMemberName</span></span>
<span data-ttu-id="b339a-112">Name des Mitgliedes.</span><span class="sxs-lookup"><span data-stu-id="b339a-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="b339a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b339a-113">-DefaultProfile</span></span>
<span data-ttu-id="b339a-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b339a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b339a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b339a-115">-ResourceGroupName</span></span>
<span data-ttu-id="b339a-116">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="b339a-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b339a-117">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="b339a-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b339a-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b339a-118">-SubscriptionId</span></span>
<span data-ttu-id="b339a-119">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b339a-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b339a-120">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="b339a-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b339a-121">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="b339a-121">-TransactionNodeName</span></span>
<span data-ttu-id="b339a-122">Name des Transaktionsknotens.</span><span class="sxs-lookup"><span data-stu-id="b339a-122">Transaction node name.</span></span>

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

### <span data-ttu-id="b339a-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b339a-123">-Confirm</span></span>
<span data-ttu-id="b339a-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b339a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b339a-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b339a-125">-WhatIf</span></span>
<span data-ttu-id="b339a-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b339a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b339a-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b339a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b339a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b339a-128">CommonParameters</span></span>
<span data-ttu-id="b339a-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b339a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b339a-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b339a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b339a-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b339a-131">INPUTS</span></span>

## <span data-ttu-id="b339a-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b339a-132">OUTPUTS</span></span>

### <span data-ttu-id="b339a-133">Microsoft.Azure.PowerShell.Cmdlets.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="b339a-133">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="b339a-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b339a-134">NOTES</span></span>

<span data-ttu-id="b339a-135">ALIASE</span><span class="sxs-lookup"><span data-stu-id="b339a-135">ALIASES</span></span>

## <span data-ttu-id="b339a-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b339a-136">RELATED LINKS</span></span>

