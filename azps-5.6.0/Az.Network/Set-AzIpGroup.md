---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
ms.openlocfilehash: 8f8e40f5b2209b75c52376c08b69dff8946add77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930880"
---
# <span data-ttu-id="c1958-101">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="c1958-101">Set-AzIpGroup</span></span>

## <span data-ttu-id="c1958-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1958-102">SYNOPSIS</span></span>
<span data-ttu-id="c1958-103">Speichert eine geänderte Firewall.</span><span class="sxs-lookup"><span data-stu-id="c1958-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="c1958-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1958-104">SYNTAX</span></span>

```
Set-AzIpGroup -IpGroup <PSIpGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1958-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c1958-105">DESCRIPTION</span></span>
<span data-ttu-id="c1958-106">Das **Cmdlet Set-AzIpGroup** aktualisiert eine Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="c1958-106">The **Set-AzIpGroup** cmdlet updates an Azure IpGroup</span></span>

## <span data-ttu-id="c1958-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c1958-107">EXAMPLES</span></span>

### <span data-ttu-id="c1958-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c1958-108">Example 1</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
$ipGroup.IpAddresses.Add("11.11.0.0/24")
Set-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="c1958-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c1958-109">PARAMETERS</span></span>

### <span data-ttu-id="c1958-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1958-110">-AsJob</span></span>
<span data-ttu-id="c1958-111">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c1958-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1958-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1958-112">-DefaultProfile</span></span>
<span data-ttu-id="c1958-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c1958-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1958-114">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="c1958-114">-IpGroup</span></span>
<span data-ttu-id="c1958-115">Die IpGroup</span><span class="sxs-lookup"><span data-stu-id="c1958-115">The IpGroup</span></span>

```yaml
Type: PSIpGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1958-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c1958-116">-Confirm</span></span>
<span data-ttu-id="c1958-117">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c1958-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1958-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1958-118">-WhatIf</span></span>
<span data-ttu-id="c1958-119">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c1958-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1958-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c1958-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1958-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1958-121">CommonParameters</span></span>
<span data-ttu-id="c1958-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1958-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1958-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1958-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1958-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c1958-124">INPUTS</span></span>

### <span data-ttu-id="c1958-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="c1958-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="c1958-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c1958-126">OUTPUTS</span></span>

### <span data-ttu-id="c1958-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="c1958-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="c1958-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c1958-128">NOTES</span></span>

## <span data-ttu-id="c1958-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c1958-129">RELATED LINKS</span></span>
