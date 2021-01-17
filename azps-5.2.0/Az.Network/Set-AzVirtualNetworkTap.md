---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
ms.openlocfilehash: 38995222182d120cd2067429d0f78798a9ebaaf8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365096"
---
# <span data-ttu-id="b8450-101">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="b8450-101">Set-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="b8450-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8450-102">SYNOPSIS</span></span>
<span data-ttu-id="b8450-103">Aktualisiert die Anzapfung eines virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="b8450-103">Updates a virtual network tap.</span></span>

## <span data-ttu-id="b8450-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8450-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8450-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b8450-105">DESCRIPTION</span></span>
<span data-ttu-id="b8450-106">Das **Cmdlet "Set-AzVirtualNetworkTap"** aktualisiert das Anzapfen eines virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="b8450-106">The **Set-AzVirtualNetworkTap** cmdlet updates a virtual network tap.</span></span>

## <span data-ttu-id="b8450-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b8450-107">EXAMPLES</span></span>

### <span data-ttu-id="b8450-108">Beispiel 1: Konfigurieren der Anzapfung eines virtuellen Netzwerks</span><span class="sxs-lookup"><span data-stu-id="b8450-108">Example 1: Configure a Virtual network tap</span></span>
```
PS C:\>$vTap = Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzVirtualNetworkTap -VirtualNetworkTap $vTap
```

<span data-ttu-id="b8450-109">Der Befehl aktualisiert die Ziel-IpConfiguration und aktualisiert das Anzapfen des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="b8450-109">The command updates the Destination IpConfiguration and updates the Virtual network tap.</span></span>
<span data-ttu-id="b8450-110">Wenn tippt, wird nach dem Update nicht der sämtliche Quelldatenverkehr auf die neue Ziel-IP-Konfiguration gespiegelt.</span><span class="sxs-lookup"><span data-stu-id="b8450-110">If there are any tap configurations referencing it, then all the source traffic will not start be mirrored to new destination ip configuration post update.</span></span>

## <span data-ttu-id="b8450-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8450-111">PARAMETERS</span></span>

### <span data-ttu-id="b8450-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8450-112">-AsJob</span></span>
<span data-ttu-id="b8450-113">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b8450-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8450-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8450-114">-DefaultProfile</span></span>
<span data-ttu-id="b8450-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8450-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8450-116">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="b8450-116">-VirtualNetworkTap</span></span>
<span data-ttu-id="b8450-117">Anzapfen des virtuellen Netzwerks</span><span class="sxs-lookup"><span data-stu-id="b8450-117">The virtual network tap</span></span>

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

### <span data-ttu-id="b8450-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8450-118">-Confirm</span></span>
<span data-ttu-id="b8450-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b8450-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8450-120">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b8450-120">-WhatIf</span></span>
<span data-ttu-id="b8450-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b8450-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8450-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b8450-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8450-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8450-123">CommonParameters</span></span>
<span data-ttu-id="b8450-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8450-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8450-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8450-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8450-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b8450-126">INPUTS</span></span>

### <span data-ttu-id="b8450-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="b8450-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="b8450-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b8450-128">OUTPUTS</span></span>

### <span data-ttu-id="b8450-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="b8450-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="b8450-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b8450-130">NOTES</span></span>

## <span data-ttu-id="b8450-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b8450-131">RELATED LINKS</span></span>

[<span data-ttu-id="b8450-132">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="b8450-132">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="b8450-133">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="b8450-133">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="b8450-134">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="b8450-134">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)
