---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
ms.openlocfilehash: 38995222182d120cd2067429d0f78798a9ebaaf8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158801"
---
# <span data-ttu-id="deaad-101">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="deaad-101">Set-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="deaad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="deaad-102">SYNOPSIS</span></span>
<span data-ttu-id="deaad-103">Aktualisiert das Anzapfen eines virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="deaad-103">Updates a virtual network tap.</span></span>

## <span data-ttu-id="deaad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="deaad-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="deaad-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="deaad-105">DESCRIPTION</span></span>
<span data-ttu-id="deaad-106">Das **Cmdlet "Set-AzVirtualNetworkTap"** aktualisiert das Anzapfen eines virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="deaad-106">The **Set-AzVirtualNetworkTap** cmdlet updates a virtual network tap.</span></span>

## <span data-ttu-id="deaad-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="deaad-107">EXAMPLES</span></span>

### <span data-ttu-id="deaad-108">Beispiel 1: Konfigurieren der Anzapfung eines virtuellen Netzwerks</span><span class="sxs-lookup"><span data-stu-id="deaad-108">Example 1: Configure a Virtual network tap</span></span>
```
PS C:\>$vTap = Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzVirtualNetworkTap -VirtualNetworkTap $vTap
```

<span data-ttu-id="deaad-109">Der Befehl aktualisiert die Ziel-IpConfiguration und aktualisiert das Anzapfen des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="deaad-109">The command updates the Destination IpConfiguration and updates the Virtual network tap.</span></span>
<span data-ttu-id="deaad-110">Wenn Tippkonfigurationen auf sie verweisen, wird nicht der sämtliche Quelldatenverkehr nach dem Update auf die neue Ziel-IP-Konfiguration gespiegelt.</span><span class="sxs-lookup"><span data-stu-id="deaad-110">If there are any tap configurations referencing it, then all the source traffic will not start be mirrored to new destination ip configuration post update.</span></span>

## <span data-ttu-id="deaad-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="deaad-111">PARAMETERS</span></span>

### <span data-ttu-id="deaad-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="deaad-112">-AsJob</span></span>
<span data-ttu-id="deaad-113">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="deaad-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="deaad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deaad-114">-DefaultProfile</span></span>
<span data-ttu-id="deaad-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="deaad-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="deaad-116">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="deaad-116">-VirtualNetworkTap</span></span>
<span data-ttu-id="deaad-117">Anzapfen des virtuellen Netzwerks</span><span class="sxs-lookup"><span data-stu-id="deaad-117">The virtual network tap</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="deaad-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="deaad-118">-Confirm</span></span>
<span data-ttu-id="deaad-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="deaad-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="deaad-120">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="deaad-120">-WhatIf</span></span>
<span data-ttu-id="deaad-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="deaad-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="deaad-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="deaad-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="deaad-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deaad-123">CommonParameters</span></span>
<span data-ttu-id="deaad-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="deaad-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deaad-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="deaad-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deaad-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="deaad-126">INPUTS</span></span>

### <span data-ttu-id="deaad-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="deaad-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="deaad-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="deaad-128">OUTPUTS</span></span>

### <span data-ttu-id="deaad-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="deaad-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="deaad-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="deaad-130">NOTES</span></span>

## <span data-ttu-id="deaad-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="deaad-131">RELATED LINKS</span></span>

[<span data-ttu-id="deaad-132">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="deaad-132">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="deaad-133">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="deaad-133">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="deaad-134">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="deaad-134">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)
