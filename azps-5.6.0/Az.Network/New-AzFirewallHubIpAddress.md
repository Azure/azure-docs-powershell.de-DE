---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallhubipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
ms.openlocfilehash: 333e245b77869903b74973a4f851d020d70c0943
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935632"
---
# <span data-ttu-id="2b4c0-101">New-AzFirewallHubIpAddress</span><span class="sxs-lookup"><span data-stu-id="2b4c0-101">New-AzFirewallHubIpAddress</span></span>

## <span data-ttu-id="2b4c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b4c0-102">SYNOPSIS</span></span>
<span data-ttu-id="2b4c0-103">Ip-Adressen, die mit der Firewall auf dem virtuellen Hub verbunden sind</span><span class="sxs-lookup"><span data-stu-id="2b4c0-103">Ip addresses assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="2b4c0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2b4c0-104">SYNTAX</span></span>

```
New-AzFirewallHubIpAddress [-PrivateIPAddress <String>] [-PublicIPs <PSAzureFirewallHubPublicIpAddresses>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b4c0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b4c0-105">DESCRIPTION</span></span>
<span data-ttu-id="2b4c0-106">Ip-Adressen, die der Firewall auf dem virtuellen Hub zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="2b4c0-106">Ip addresses assoicated to the firewall on virtual hub.</span></span> <span data-ttu-id="2b4c0-107">Dabei kann es sich um öffentliche und private Adressen handelt</span><span class="sxs-lookup"><span data-stu-id="2b4c0-107">These can be public and private addresses</span></span>

## <span data-ttu-id="2b4c0-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2b4c0-108">EXAMPLES</span></span>

### <span data-ttu-id="2b4c0-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2b4c0-109">Example 1</span></span>
```powershell
PS C:\> $fwpips = New-AzFirewallHubPublicIpAddress -Count 2
PS C:\> New-AzFirewallHubIpAddress -PublicIPs $fwpips
```

<span data-ttu-id="2b4c0-110">In diesem Beispiel wird ein Hub Ip-Adressobjekt mit einer Anzahl von zwei öffentlichen IPs erstellt.</span><span class="sxs-lookup"><span data-stu-id="2b4c0-110">This example creates a Hub Ip address object with a count of 2 public IPs.</span></span> <span data-ttu-id="2b4c0-111">Das HubIPAddress-Objekt wird mit der Firewall auf dem virtuellen Hub verbunden.</span><span class="sxs-lookup"><span data-stu-id="2b4c0-111">The HubIPAddress object is ssociated to the firewall on the virtual hub.</span></span>

## <span data-ttu-id="2b4c0-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2b4c0-112">PARAMETERS</span></span>

### <span data-ttu-id="2b4c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b4c0-113">-DefaultProfile</span></span>
<span data-ttu-id="2b4c0-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2b4c0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b4c0-115">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="2b4c0-115">-PrivateIPAddress</span></span>
<span data-ttu-id="2b4c0-116">Die private IP-Adresse der Firewall, die an einen Hub angefügt ist</span><span class="sxs-lookup"><span data-stu-id="2b4c0-116">The private Ip Address of the Firewall attached to a Hub</span></span>

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

### <span data-ttu-id="2b4c0-117">-PublicIPs</span><span class="sxs-lookup"><span data-stu-id="2b4c0-117">-PublicIPs</span></span>
<span data-ttu-id="2b4c0-118">Die AN einen Hub angefügten IP-Adressen der Firewall</span><span class="sxs-lookup"><span data-stu-id="2b4c0-118">The IP Addresses of the Firewall attached to a hub</span></span>

```yaml
Type: PSAzureFirewallHubPublicIpAddresses
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b4c0-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2b4c0-119">-Confirm</span></span>
<span data-ttu-id="2b4c0-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2b4c0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b4c0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b4c0-121">-WhatIf</span></span>
<span data-ttu-id="2b4c0-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2b4c0-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2b4c0-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2b4c0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b4c0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b4c0-124">CommonParameters</span></span>
<span data-ttu-id="2b4c0-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b4c0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b4c0-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b4c0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b4c0-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2b4c0-127">INPUTS</span></span>

### <span data-ttu-id="2b4c0-128">Keine</span><span class="sxs-lookup"><span data-stu-id="2b4c0-128">None</span></span>

## <span data-ttu-id="2b4c0-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2b4c0-129">OUTPUTS</span></span>

### <span data-ttu-id="2b4c0-130">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses</span><span class="sxs-lookup"><span data-stu-id="2b4c0-130">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses</span></span>

## <span data-ttu-id="2b4c0-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2b4c0-131">NOTES</span></span>

## <span data-ttu-id="2b4c0-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2b4c0-132">RELATED LINKS</span></span>
