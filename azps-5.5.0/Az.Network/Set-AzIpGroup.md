---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
ms.openlocfilehash: 2d78e7136fe42187cbabc2345e2ad2314af1d9c5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156732"
---
# <span data-ttu-id="268d2-101">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="268d2-101">Set-AzIpGroup</span></span>

## <span data-ttu-id="268d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="268d2-102">SYNOPSIS</span></span>
<span data-ttu-id="268d2-103">Speichert eine geänderte Firewall.</span><span class="sxs-lookup"><span data-stu-id="268d2-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="268d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="268d2-104">SYNTAX</span></span>

```
Set-AzIpGroup -IpGroup <PSIpGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="268d2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="268d2-105">DESCRIPTION</span></span>
<span data-ttu-id="268d2-106">Das **Cmdlet "Set-AzIpGroup"** aktualisiert eine Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="268d2-106">The **Set-AzIpGroup** cmdlet updates an Azure IpGroup</span></span>

## <span data-ttu-id="268d2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="268d2-107">EXAMPLES</span></span>

### <span data-ttu-id="268d2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="268d2-108">Example 1</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
$ipGroup.IpAddresses.Add("11.11.0.0/24")
Set-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="268d2-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="268d2-109">PARAMETERS</span></span>

### <span data-ttu-id="268d2-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="268d2-110">-AsJob</span></span>
<span data-ttu-id="268d2-111">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="268d2-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="268d2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="268d2-112">-DefaultProfile</span></span>
<span data-ttu-id="268d2-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="268d2-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="268d2-114">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="268d2-114">-IpGroup</span></span>
<span data-ttu-id="268d2-115">Die IpGroup</span><span class="sxs-lookup"><span data-stu-id="268d2-115">The IpGroup</span></span>

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

### <span data-ttu-id="268d2-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="268d2-116">-Confirm</span></span>
<span data-ttu-id="268d2-117">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="268d2-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="268d2-118">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="268d2-118">-WhatIf</span></span>
<span data-ttu-id="268d2-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="268d2-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="268d2-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="268d2-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="268d2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="268d2-121">CommonParameters</span></span>
<span data-ttu-id="268d2-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="268d2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="268d2-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="268d2-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="268d2-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="268d2-124">INPUTS</span></span>

### <span data-ttu-id="268d2-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="268d2-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="268d2-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="268d2-126">OUTPUTS</span></span>

### <span data-ttu-id="268d2-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="268d2-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="268d2-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="268d2-128">NOTES</span></span>

## <span data-ttu-id="268d2-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="268d2-129">RELATED LINKS</span></span>
