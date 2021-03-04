---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
ms.openlocfilehash: 2f46b13570ef1f538658dae6d02000848822c150
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919560"
---
# <span data-ttu-id="c247a-101">New-AzPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="c247a-101">New-AzPublicIpTag</span></span>

## <span data-ttu-id="c247a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c247a-102">SYNOPSIS</span></span>
<span data-ttu-id="c247a-103">Erstellt ein IP-Tag.</span><span class="sxs-lookup"><span data-stu-id="c247a-103">Creates an IP Tag.</span></span>

## <span data-ttu-id="c247a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c247a-104">SYNTAX</span></span>

```
New-AzPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c247a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c247a-105">DESCRIPTION</span></span>
<span data-ttu-id="c247a-106">Das **Cmdlet New-AzPublicIpTag** erstellt ein IP-Tag.</span><span class="sxs-lookup"><span data-stu-id="c247a-106">The **New-AzPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="c247a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c247a-107">EXAMPLES</span></span>

### <span data-ttu-id="c247a-108">Beispiel 1: Erstellen eines neuen IP-Tags</span><span class="sxs-lookup"><span data-stu-id="c247a-108">Example 1: Create a new IP Tag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="c247a-109">Mit diesem Befehl wird ein neues IP-Tag mit dem Tagtyp wie "FirstPartyUsage" und einem Tag wie "/Sql" erstellt.</span><span class="sxs-lookup"><span data-stu-id="c247a-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="c247a-110">Dies wird bei der öffentlichenIpAddress-Erstellung mit diesen speziellen Tags für die Zuweisung verwendet.</span><span class="sxs-lookup"><span data-stu-id="c247a-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="c247a-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c247a-111">PARAMETERS</span></span>

### <span data-ttu-id="c247a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c247a-112">-DefaultProfile</span></span>
<span data-ttu-id="c247a-113">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c247a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c247a-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="c247a-114">-IpTagType</span></span>
<span data-ttu-id="c247a-115">#A0 Beispiel:FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="c247a-115">IpTag type Example:FirstPartyUsage</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c247a-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="c247a-116">-Tag</span></span>
<span data-ttu-id="c247a-117">#A0 Beispiel:/Sql</span><span class="sxs-lookup"><span data-stu-id="c247a-117">IpTag value Example:/Sql</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c247a-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c247a-118">-Confirm</span></span>
<span data-ttu-id="c247a-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c247a-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c247a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c247a-120">-WhatIf</span></span>
<span data-ttu-id="c247a-121">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c247a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c247a-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c247a-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c247a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c247a-123">CommonParameters</span></span>
<span data-ttu-id="c247a-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c247a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c247a-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c247a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c247a-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c247a-126">INPUTS</span></span>

### <span data-ttu-id="c247a-127">System.String</span><span class="sxs-lookup"><span data-stu-id="c247a-127">System.String</span></span>

## <span data-ttu-id="c247a-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c247a-128">OUTPUTS</span></span>

### <span data-ttu-id="c247a-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="c247a-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>

## <span data-ttu-id="c247a-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c247a-130">NOTES</span></span>

## <span data-ttu-id="c247a-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c247a-131">RELATED LINKS</span></span>
