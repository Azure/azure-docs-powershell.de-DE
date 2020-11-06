---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: 1d767677c547c2418ca19e3206f3ca5a25638de0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504321"
---
# <span data-ttu-id="0b102-101">Set-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="0b102-101">Set-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="0b102-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0b102-102">SYNOPSIS</span></span>
<span data-ttu-id="0b102-103">Legt den Zielstatus für einen virtuellen Netzwerk Hahn fest.</span><span class="sxs-lookup"><span data-stu-id="0b102-103">Sets the goal state for a virtual network tap.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b102-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b102-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b102-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b102-105">DESCRIPTION</span></span>
<span data-ttu-id="0b102-106">Das **Set-AzureRmVirtualNetworkTap-** Element legt den Zielstatus für ein Azure Virtual Network Tap fest.</span><span class="sxs-lookup"><span data-stu-id="0b102-106">The **Set-AzureRmVirtualNetworkTap** sets the goal state for an Azure virtual network tap.</span></span>

## <span data-ttu-id="0b102-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b102-107">EXAMPLES</span></span>

### <span data-ttu-id="0b102-108">Beispiel 1: Konfigurieren eines virtuellen Netzwerk Hahns</span><span class="sxs-lookup"><span data-stu-id="0b102-108">Example 1: Configure a Virtual network tap</span></span>
```
PS C:\>$vTap = Get-AzureRmVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzureRmVirtualNetworkTap -VirtualNetworkTap $vTap
```

<span data-ttu-id="0b102-109">Der Befehl aktualisiert das Ziel IPKonfigurationsdateiAddress und aktualisiert das virtuelle Netzwerk Tap.</span><span class="sxs-lookup"><span data-stu-id="0b102-109">The command updates the Destination IpConfiguration and updates the Virtual network tap.</span></span>
<span data-ttu-id="0b102-110">Wenn es auf eine Tap-Konfiguration ankommt, die darauf verweist, wird der gesamte Quell Verkehr nicht mit dem neuen Ziel-IP-Konfigurations Post-Update gespiegelt.</span><span class="sxs-lookup"><span data-stu-id="0b102-110">If there are any tap configurations referencing it, then all the source traffic will not start be mirrored to new destination ip configuration post update.</span></span>

## <span data-ttu-id="0b102-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b102-111">PARAMETERS</span></span>

### <span data-ttu-id="0b102-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b102-112">-AsJob</span></span>
<span data-ttu-id="0b102-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0b102-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0b102-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b102-114">-DefaultProfile</span></span>
<span data-ttu-id="0b102-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0b102-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b102-116">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="0b102-116">-VirtualNetworkTap</span></span>
<span data-ttu-id="0b102-117">Das virtuelle Netzwerk tippen</span><span class="sxs-lookup"><span data-stu-id="0b102-117">The virtual network tap</span></span>

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

### <span data-ttu-id="0b102-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0b102-118">-Confirm</span></span>
<span data-ttu-id="0b102-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0b102-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b102-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b102-120">-WhatIf</span></span>
<span data-ttu-id="0b102-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b102-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b102-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b102-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b102-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b102-123">CommonParameters</span></span>
<span data-ttu-id="0b102-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b102-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b102-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b102-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b102-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0b102-126">INPUTS</span></span>

### <span data-ttu-id="0b102-127">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="0b102-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="0b102-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0b102-128">OUTPUTS</span></span>

### <span data-ttu-id="0b102-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="0b102-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="0b102-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="0b102-130">NOTES</span></span>

## <span data-ttu-id="0b102-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0b102-131">RELATED LINKS</span></span>
