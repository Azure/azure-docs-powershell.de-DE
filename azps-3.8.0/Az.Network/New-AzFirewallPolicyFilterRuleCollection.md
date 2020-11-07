---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyfilterrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
ms.openlocfilehash: d5871a9e1a99a27cc0b2728ca3638a0548f42fc6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93844987"
---
# <span data-ttu-id="360fa-101">New-AzFirewallPolicyFilterRuleCollection</span><span class="sxs-lookup"><span data-stu-id="360fa-101">New-AzFirewallPolicyFilterRuleCollection</span></span>

## <span data-ttu-id="360fa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="360fa-102">SYNOPSIS</span></span>
<span data-ttu-id="360fa-103">Erstellen einer neuen Azure Firewall-Richtlinien Filter-Regelsammlung</span><span class="sxs-lookup"><span data-stu-id="360fa-103">Create a new Azure Firewall Policy Filter Rule Collection</span></span>

## <span data-ttu-id="360fa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="360fa-104">SYNTAX</span></span>

```
New-AzFirewallPolicyFilterRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallPolicyRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="360fa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="360fa-105">DESCRIPTION</span></span>
<span data-ttu-id="360fa-106">Das Cmdlet **New-AzFirewallPolicyFilterRuleCollection** erstellt eine Filter Regelsammlung für eine Azure-Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="360fa-106">The **New-AzFirewallPolicyFilterRuleCollection** cmdlet creates a Filter rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="360fa-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="360fa-107">EXAMPLES</span></span>

### <span data-ttu-id="360fa-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="360fa-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyFilterRuleCollection -Name FR1 -Priority 400 -Rule $appRule1 ,$appRule2 -ActionType "Allow"
```

<span data-ttu-id="360fa-109">In diesem Beispiel wird eine Filter Regel mit 2 Regelbedingungen erstellt</span><span class="sxs-lookup"><span data-stu-id="360fa-109">This example creates a Filter rule with 2 rule conditions</span></span>

## <span data-ttu-id="360fa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="360fa-110">PARAMETERS</span></span>

### <span data-ttu-id="360fa-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="360fa-111">-ActionType</span></span>
<span data-ttu-id="360fa-112">Die Aktion der Regelsammlung</span><span class="sxs-lookup"><span data-stu-id="360fa-112">The action of the rule collection</span></span>

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

### <span data-ttu-id="360fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="360fa-113">-DefaultProfile</span></span>
<span data-ttu-id="360fa-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="360fa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="360fa-115">-Name</span><span class="sxs-lookup"><span data-stu-id="360fa-115">-Name</span></span>
<span data-ttu-id="360fa-116">Der Name der Anwendungsregel Sammlung</span><span class="sxs-lookup"><span data-stu-id="360fa-116">The name of the Application Rule Collection</span></span>

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

### <span data-ttu-id="360fa-117">-Priorität</span><span class="sxs-lookup"><span data-stu-id="360fa-117">-Priority</span></span>
<span data-ttu-id="360fa-118">Die Priorität der Regelsammlung</span><span class="sxs-lookup"><span data-stu-id="360fa-118">The priority of the rule collection</span></span>

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

### <span data-ttu-id="360fa-119">-Rule</span><span class="sxs-lookup"><span data-stu-id="360fa-119">-Rule</span></span>
<span data-ttu-id="360fa-120">Die Liste der Anwendungsregeln</span><span class="sxs-lookup"><span data-stu-id="360fa-120">The list of application rules</span></span>

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

### <span data-ttu-id="360fa-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="360fa-121">-Confirm</span></span>
<span data-ttu-id="360fa-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="360fa-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="360fa-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="360fa-123">-WhatIf</span></span>
<span data-ttu-id="360fa-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="360fa-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="360fa-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="360fa-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="360fa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="360fa-126">CommonParameters</span></span>
<span data-ttu-id="360fa-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="360fa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="360fa-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="360fa-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="360fa-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="360fa-129">INPUTS</span></span>

### <span data-ttu-id="360fa-130">Keine</span><span class="sxs-lookup"><span data-stu-id="360fa-130">None</span></span>

## <span data-ttu-id="360fa-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="360fa-131">OUTPUTS</span></span>

### <span data-ttu-id="360fa-132">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="360fa-132">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="360fa-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="360fa-133">NOTES</span></span>

## <span data-ttu-id="360fa-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="360fa-134">RELATED LINKS</span></span>
