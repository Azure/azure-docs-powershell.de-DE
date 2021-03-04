---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicyintrusiondetectionsignatureoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionSignatureOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionSignatureOverride.md
ms.openlocfilehash: c6aa2bb9bf3866e35ad59e59bdf5ded333fd2816
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948555"
---
# <span data-ttu-id="77c01-101">New-AzFirewallPolicyIntrusionDetectionSignatureOverride</span><span class="sxs-lookup"><span data-stu-id="77c01-101">New-AzFirewallPolicyIntrusionDetectionSignatureOverride</span></span>

## <span data-ttu-id="77c01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77c01-102">SYNOPSIS</span></span>
<span data-ttu-id="77c01-103">Erstellt eine neue Signaturüberschreibung der Signaturüberschreibung für die Erkennung von Eindringversuchen in azureer Firewallrichtlinie</span><span class="sxs-lookup"><span data-stu-id="77c01-103">Creates a new Azure Firewall Policy Intrusion Detection Signature Override</span></span>

## <span data-ttu-id="77c01-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="77c01-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id <UInt64> -Mode <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77c01-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="77c01-105">DESCRIPTION</span></span>
<span data-ttu-id="77c01-106">Das **Cmdlet New-AzFirewallPolicyIntrusionDetectionSignatureOverride** erstellt ein Außerkraftsetzungsobjekt der Azure-Firewall-Richtliniensignatur.</span><span class="sxs-lookup"><span data-stu-id="77c01-106">The **New-AzFirewallPolicyIntrusionDetectionSignatureOverride** cmdlet creates an Azure Firewall Policy Signature Override Object.</span></span>

## <span data-ttu-id="77c01-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="77c01-107">EXAMPLES</span></span>

### <span data-ttu-id="77c01-108">Beispiel 1: 1.</span><span class="sxs-lookup"><span data-stu-id="77c01-108">Example 1: 1.</span></span> <span data-ttu-id="77c01-109">Erstellen der Erkennung von Eindringversuchen mit Signaturüberschreibungen</span><span class="sxs-lookup"><span data-stu-id="77c01-109">Create intrusion detection with signature overrides</span></span>
```powershell
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride
```
<span data-ttu-id="77c01-110">In diesem Beispiel wird die Erkennung von Eindringversuchen mit einer bestimmten Signaturüberschreibung in den Deny-Modus erstellt.</span><span class="sxs-lookup"><span data-stu-id="77c01-110">This example creates intrusion detection with specific signature override to Deny mode</span></span>

## <span data-ttu-id="77c01-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="77c01-111">PARAMETERS</span></span>

### <span data-ttu-id="77c01-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77c01-112">-DefaultProfile</span></span>
<span data-ttu-id="77c01-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="77c01-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77c01-114">-ID</span><span class="sxs-lookup"><span data-stu-id="77c01-114">-Id</span></span>
<span data-ttu-id="77c01-115">Signatur-ID.</span><span class="sxs-lookup"><span data-stu-id="77c01-115">Signature id.</span></span>

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77c01-116">-Modus</span><span class="sxs-lookup"><span data-stu-id="77c01-116">-Mode</span></span>
<span data-ttu-id="77c01-117">Signaturzustand.</span><span class="sxs-lookup"><span data-stu-id="77c01-117">Signature state.</span></span>

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

### <span data-ttu-id="77c01-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="77c01-118">-Confirm</span></span>
<span data-ttu-id="77c01-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="77c01-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77c01-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77c01-120">-WhatIf</span></span>
<span data-ttu-id="77c01-121">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="77c01-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77c01-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="77c01-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77c01-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77c01-123">CommonParameters</span></span>
<span data-ttu-id="77c01-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77c01-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77c01-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77c01-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77c01-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="77c01-126">INPUTS</span></span>

### <span data-ttu-id="77c01-127">Keine</span><span class="sxs-lookup"><span data-stu-id="77c01-127">None</span></span>

## <span data-ttu-id="77c01-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="77c01-128">OUTPUTS</span></span>

### <span data-ttu-id="77c01-129">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionSignatureOverride</span><span class="sxs-lookup"><span data-stu-id="77c01-129">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionSignatureOverride</span></span>

## <span data-ttu-id="77c01-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="77c01-130">NOTES</span></span>

## <span data-ttu-id="77c01-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="77c01-131">RELATED LINKS</span></span>
