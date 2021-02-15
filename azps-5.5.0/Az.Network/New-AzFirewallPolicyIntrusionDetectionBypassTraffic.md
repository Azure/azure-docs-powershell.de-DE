---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyintrusiondetectionbypasstraffic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionBypassTraffic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionBypassTraffic.md
ms.openlocfilehash: c296c44c96d756dc0ca3a107d8eee265a9226b15
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151713"
---
# <span data-ttu-id="6d9ea-101">New-AzFirewallPolicyIntrusionDetectionBypassTraffic</span><span class="sxs-lookup"><span data-stu-id="6d9ea-101">New-AzFirewallPolicyIntrusionDetectionBypassTraffic</span></span>

## <span data-ttu-id="6d9ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d9ea-102">SYNOPSIS</span></span>
<span data-ttu-id="6d9ea-103">Erstellt eine neue Einstellung für die Umgehung des Datenverkehrs in der Azure-Firewall-Richtlinienerkennung.</span><span class="sxs-lookup"><span data-stu-id="6d9ea-103">Creates a new Azure Firewall Policy Intrusion Detection Bypass Traffic Setting</span></span>

## <span data-ttu-id="6d9ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d9ea-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name <String> [-Description <String>] -Protocol <String>
 [-SourceAddress <String[]>] [-DestinationAddress <String[]>] [-SourceIpGroup <String[]>]
 [-DestinationIpGroup <String[]>] -DestinationPort <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d9ea-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d9ea-105">DESCRIPTION</span></span>
<span data-ttu-id="6d9ea-106">Das **Cmdlet "New-AzFirewallPolicyIntrusionDetectionBypassTraffic"** erstellt ein Datenverkehrsobjekt für die Umgehung des Datenverkehrs durch die Azure Firewall Policy Bypass.</span><span class="sxs-lookup"><span data-stu-id="6d9ea-106">The **New-AzFirewallPolicyIntrusionDetectionBypassTraffic** cmdlet creates an Azure Firewall Policy Intrusion Detection Bypass Traffic Object.</span></span>

## <span data-ttu-id="6d9ea-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6d9ea-107">EXAMPLES</span></span>

### <span data-ttu-id="6d9ea-108">Beispiel 1: 1.</span><span class="sxs-lookup"><span data-stu-id="6d9ea-108">Example 1: 1.</span></span> <span data-ttu-id="6d9ea-109">Erstellen von Umgehungsverkehr mit einer bestimmten Port- und Quelladresse</span><span class="sxs-lookup"><span data-stu-id="6d9ea-109">Create bypass traffic with specific port and source address</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress "*"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Deny" -BypassTraffic $bypass
```

<span data-ttu-id="6d9ea-110">In diesem Beispiel wird die Angriffserkennung mit Einstellung für die Umgehung des Datenverkehrs erstellt.</span><span class="sxs-lookup"><span data-stu-id="6d9ea-110">This example creates intrusion detection with bypass traffic setting</span></span>

## <span data-ttu-id="6d9ea-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d9ea-111">PARAMETERS</span></span>

### <span data-ttu-id="6d9ea-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d9ea-112">-DefaultProfile</span></span>
<span data-ttu-id="6d9ea-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6d9ea-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d9ea-114">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6d9ea-114">-Description</span></span>
<span data-ttu-id="6d9ea-115">Beschreibung der Umgehungseinstellung</span><span class="sxs-lookup"><span data-stu-id="6d9ea-115">Bypass setting description.</span></span>

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

### <span data-ttu-id="6d9ea-116">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="6d9ea-116">-DestinationAddress</span></span>
<span data-ttu-id="6d9ea-117">Liste der Ziel-IP-Adressen oder -Bereiche.</span><span class="sxs-lookup"><span data-stu-id="6d9ea-117">List of destination IP addresses or ranges.</span></span>

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

### <span data-ttu-id="6d9ea-118">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="6d9ea-118">-DestinationIpGroup</span></span>
<span data-ttu-id="6d9ea-119">Liste der Ziel-IpGroups.</span><span class="sxs-lookup"><span data-stu-id="6d9ea-119">List of destination IpGroups.</span></span>

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

### <span data-ttu-id="6d9ea-120">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="6d9ea-120">-DestinationPort</span></span>
<span data-ttu-id="6d9ea-121">Liste der Zielports oder -bereiche.</span><span class="sxs-lookup"><span data-stu-id="6d9ea-121">List of destination ports or ranges.</span></span>

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

### <span data-ttu-id="6d9ea-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6d9ea-122">-Name</span></span>
<span data-ttu-id="6d9ea-123">Name der Einstellung umgehen.</span><span class="sxs-lookup"><span data-stu-id="6d9ea-123">Bypass setting name.</span></span>

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

### <span data-ttu-id="6d9ea-124">-Protocol</span><span class="sxs-lookup"><span data-stu-id="6d9ea-124">-Protocol</span></span>
<span data-ttu-id="6d9ea-125">Umgehungseinstellungsprotokoll.</span><span class="sxs-lookup"><span data-stu-id="6d9ea-125">Bypass setting protocol.</span></span>

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

### <span data-ttu-id="6d9ea-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="6d9ea-126">-SourceAddress</span></span>
<span data-ttu-id="6d9ea-127">Liste der IP-Quelladressen oder -bereiche.</span><span class="sxs-lookup"><span data-stu-id="6d9ea-127">List of source IP addresses or ranges.</span></span>

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

### <span data-ttu-id="6d9ea-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="6d9ea-128">-SourceIpGroup</span></span>
<span data-ttu-id="6d9ea-129">Liste der IpGroup-Quellgruppen.</span><span class="sxs-lookup"><span data-stu-id="6d9ea-129">List of source IpGroups.</span></span>

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

### <span data-ttu-id="6d9ea-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d9ea-130">-Confirm</span></span>
<span data-ttu-id="6d9ea-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6d9ea-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d9ea-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6d9ea-132">-WhatIf</span></span>
<span data-ttu-id="6d9ea-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6d9ea-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d9ea-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6d9ea-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d9ea-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d9ea-135">CommonParameters</span></span>
<span data-ttu-id="6d9ea-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d9ea-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d9ea-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d9ea-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d9ea-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6d9ea-138">INPUTS</span></span>

### <span data-ttu-id="6d9ea-139">Keine</span><span class="sxs-lookup"><span data-stu-id="6d9ea-139">None</span></span>

## <span data-ttu-id="6d9ea-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6d9ea-140">OUTPUTS</span></span>

### <span data-ttu-id="6d9ea-141">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting</span><span class="sxs-lookup"><span data-stu-id="6d9ea-141">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting</span></span>

## <span data-ttu-id="6d9ea-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6d9ea-142">NOTES</span></span>

## <span data-ttu-id="6d9ea-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6d9ea-143">RELATED LINKS</span></span>
