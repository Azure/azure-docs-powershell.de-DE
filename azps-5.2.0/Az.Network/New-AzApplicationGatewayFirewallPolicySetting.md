---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicysetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
ms.openlocfilehash: b1665975fd85268bdb8788eb96ba0c8694b6f4c6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297931"
---
# <span data-ttu-id="be5df-101">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="be5df-101">New-AzApplicationGatewayFirewallPolicySetting</span></span>

## <span data-ttu-id="be5df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be5df-102">SYNOPSIS</span></span>
<span data-ttu-id="be5df-103">Erstellt eine Richtlinieneinstellung für die Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="be5df-103">Creates a policy setting for the firewall policy</span></span>

## <span data-ttu-id="be5df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="be5df-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicySetting [-Mode <String>] [-State <String>] [-DisableRequestBodyCheck]
 [-MaxRequestBodySizeInKb <Int32>] [-MaxFileUploadInMb <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="be5df-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="be5df-105">DESCRIPTION</span></span>
<span data-ttu-id="be5df-106">Das **New-AzApplicationGatewayFirewallPolicySetting** erstellt richtlinieneinstellungen für eine Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="be5df-106">The **New-AzApplicationGatewayFirewallPolicySetting** creates a policy settings for a firewall policy.</span></span>

## <span data-ttu-id="be5df-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="be5df-107">EXAMPLES</span></span>

### <span data-ttu-id="be5df-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="be5df-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicySetting -State $enabledState -Mode $enabledMode -DisableRequestBodyCheck -MaxFileUploadInMb $fileUploadLimitInMb -MaxRequestBodySizeInKb $maxRequestBodySizeInKb
```

<span data-ttu-id="be5df-109">Der Befehl erstellt eine Richtlinieneinstellung mit dem Status $enabledState, modus als $enabledMode, RequestBodyCheck as false, FileUploadLimitInMb as $fileUploadLimitInMb und MaxRequestBodySizeInKb as $$maxRequestBodySizeInKb.</span><span class="sxs-lookup"><span data-stu-id="be5df-109">The command creates a policy setting with state as $enabledState, mode as $enabledMode, RequestBodyCheck as false, FileUploadLimitInMb as $fileUploadLimitInMb and MaxRequestBodySizeInKb as $$maxRequestBodySizeInKb.</span></span>
<span data-ttu-id="be5df-110">Die neuen "policySettings" werden im $condition.</span><span class="sxs-lookup"><span data-stu-id="be5df-110">The new policySettings is stored to $condition.</span></span>

## <span data-ttu-id="be5df-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be5df-111">PARAMETERS</span></span>

### <span data-ttu-id="be5df-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be5df-112">-DefaultProfile</span></span>
<span data-ttu-id="be5df-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="be5df-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be5df-114">-DisableRequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="be5df-114">-DisableRequestBodyCheck</span></span>
<span data-ttu-id="be5df-115">Diables the requestBodyCheck in policy settings of the firewall policy.</span><span class="sxs-lookup"><span data-stu-id="be5df-115">Diables the requestBodyCheck in policy settings of the firewall policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be5df-116">-MaxFileUploadInMb</span><span class="sxs-lookup"><span data-stu-id="be5df-116">-MaxFileUploadInMb</span></span>
<span data-ttu-id="be5df-117">Maximale Dateiuploadgröße in MB.</span><span class="sxs-lookup"><span data-stu-id="be5df-117">Maximum fileUpload size in MB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be5df-118">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="be5df-118">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="be5df-119">MaxRequestBodySizeInKb in den Richtlinieneinstellungen der Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="be5df-119">MaxRequestBodySizeInKb in policy settings of the firewall policy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 128
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be5df-120">-Mode</span><span class="sxs-lookup"><span data-stu-id="be5df-120">-Mode</span></span>
<span data-ttu-id="be5df-121">Firewallmodus in den Richtlinieneinstellungen der Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="be5df-121">Firewall Mode in policy settings of the firewall policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Prevention, Detection

Required: False
Position: Named
Default value: Detection
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be5df-122">-State</span><span class="sxs-lookup"><span data-stu-id="be5df-122">-State</span></span>
<span data-ttu-id="be5df-123">Zustandsvariable in den Richtlinieneinstellungen der Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="be5df-123">State variable in policy settings of the firewall policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be5df-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be5df-124">CommonParameters</span></span>
<span data-ttu-id="be5df-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be5df-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be5df-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be5df-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be5df-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="be5df-127">INPUTS</span></span>

### <span data-ttu-id="be5df-128">Keine</span><span class="sxs-lookup"><span data-stu-id="be5df-128">None</span></span>

## <span data-ttu-id="be5df-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="be5df-129">OUTPUTS</span></span>

### <span data-ttu-id="be5df-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="be5df-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

## <span data-ttu-id="be5df-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="be5df-131">NOTES</span></span>

## <span data-ttu-id="be5df-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="be5df-132">RELATED LINKS</span></span>
