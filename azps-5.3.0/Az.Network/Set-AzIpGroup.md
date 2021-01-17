---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
ms.openlocfilehash: 2d78e7136fe42187cbabc2345e2ad2314af1d9c5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473401"
---
# <span data-ttu-id="75d0c-101">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="75d0c-101">Set-AzIpGroup</span></span>

## <span data-ttu-id="75d0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75d0c-102">SYNOPSIS</span></span>
<span data-ttu-id="75d0c-103">Speichert eine geänderte Firewall.</span><span class="sxs-lookup"><span data-stu-id="75d0c-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="75d0c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75d0c-104">SYNTAX</span></span>

```
Set-AzIpGroup -IpGroup <PSIpGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="75d0c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="75d0c-105">DESCRIPTION</span></span>
<span data-ttu-id="75d0c-106">Das **Cmdlet "Set-AzIpGroup"** aktualisiert eine Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="75d0c-106">The **Set-AzIpGroup** cmdlet updates an Azure IpGroup</span></span>

## <span data-ttu-id="75d0c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="75d0c-107">EXAMPLES</span></span>

### <span data-ttu-id="75d0c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="75d0c-108">Example 1</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
$ipGroup.IpAddresses.Add("11.11.0.0/24")
Set-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="75d0c-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75d0c-109">PARAMETERS</span></span>

### <span data-ttu-id="75d0c-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75d0c-110">-AsJob</span></span>
<span data-ttu-id="75d0c-111">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="75d0c-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75d0c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75d0c-112">-DefaultProfile</span></span>
<span data-ttu-id="75d0c-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="75d0c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75d0c-114">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="75d0c-114">-IpGroup</span></span>
<span data-ttu-id="75d0c-115">Die IpGroup</span><span class="sxs-lookup"><span data-stu-id="75d0c-115">The IpGroup</span></span>

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

### <span data-ttu-id="75d0c-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75d0c-116">-Confirm</span></span>
<span data-ttu-id="75d0c-117">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="75d0c-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75d0c-118">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="75d0c-118">-WhatIf</span></span>
<span data-ttu-id="75d0c-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="75d0c-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75d0c-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="75d0c-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75d0c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75d0c-121">CommonParameters</span></span>
<span data-ttu-id="75d0c-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75d0c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75d0c-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75d0c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75d0c-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="75d0c-124">INPUTS</span></span>

### <span data-ttu-id="75d0c-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="75d0c-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="75d0c-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="75d0c-126">OUTPUTS</span></span>

### <span data-ttu-id="75d0c-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="75d0c-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="75d0c-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="75d0c-128">NOTES</span></span>

## <span data-ttu-id="75d0c-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="75d0c-129">RELATED LINKS</span></span>
