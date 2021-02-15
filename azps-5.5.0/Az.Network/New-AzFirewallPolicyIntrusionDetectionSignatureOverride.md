---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyintrusiondetectionsignatureoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionSignatureOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionSignatureOverride.md
ms.openlocfilehash: d2389a8d4880b576e51cda41ac3c15bd091257c1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151700"
---
# <span data-ttu-id="c2a37-101">New-AzFirewallPolicyIntrusionDetectionSignatureOverride</span><span class="sxs-lookup"><span data-stu-id="c2a37-101">New-AzFirewallPolicyIntrusionDetectionSignatureOverride</span></span>

## <span data-ttu-id="c2a37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2a37-102">SYNOPSIS</span></span>
<span data-ttu-id="c2a37-103">Erstellt eine neue Außerkraftsetzung der Signaturüberschreibung der Azure-Firewall-Richtlinieneindringerkennung.</span><span class="sxs-lookup"><span data-stu-id="c2a37-103">Creates a new Azure Firewall Policy Intrusion Detection Signature Override</span></span>

## <span data-ttu-id="c2a37-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2a37-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id <UInt64> -Mode <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2a37-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c2a37-105">DESCRIPTION</span></span>
<span data-ttu-id="c2a37-106">Das **Cmdlet "New-AzFirewallPolicyIntrusionDetectionSignatureOverride"** erstellt ein Überschreibungsobjekt für die Signatur der Azure-Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="c2a37-106">The **New-AzFirewallPolicyIntrusionDetectionSignatureOverride** cmdlet creates an Azure Firewall Policy Signature Override Object.</span></span>

## <span data-ttu-id="c2a37-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c2a37-107">EXAMPLES</span></span>

### <span data-ttu-id="c2a37-108">Beispiel 1: 1.</span><span class="sxs-lookup"><span data-stu-id="c2a37-108">Example 1: 1.</span></span> <span data-ttu-id="c2a37-109">Erstellen der Angriffserkennung mit Signaturüberschreibungen</span><span class="sxs-lookup"><span data-stu-id="c2a37-109">Create intrusion detection with signature overrides</span></span>
```powershell
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride
```
<span data-ttu-id="c2a37-110">In diesem Beispiel wird die Angriffserkennung mit einer bestimmten Signaturüberschreibung in den Verweigernmodus erstellt.</span><span class="sxs-lookup"><span data-stu-id="c2a37-110">This example creates intrusion detection with specific signature override to Deny mode</span></span>

## <span data-ttu-id="c2a37-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2a37-111">PARAMETERS</span></span>

### <span data-ttu-id="c2a37-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2a37-112">-DefaultProfile</span></span>
<span data-ttu-id="c2a37-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2a37-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2a37-114">-ID</span><span class="sxs-lookup"><span data-stu-id="c2a37-114">-Id</span></span>
<span data-ttu-id="c2a37-115">Signatur-ID.</span><span class="sxs-lookup"><span data-stu-id="c2a37-115">Signature id.</span></span>

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

### <span data-ttu-id="c2a37-116">-Mode</span><span class="sxs-lookup"><span data-stu-id="c2a37-116">-Mode</span></span>
<span data-ttu-id="c2a37-117">Signaturzustand.</span><span class="sxs-lookup"><span data-stu-id="c2a37-117">Signature state.</span></span>

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

### <span data-ttu-id="c2a37-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2a37-118">-Confirm</span></span>
<span data-ttu-id="c2a37-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c2a37-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2a37-120">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c2a37-120">-WhatIf</span></span>
<span data-ttu-id="c2a37-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2a37-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2a37-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2a37-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2a37-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2a37-123">CommonParameters</span></span>
<span data-ttu-id="c2a37-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2a37-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2a37-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2a37-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2a37-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c2a37-126">INPUTS</span></span>

### <span data-ttu-id="c2a37-127">Keine</span><span class="sxs-lookup"><span data-stu-id="c2a37-127">None</span></span>

## <span data-ttu-id="c2a37-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c2a37-128">OUTPUTS</span></span>

### <span data-ttu-id="c2a37-129">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionSignatureOverride</span><span class="sxs-lookup"><span data-stu-id="c2a37-129">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionSignatureOverride</span></span>

## <span data-ttu-id="c2a37-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c2a37-130">NOTES</span></span>

## <span data-ttu-id="c2a37-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c2a37-131">RELATED LINKS</span></span>
