---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyintrusiondetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetection.md
ms.openlocfilehash: bc3c71c8900be049dce7b00b698068e96ccc8519
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151716"
---
# <span data-ttu-id="d40ba-101">New-AzFirewallPolicyIntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="d40ba-101">New-AzFirewallPolicyIntrusionDetection</span></span>

## <span data-ttu-id="d40ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d40ba-102">SYNOPSIS</span></span>
<span data-ttu-id="d40ba-103">Erstellt eine neue Angriffserkennung für die Firewallrichtlinie von Azure, die der Firewallrichtlinie zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d40ba-103">Creates a new Azure Firewall Policy Intrusion Detection to associate with Firewall Policy</span></span>

## <span data-ttu-id="d40ba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d40ba-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetection -Mode <String>
 [-SignatureOverride <PSAzureFirewallPolicyIntrusionDetectionSignatureOverride[]>]
 [-BypassTraffic <PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d40ba-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d40ba-105">DESCRIPTION</span></span>
<span data-ttu-id="d40ba-106">Das **Cmdlet "New-AzFirewallPolicyIntrusionDetection"** erstellt ein Azure Firewall Policy Intrusion Detection-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d40ba-106">The **New-AzFirewallPolicyIntrusionDetection** cmdlet creates an Azure Firewall Policy Intrusion Detection Object.</span></span>

## <span data-ttu-id="d40ba-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d40ba-107">EXAMPLES</span></span>

### <span data-ttu-id="d40ba-108">Beispiel 1: 1.</span><span class="sxs-lookup"><span data-stu-id="d40ba-108">Example 1: 1.</span></span> <span data-ttu-id="d40ba-109">Erstellen der Angriffserkennung mit Modus</span><span class="sxs-lookup"><span data-stu-id="d40ba-109">Create intrusion detection with mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert"
```

<span data-ttu-id="d40ba-110">In diesem Beispiel wird die Angriffserkennung mit dem Warnungsmodus (Erkennung) erstellt.</span><span class="sxs-lookup"><span data-stu-id="d40ba-110">This example creates intrusion detection with Alert (detection) mode</span></span>

### <span data-ttu-id="d40ba-111">Beispiel 2: 2.</span><span class="sxs-lookup"><span data-stu-id="d40ba-111">Example 2: 2.</span></span> <span data-ttu-id="d40ba-112">Erstellen der Angriffserkennung mit Signaturüberschreibungen</span><span class="sxs-lookup"><span data-stu-id="d40ba-112">Create intrusion detection with signature overrides</span></span>
```powershell
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride
```

<span data-ttu-id="d40ba-113">In diesem Beispiel wird die Angriffserkennung mit einer bestimmten Signaturüberschreibung erstellt.</span><span class="sxs-lookup"><span data-stu-id="d40ba-113">This example creates intrusion detection with specific signature override</span></span>

### <span data-ttu-id="d40ba-114">Beispiel 3: 3.</span><span class="sxs-lookup"><span data-stu-id="d40ba-114">Example 3: 3.</span></span> <span data-ttu-id="d40ba-115">Erstellen einer Firewallrichtlinie mit konfigurierter Angriffserkennung mit Einstellung für die Umgehung des Datenverkehrs</span><span class="sxs-lookup"><span data-stu-id="d40ba-115">Create firewall policy with intrusion detection configured with bypass traffic setting</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress "10.0.0.0"
PS C:\> $intrusionDetection = New-AzFirewallPolicyIntrusionDetection -Mode "Deny" -BypassTraffic $bypass
PS C:\> New-AzFirewallPolicy -Name fp1 -Location "westus2" -ResourceGroup TestRg -SkuTier "Premium" -IntrusionDetection $intrusionDetection
```

<span data-ttu-id="d40ba-116">In diesem Beispiel wird die Angriffserkennung mit Einstellung für die Umgehung des Datenverkehrs erstellt.</span><span class="sxs-lookup"><span data-stu-id="d40ba-116">This example creates intrusion detection with bypass traffic setting</span></span>

## <span data-ttu-id="d40ba-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d40ba-117">PARAMETERS</span></span>

### <span data-ttu-id="d40ba-118">-BypassTraffic</span><span class="sxs-lookup"><span data-stu-id="d40ba-118">-BypassTraffic</span></span>
<span data-ttu-id="d40ba-119">Liste der Regeln für den zu umgehende Datenverkehr.</span><span class="sxs-lookup"><span data-stu-id="d40ba-119">List of rules for traffic to bypass.</span></span>

```yaml
Type: PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d40ba-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d40ba-120">-DefaultProfile</span></span>
<span data-ttu-id="d40ba-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d40ba-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d40ba-122">-Mode</span><span class="sxs-lookup"><span data-stu-id="d40ba-122">-Mode</span></span>
<span data-ttu-id="d40ba-123">Allgemeiner Zustand der Angriffserkennung.</span><span class="sxs-lookup"><span data-stu-id="d40ba-123">Intrusion Detection general state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Off, Alert, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d40ba-124">-SignatureOverride</span><span class="sxs-lookup"><span data-stu-id="d40ba-124">-SignatureOverride</span></span>
<span data-ttu-id="d40ba-125">Liste bestimmter Signaturzustände.</span><span class="sxs-lookup"><span data-stu-id="d40ba-125">List of specific signatures states.</span></span>

```yaml
Type: PSAzureFirewallPolicyIntrusionDetectionSignatureOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d40ba-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d40ba-126">-Confirm</span></span>
<span data-ttu-id="d40ba-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d40ba-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d40ba-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d40ba-128">-WhatIf</span></span>
<span data-ttu-id="d40ba-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d40ba-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d40ba-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d40ba-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d40ba-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d40ba-131">CommonParameters</span></span>
<span data-ttu-id="d40ba-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d40ba-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d40ba-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d40ba-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d40ba-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d40ba-134">INPUTS</span></span>

### <span data-ttu-id="d40ba-135">Keine</span><span class="sxs-lookup"><span data-stu-id="d40ba-135">None</span></span>

## <span data-ttu-id="d40ba-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d40ba-136">OUTPUTS</span></span>

### <span data-ttu-id="d40ba-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="d40ba-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetection</span></span>

## <span data-ttu-id="d40ba-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d40ba-138">NOTES</span></span>

## <span data-ttu-id="d40ba-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d40ba-139">RELATED LINKS</span></span>
