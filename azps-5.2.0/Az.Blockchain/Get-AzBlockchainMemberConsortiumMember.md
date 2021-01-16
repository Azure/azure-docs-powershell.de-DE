---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmemberconsortiummember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
ms.openlocfilehash: f4dc342d72ce092a1f3cbd1695613fce2220661d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98299064"
---
# <span data-ttu-id="00e30-101">Get-AzBlockchainMemberConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="00e30-101">Get-AzBlockchainMemberConsortiumMember</span></span>

## <span data-ttu-id="00e30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00e30-102">SYNOPSIS</span></span>
<span data-ttu-id="00e30-103">Listet die Mitglieder des Consortiums für ein Mitglied auf.</span><span class="sxs-lookup"><span data-stu-id="00e30-103">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="00e30-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00e30-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="00e30-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="00e30-105">DESCRIPTION</span></span>
<span data-ttu-id="00e30-106">Listet die Mitglieder des Consortiums für ein Mitglied auf.</span><span class="sxs-lookup"><span data-stu-id="00e30-106">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="00e30-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="00e30-107">EXAMPLES</span></span>

### <span data-ttu-id="00e30-108">Beispiel 1: Listet die Consortiummitglieder für ein Mitglied auf.</span><span class="sxs-lookup"><span data-stu-id="00e30-108">Example 1: Lists the consortium members for a blockchain member.</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

DateModified          DisplayName JoinDate              Name       Role  Status SubscriptionId
------------          ----------- --------              ----       ----  ------ --------------
11/19/2019 5:14:41 AM dolauli001  11/19/2019 5:01:20 AM dolauli001 ADMIN Ready  c9cbd920-c00c-427c-852b-8aaf38badaeb
```

<span data-ttu-id="00e30-109">Mit diesem Befehl werden die Mitglieder des Consortiums für ein Mitglied des Consortiums aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="00e30-109">This command lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="00e30-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00e30-110">PARAMETERS</span></span>

### <span data-ttu-id="00e30-111">-DestemberName</span><span class="sxs-lookup"><span data-stu-id="00e30-111">-BlockchainMemberName</span></span>
<span data-ttu-id="00e30-112">Name des Mitgliedes.</span><span class="sxs-lookup"><span data-stu-id="00e30-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="00e30-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00e30-113">-DefaultProfile</span></span>
<span data-ttu-id="00e30-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00e30-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00e30-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00e30-115">-ResourceGroupName</span></span>
<span data-ttu-id="00e30-116">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="00e30-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="00e30-117">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="00e30-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="00e30-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="00e30-118">-SubscriptionId</span></span>
<span data-ttu-id="00e30-119">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="00e30-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="00e30-120">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="00e30-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="00e30-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00e30-121">CommonParameters</span></span>
<span data-ttu-id="00e30-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00e30-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00e30-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00e30-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00e30-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="00e30-124">INPUTS</span></span>

## <span data-ttu-id="00e30-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="00e30-125">OUTPUTS</span></span>

### <span data-ttu-id="00e30-126">Microsoft.Azure.PowerShell.Cmdlets.Ial.Models.Api20180601Preview.IConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="00e30-126">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortiumMember</span></span>

## <span data-ttu-id="00e30-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="00e30-127">NOTES</span></span>

<span data-ttu-id="00e30-128">ALIASE</span><span class="sxs-lookup"><span data-stu-id="00e30-128">ALIASES</span></span>

## <span data-ttu-id="00e30-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="00e30-129">RELATED LINKS</span></span>

