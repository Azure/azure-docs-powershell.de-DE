---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
ms.openlocfilehash: 38995222182d120cd2067429d0f78798a9ebaaf8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303574"
---
# <span data-ttu-id="dd895-101">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="dd895-101">Set-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="dd895-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dd895-102">SYNOPSIS</span></span>
<span data-ttu-id="dd895-103">Aktualisiert ein virtuelles Netzwerk, tippen Sie auf.</span><span class="sxs-lookup"><span data-stu-id="dd895-103">Updates a virtual network tap.</span></span>

## <span data-ttu-id="dd895-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd895-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd895-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd895-105">DESCRIPTION</span></span>
<span data-ttu-id="dd895-106">Das Cmdlet " **Satz-AzVirtualNetworkTap** " aktualisiert einen virtuellen Netzwerk-Tap.</span><span class="sxs-lookup"><span data-stu-id="dd895-106">The **Set-AzVirtualNetworkTap** cmdlet updates a virtual network tap.</span></span>

## <span data-ttu-id="dd895-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd895-107">EXAMPLES</span></span>

### <span data-ttu-id="dd895-108">Beispiel 1: Konfigurieren eines virtuellen Netzwerk Hahns</span><span class="sxs-lookup"><span data-stu-id="dd895-108">Example 1: Configure a Virtual network tap</span></span>
```
PS C:\>$vTap = Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzVirtualNetworkTap -VirtualNetworkTap $vTap
```

<span data-ttu-id="dd895-109">Der Befehl aktualisiert das Ziel IPKonfigurationsdateiAddress und aktualisiert das virtuelle Netzwerk Tap.</span><span class="sxs-lookup"><span data-stu-id="dd895-109">The command updates the Destination IpConfiguration and updates the Virtual network tap.</span></span>
<span data-ttu-id="dd895-110">Wenn es auf eine Tap-Konfiguration ankommt, die darauf verweist, wird der gesamte Quell Verkehr nicht mit dem neuen Ziel-IP-Konfigurations Post-Update gespiegelt.</span><span class="sxs-lookup"><span data-stu-id="dd895-110">If there are any tap configurations referencing it, then all the source traffic will not start be mirrored to new destination ip configuration post update.</span></span>

## <span data-ttu-id="dd895-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd895-111">PARAMETERS</span></span>

### <span data-ttu-id="dd895-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd895-112">-AsJob</span></span>
<span data-ttu-id="dd895-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="dd895-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd895-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd895-114">-DefaultProfile</span></span>
<span data-ttu-id="dd895-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dd895-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd895-116">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="dd895-116">-VirtualNetworkTap</span></span>
<span data-ttu-id="dd895-117">Das virtuelle Netzwerk tippen</span><span class="sxs-lookup"><span data-stu-id="dd895-117">The virtual network tap</span></span>

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

### <span data-ttu-id="dd895-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dd895-118">-Confirm</span></span>
<span data-ttu-id="dd895-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dd895-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd895-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd895-120">-WhatIf</span></span>
<span data-ttu-id="dd895-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dd895-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd895-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd895-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd895-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd895-123">CommonParameters</span></span>
<span data-ttu-id="dd895-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd895-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd895-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd895-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd895-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dd895-126">INPUTS</span></span>

### <span data-ttu-id="dd895-127">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="dd895-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="dd895-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dd895-128">OUTPUTS</span></span>

### <span data-ttu-id="dd895-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="dd895-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="dd895-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="dd895-130">NOTES</span></span>

## <span data-ttu-id="dd895-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dd895-131">RELATED LINKS</span></span>

[<span data-ttu-id="dd895-132">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="dd895-132">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="dd895-133">Neu – AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="dd895-133">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="dd895-134">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="dd895-134">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)
