---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyfilterrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
ms.openlocfilehash: d5871a9e1a99a27cc0b2728ca3638a0548f42fc6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469007"
---
# <span data-ttu-id="3c523-101">New-AzFirewallPolicyFilterRuleCollection</span><span class="sxs-lookup"><span data-stu-id="3c523-101">New-AzFirewallPolicyFilterRuleCollection</span></span>

## <span data-ttu-id="3c523-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c523-102">SYNOPSIS</span></span>
<span data-ttu-id="3c523-103">Erstellen einer neuen Sammlung von Filterregeln für azure-Firewallrichtlinien</span><span class="sxs-lookup"><span data-stu-id="3c523-103">Create a new Azure Firewall Policy Filter Rule Collection</span></span>

## <span data-ttu-id="3c523-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3c523-104">SYNTAX</span></span>

```
New-AzFirewallPolicyFilterRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallPolicyRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c523-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3c523-105">DESCRIPTION</span></span>
<span data-ttu-id="3c523-106">Das **Cmdlet "New-AzFirewallPolicyFilterRuleCollection"** erstellt eine Filterregelsammlung für eine Azure-Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="3c523-106">The **New-AzFirewallPolicyFilterRuleCollection** cmdlet creates a Filter rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="3c523-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3c523-107">EXAMPLES</span></span>

### <span data-ttu-id="3c523-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3c523-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyFilterRuleCollection -Name FR1 -Priority 400 -Rule $appRule1 ,$appRule2 -ActionType "Allow"
```

<span data-ttu-id="3c523-109">In diesem Beispiel wird eine Filterregel mit zwei Regelbedingungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="3c523-109">This example creates a Filter rule with 2 rule conditions</span></span>

## <span data-ttu-id="3c523-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c523-110">PARAMETERS</span></span>

### <span data-ttu-id="3c523-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="3c523-111">-ActionType</span></span>
<span data-ttu-id="3c523-112">Die Aktion der Regelsammlung</span><span class="sxs-lookup"><span data-stu-id="3c523-112">The action of the rule collection</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c523-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c523-113">-DefaultProfile</span></span>
<span data-ttu-id="3c523-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3c523-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c523-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3c523-115">-Name</span></span>
<span data-ttu-id="3c523-116">Der Name der Anwendungsregelsammlung</span><span class="sxs-lookup"><span data-stu-id="3c523-116">The name of the Application Rule Collection</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c523-117">-Priority</span><span class="sxs-lookup"><span data-stu-id="3c523-117">-Priority</span></span>
<span data-ttu-id="3c523-118">Die Priorität der Regelsammlung</span><span class="sxs-lookup"><span data-stu-id="3c523-118">The priority of the rule collection</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c523-119">-Rule</span><span class="sxs-lookup"><span data-stu-id="3c523-119">-Rule</span></span>
<span data-ttu-id="3c523-120">Die Liste der Anwendungsregeln</span><span class="sxs-lookup"><span data-stu-id="3c523-120">The list of application rules</span></span>

```yaml
Type: PSAzureFirewallPolicyRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c523-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c523-121">-Confirm</span></span>
<span data-ttu-id="3c523-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3c523-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c523-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3c523-123">-WhatIf</span></span>
<span data-ttu-id="3c523-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3c523-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c523-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3c523-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c523-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c523-126">CommonParameters</span></span>
<span data-ttu-id="3c523-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c523-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c523-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c523-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c523-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3c523-129">INPUTS</span></span>

### <span data-ttu-id="3c523-130">Keine</span><span class="sxs-lookup"><span data-stu-id="3c523-130">None</span></span>

## <span data-ttu-id="3c523-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3c523-131">OUTPUTS</span></span>

### <span data-ttu-id="3c523-132">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="3c523-132">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="3c523-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3c523-133">NOTES</span></span>

## <span data-ttu-id="3c523-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3c523-134">RELATED LINKS</span></span>
