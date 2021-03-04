---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
ms.openlocfilehash: 2e7c1b0468ed3faf37c8f11bc0cb1eca707195bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921888"
---
# <span data-ttu-id="41335-101">New-AzFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="41335-101">New-AzFirewallPublicIpAddress</span></span>

## <span data-ttu-id="41335-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41335-102">SYNOPSIS</span></span>
<span data-ttu-id="41335-103">Dies ist der Platzhalter für die Ip-Adresse, die für multi pip in der Azure-Firewall verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="41335-103">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="41335-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41335-104">SYNTAX</span></span>

```
New-AzFirewallPublicIpAddress [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41335-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="41335-105">DESCRIPTION</span></span>
<span data-ttu-id="41335-106">Dies ist der Platzhalter für die Ip-Adresse, die für multi pip in der Azure-Firewall verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="41335-106">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="41335-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="41335-107">EXAMPLES</span></span>

### <span data-ttu-id="41335-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="41335-108">Example 1</span></span>
```powershell
PS C:\> $publicIp = New-AzFirewallPublicIpAddress -Address 20.2.3.4
```

<span data-ttu-id="41335-109">$publicIp wird der Platzhalter für die IP-Adresse 20.2.3.4</span><span class="sxs-lookup"><span data-stu-id="41335-109">$publicIp will be the placeholder for the ip address 20.2.3.4</span></span>

## <span data-ttu-id="41335-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="41335-110">PARAMETERS</span></span>

### <span data-ttu-id="41335-111">-Adresse</span><span class="sxs-lookup"><span data-stu-id="41335-111">-Address</span></span>
<span data-ttu-id="41335-112">Die AN einen Hub angefügten IP-Adressen der Firewall</span><span class="sxs-lookup"><span data-stu-id="41335-112">The IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="41335-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41335-113">-DefaultProfile</span></span>
<span data-ttu-id="41335-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="41335-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41335-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="41335-115">-Confirm</span></span>
<span data-ttu-id="41335-116">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="41335-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41335-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41335-117">-WhatIf</span></span>
<span data-ttu-id="41335-118">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="41335-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41335-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="41335-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41335-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41335-120">CommonParameters</span></span>
<span data-ttu-id="41335-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41335-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41335-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41335-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41335-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="41335-123">INPUTS</span></span>

### <span data-ttu-id="41335-124">Keine</span><span class="sxs-lookup"><span data-stu-id="41335-124">None</span></span>

## <span data-ttu-id="41335-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="41335-125">OUTPUTS</span></span>

### <span data-ttu-id="41335-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="41335-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPublicIpAddress</span></span>

## <span data-ttu-id="41335-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="41335-127">NOTES</span></span>

## <span data-ttu-id="41335-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="41335-128">RELATED LINKS</span></span>
