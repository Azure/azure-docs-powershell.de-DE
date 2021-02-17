---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
ms.openlocfilehash: c4bc5e9fcc7d0ca405a8031af29d16283f963ad2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169847"
---
# <span data-ttu-id="9249f-101">New-AzFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9249f-101">New-AzFirewallPublicIpAddress</span></span>

## <span data-ttu-id="9249f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9249f-102">SYNOPSIS</span></span>
<span data-ttu-id="9249f-103">Dies ist der Platzhalter für die Ip-Adresse, die für die Azure Firewall mit mehreren Pips verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9249f-103">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="9249f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9249f-104">SYNTAX</span></span>

```
New-AzFirewallPublicIpAddress [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9249f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9249f-105">DESCRIPTION</span></span>
<span data-ttu-id="9249f-106">Dies ist der Platzhalter für die Ip-Adresse, die für die Azure Firewall mit mehreren Pips verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9249f-106">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="9249f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9249f-107">EXAMPLES</span></span>

### <span data-ttu-id="9249f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9249f-108">Example 1</span></span>
```powershell
PS C:\> $publicIp = New-AzFirewallPublicIpAddress -Address 20.2.3.4
```

<span data-ttu-id="9249f-109">$publicIp als Platzhalter für die ip-Adresse 20.2.3.4</span><span class="sxs-lookup"><span data-stu-id="9249f-109">$publicIp will be the placeholder for the ip address 20.2.3.4</span></span>

## <span data-ttu-id="9249f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9249f-110">PARAMETERS</span></span>

### <span data-ttu-id="9249f-111">-Address</span><span class="sxs-lookup"><span data-stu-id="9249f-111">-Address</span></span>
<span data-ttu-id="9249f-112">Die an einen Hub angefügten IP-Adressen der Firewall</span><span class="sxs-lookup"><span data-stu-id="9249f-112">The IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="9249f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9249f-113">-DefaultProfile</span></span>
<span data-ttu-id="9249f-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9249f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9249f-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9249f-115">-Confirm</span></span>
<span data-ttu-id="9249f-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9249f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9249f-117">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9249f-117">-WhatIf</span></span>
<span data-ttu-id="9249f-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9249f-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9249f-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9249f-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9249f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9249f-120">CommonParameters</span></span>
<span data-ttu-id="9249f-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9249f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9249f-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9249f-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9249f-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9249f-123">INPUTS</span></span>

### <span data-ttu-id="9249f-124">Keine</span><span class="sxs-lookup"><span data-stu-id="9249f-124">None</span></span>

## <span data-ttu-id="9249f-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9249f-125">OUTPUTS</span></span>

### <span data-ttu-id="9249f-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9249f-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPublicIpAddress</span></span>

## <span data-ttu-id="9249f-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9249f-127">NOTES</span></span>

## <span data-ttu-id="9249f-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9249f-128">RELATED LINKS</span></span>
