---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicysetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
ms.openlocfilehash: b1665975fd85268bdb8788eb96ba0c8694b6f4c6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005016"
---
# <span data-ttu-id="735f6-101">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="735f6-101">New-AzApplicationGatewayFirewallPolicySetting</span></span>

## <span data-ttu-id="735f6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="735f6-102">SYNOPSIS</span></span>
<span data-ttu-id="735f6-103">Erstellt eine Richtlinieneinstellung für die Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="735f6-103">Creates a policy setting for the firewall policy</span></span>

## <span data-ttu-id="735f6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="735f6-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicySetting [-Mode <String>] [-State <String>] [-DisableRequestBodyCheck]
 [-MaxRequestBodySizeInKb <Int32>] [-MaxFileUploadInMb <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="735f6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="735f6-105">DESCRIPTION</span></span>
<span data-ttu-id="735f6-106">Das **AzApplicationGatewayFirewallPolicySetting** erstellt eine Richtlinieneinstellung für eine Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="735f6-106">The **New-AzApplicationGatewayFirewallPolicySetting** creates a policy settings for a firewall policy.</span></span>

## <span data-ttu-id="735f6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="735f6-107">EXAMPLES</span></span>

### <span data-ttu-id="735f6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="735f6-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicySetting -State $enabledState -Mode $enabledMode -DisableRequestBodyCheck -MaxFileUploadInMb $fileUploadLimitInMb -MaxRequestBodySizeInKb $maxRequestBodySizeInKb
```

<span data-ttu-id="735f6-109">Der Befehl erstellt eine Richtlinieneinstellung mit dem Status als $enabledState, Modus als $enabledMode, RequestBodyCheck als falsch, FileUploadLimitInMb als $fileUploadLimitInMb und MaxRequestBodySizeInKb als $ $maxRequestBodySizeInKb.</span><span class="sxs-lookup"><span data-stu-id="735f6-109">The command creates a policy setting with state as $enabledState, mode as $enabledMode, RequestBodyCheck as false, FileUploadLimitInMb as $fileUploadLimitInMb and MaxRequestBodySizeInKb as $$maxRequestBodySizeInKb.</span></span>
<span data-ttu-id="735f6-110">Das neue policySettings wird in $Condition gespeichert.</span><span class="sxs-lookup"><span data-stu-id="735f6-110">The new policySettings is stored to $condition.</span></span>

## <span data-ttu-id="735f6-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="735f6-111">PARAMETERS</span></span>

### <span data-ttu-id="735f6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="735f6-112">-DefaultProfile</span></span>
<span data-ttu-id="735f6-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="735f6-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="735f6-114">-DisableRequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="735f6-114">-DisableRequestBodyCheck</span></span>
<span data-ttu-id="735f6-115">Deaktiviert die requestBodyCheck in den Richtlinieneinstellungen der Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="735f6-115">Diables the requestBodyCheck in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="735f6-116">-MaxFileUploadInMb</span><span class="sxs-lookup"><span data-stu-id="735f6-116">-MaxFileUploadInMb</span></span>
<span data-ttu-id="735f6-117">Maximale Datei Uploadgröße in MB.</span><span class="sxs-lookup"><span data-stu-id="735f6-117">Maximum fileUpload size in MB.</span></span>

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

### <span data-ttu-id="735f6-118">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="735f6-118">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="735f6-119">MaxRequestBodySizeInKb in den Richtlinieneinstellungen der Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="735f6-119">MaxRequestBodySizeInKb in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="735f6-120">-Modus</span><span class="sxs-lookup"><span data-stu-id="735f6-120">-Mode</span></span>
<span data-ttu-id="735f6-121">Firewallmodus in den Richtlinieneinstellungen der Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="735f6-121">Firewall Mode in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="735f6-122">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="735f6-122">-State</span></span>
<span data-ttu-id="735f6-123">Statusvariable in den Richtlinieneinstellungen der Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="735f6-123">State variable in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="735f6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="735f6-124">CommonParameters</span></span>
<span data-ttu-id="735f6-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="735f6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="735f6-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="735f6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="735f6-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="735f6-127">INPUTS</span></span>

### <span data-ttu-id="735f6-128">Keine</span><span class="sxs-lookup"><span data-stu-id="735f6-128">None</span></span>

## <span data-ttu-id="735f6-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="735f6-129">OUTPUTS</span></span>

### <span data-ttu-id="735f6-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="735f6-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

## <span data-ttu-id="735f6-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="735f6-131">NOTES</span></span>

## <span data-ttu-id="735f6-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="735f6-132">RELATED LINKS</span></span>
