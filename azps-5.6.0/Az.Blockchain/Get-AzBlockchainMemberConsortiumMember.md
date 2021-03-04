---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/get-azblockchainmemberconsortiummember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
ms.openlocfilehash: 19901a3834716e1f2b04102c4904c059fab29397
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928368"
---
# <span data-ttu-id="b5f6e-101">Get-AzBlockchainMemberConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="b5f6e-101">Get-AzBlockchainMemberConsortiumMember</span></span>

## <span data-ttu-id="b5f6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5f6e-102">SYNOPSIS</span></span>
<span data-ttu-id="b5f6e-103">Listet die Mitglieder des Consortiums für ein Mitglied der Blockkette auf.</span><span class="sxs-lookup"><span data-stu-id="b5f6e-103">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="b5f6e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b5f6e-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b5f6e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b5f6e-105">DESCRIPTION</span></span>
<span data-ttu-id="b5f6e-106">Listet die Mitglieder des Consortiums für ein Mitglied der Blockkette auf.</span><span class="sxs-lookup"><span data-stu-id="b5f6e-106">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="b5f6e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b5f6e-107">EXAMPLES</span></span>

### <span data-ttu-id="b5f6e-108">Beispiel 1: Listet die Mitglieder des Consortiums für ein Mitglied der Blockkette auf.</span><span class="sxs-lookup"><span data-stu-id="b5f6e-108">Example 1: Lists the consortium members for a blockchain member.</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

DateModified          DisplayName JoinDate              Name       Role  Status SubscriptionId
------------          ----------- --------              ----       ----  ------ --------------
11/19/2019 5:14:41 AM dolauli001  11/19/2019 5:01:20 AM dolauli001 ADMIN Ready  c9cbd920-c00c-427c-852b-8aaf38badaeb
```

<span data-ttu-id="b5f6e-109">Mit diesem Befehl werden die Mitglieder des Consortiums für ein Mitglied der Blockkette aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b5f6e-109">This command lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="b5f6e-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b5f6e-110">PARAMETERS</span></span>

### <span data-ttu-id="b5f6e-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="b5f6e-111">-BlockchainMemberName</span></span>
<span data-ttu-id="b5f6e-112">Name des Mitgliedes der Blockkette.</span><span class="sxs-lookup"><span data-stu-id="b5f6e-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="b5f6e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5f6e-113">-DefaultProfile</span></span>
<span data-ttu-id="b5f6e-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b5f6e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5f6e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5f6e-115">-ResourceGroupName</span></span>
<span data-ttu-id="b5f6e-116">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="b5f6e-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b5f6e-117">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="b5f6e-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b5f6e-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b5f6e-118">-SubscriptionId</span></span>
<span data-ttu-id="b5f6e-119">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b5f6e-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b5f6e-120">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="b5f6e-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b5f6e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5f6e-121">CommonParameters</span></span>
<span data-ttu-id="b5f6e-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5f6e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5f6e-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5f6e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5f6e-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b5f6e-124">INPUTS</span></span>

## <span data-ttu-id="b5f6e-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b5f6e-125">OUTPUTS</span></span>

### <span data-ttu-id="b5f6e-126">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="b5f6e-126">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortiumMember</span></span>

## <span data-ttu-id="b5f6e-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b5f6e-127">NOTES</span></span>

<span data-ttu-id="b5f6e-128">ALIASE</span><span class="sxs-lookup"><span data-stu-id="b5f6e-128">ALIASES</span></span>

## <span data-ttu-id="b5f6e-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b5f6e-129">RELATED LINKS</span></span>

