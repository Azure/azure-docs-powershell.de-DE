---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicyintrusiondetectionbypasstraffic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionBypassTraffic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionBypassTraffic.md
ms.openlocfilehash: dd15a93fc2df022a0b016f9dae4845da13240534
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933464"
---
# <span data-ttu-id="b2b05-101">New-AzFirewallPolicyIntrusionDetectionBypassTraffic</span><span class="sxs-lookup"><span data-stu-id="b2b05-101">New-AzFirewallPolicyIntrusionDetectionBypassTraffic</span></span>

## <span data-ttu-id="b2b05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2b05-102">SYNOPSIS</span></span>
<span data-ttu-id="b2b05-103">Erstellt eine neue Einstellung für die Erkennung von Datenverkehrsumgehungen durch Azure Firewall-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="b2b05-103">Creates a new Azure Firewall Policy Intrusion Detection Bypass Traffic Setting</span></span>

## <span data-ttu-id="b2b05-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2b05-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name <String> [-Description <String>] -Protocol <String>
 [-SourceAddress <String[]>] [-DestinationAddress <String[]>] [-SourceIpGroup <String[]>]
 [-DestinationIpGroup <String[]>] -DestinationPort <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2b05-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2b05-105">DESCRIPTION</span></span>
<span data-ttu-id="b2b05-106">Das **Cmdlet New-AzFirewallPolicyIntrusionDetectionBypassTraffic** erstellt ein Azure Firewall Policy Intrusion Detection Bypass Traffic Object.</span><span class="sxs-lookup"><span data-stu-id="b2b05-106">The **New-AzFirewallPolicyIntrusionDetectionBypassTraffic** cmdlet creates an Azure Firewall Policy Intrusion Detection Bypass Traffic Object.</span></span>

## <span data-ttu-id="b2b05-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b2b05-107">EXAMPLES</span></span>

### <span data-ttu-id="b2b05-108">Beispiel 1: 1.</span><span class="sxs-lookup"><span data-stu-id="b2b05-108">Example 1: 1.</span></span> <span data-ttu-id="b2b05-109">Erstellen von Umgehungsverkehr mit einer bestimmten Port- und Quelladresse</span><span class="sxs-lookup"><span data-stu-id="b2b05-109">Create bypass traffic with specific port and source address</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress "*"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Deny" -BypassTraffic $bypass
```

<span data-ttu-id="b2b05-110">In diesem Beispiel wird die Erkennung von Eindringversuchen mit der Einstellung "Umgehung des Datenverkehrs" erstellt.</span><span class="sxs-lookup"><span data-stu-id="b2b05-110">This example creates intrusion detection with bypass traffic setting</span></span>

## <span data-ttu-id="b2b05-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b2b05-111">PARAMETERS</span></span>

### <span data-ttu-id="b2b05-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2b05-112">-DefaultProfile</span></span>
<span data-ttu-id="b2b05-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b2b05-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2b05-114">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2b05-114">-Description</span></span>
<span data-ttu-id="b2b05-115">Beschreibung der Einstellung umgehen.</span><span class="sxs-lookup"><span data-stu-id="b2b05-115">Bypass setting description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2b05-116">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="b2b05-116">-DestinationAddress</span></span>
<span data-ttu-id="b2b05-117">Liste der ZIEL-IP-Adressen oder -Bereiche.</span><span class="sxs-lookup"><span data-stu-id="b2b05-117">List of destination IP addresses or ranges.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2b05-118">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="b2b05-118">-DestinationIpGroup</span></span>
<span data-ttu-id="b2b05-119">Liste der Ziel-IpGroups.</span><span class="sxs-lookup"><span data-stu-id="b2b05-119">List of destination IpGroups.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2b05-120">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="b2b05-120">-DestinationPort</span></span>
<span data-ttu-id="b2b05-121">Liste der Zielports oder -bereiche.</span><span class="sxs-lookup"><span data-stu-id="b2b05-121">List of destination ports or ranges.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2b05-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b2b05-122">-Name</span></span>
<span data-ttu-id="b2b05-123">Umgehen des Einstellungsnamens.</span><span class="sxs-lookup"><span data-stu-id="b2b05-123">Bypass setting name.</span></span>

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

### <span data-ttu-id="b2b05-124">-Protocol</span><span class="sxs-lookup"><span data-stu-id="b2b05-124">-Protocol</span></span>
<span data-ttu-id="b2b05-125">Umgehung des Einstellungsprotokolls.</span><span class="sxs-lookup"><span data-stu-id="b2b05-125">Bypass setting protocol.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: TCP, UDP, ICMP, ANY

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2b05-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="b2b05-126">-SourceAddress</span></span>
<span data-ttu-id="b2b05-127">Liste der Quell-IP-Adressen oder -Bereiche.</span><span class="sxs-lookup"><span data-stu-id="b2b05-127">List of source IP addresses or ranges.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2b05-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="b2b05-128">-SourceIpGroup</span></span>
<span data-ttu-id="b2b05-129">Liste der Quell-IpGroups.</span><span class="sxs-lookup"><span data-stu-id="b2b05-129">List of source IpGroups.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2b05-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b2b05-130">-Confirm</span></span>
<span data-ttu-id="b2b05-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b2b05-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2b05-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2b05-132">-WhatIf</span></span>
<span data-ttu-id="b2b05-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b2b05-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2b05-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2b05-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2b05-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2b05-135">CommonParameters</span></span>
<span data-ttu-id="b2b05-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2b05-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2b05-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2b05-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2b05-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b2b05-138">INPUTS</span></span>

### <span data-ttu-id="b2b05-139">Keine</span><span class="sxs-lookup"><span data-stu-id="b2b05-139">None</span></span>

## <span data-ttu-id="b2b05-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b2b05-140">OUTPUTS</span></span>

### <span data-ttu-id="b2b05-141">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting</span><span class="sxs-lookup"><span data-stu-id="b2b05-141">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting</span></span>

## <span data-ttu-id="b2b05-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b2b05-142">NOTES</span></span>

## <span data-ttu-id="b2b05-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b2b05-143">RELATED LINKS</span></span>
