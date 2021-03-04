---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/powershell/module/az.network/test-azprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
ms.openlocfilehash: a39dd390e0307662c8105bf84999ae8dfc1fc7aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918475"
---
# <span data-ttu-id="f4e21-101">Test-AzPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="f4e21-101">Test-AzPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="f4e21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4e21-102">SYNOPSIS</span></span>
<span data-ttu-id="f4e21-103">Testen Sie die Verfügbarkeit einer privaten IP-Adresse in einem virtuellen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="f4e21-103">Test availability of a private IP address in a virtual network.</span></span>

## <span data-ttu-id="f4e21-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4e21-104">SYNTAX</span></span>

### <span data-ttu-id="f4e21-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="f4e21-105">TestByResource</span></span>
```
Test-AzPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4e21-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="f4e21-106">TestByResourceId</span></span>
```
Test-AzPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4e21-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f4e21-107">DESCRIPTION</span></span>
<span data-ttu-id="f4e21-108">Das **Cmdlet Test-AzPrivateIPAddressAvailability** testet, ob eine angegebene private IP-Adresse in einem virtuellen Netzwerk verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f4e21-108">The **Test-AzPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="f4e21-109">Dieses Cmdlet gibt eine Liste der verfügbaren privaten IP-Adressen zurück, wenn die angeforderte private IP-Adresse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f4e21-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="f4e21-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f4e21-110">EXAMPLES</span></span>

### <span data-ttu-id="f4e21-111">Beispiel 1: Testen, ob eine IP-Adresse über die Pipeline verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="f4e21-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="f4e21-112">Dieser Befehl ruft ein virtuelles Netzwerk ab und verwendet den Pipelineoperator, um es an **Test-AzPrivateIPAddressAvailability** zu übergeben, wodurch überprüft wird, ob die angegebene private IP-Adresse verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f4e21-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzPrivateIPAddressAvailability**, which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="f4e21-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f4e21-113">PARAMETERS</span></span>

### <span data-ttu-id="f4e21-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4e21-114">-DefaultProfile</span></span>
<span data-ttu-id="f4e21-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f4e21-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4e21-116">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="f4e21-116">-IPAddress</span></span>
<span data-ttu-id="f4e21-117">Gibt die zu testende IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="f4e21-117">Specifies the IP address to test.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e21-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4e21-118">-ResourceGroupName</span></span>
<span data-ttu-id="f4e21-119">Gibt den Namen der Ressourcengruppe für das virtuelle Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="f4e21-119">Specifies the name of the resource group for the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e21-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f4e21-120">-VirtualNetwork</span></span>
<span data-ttu-id="f4e21-121">Gibt ein **PSVirtualNetwork-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="f4e21-121">Specifies a **PSVirtualNetwork** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: TestByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4e21-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="f4e21-122">-VirtualNetworkName</span></span>
<span data-ttu-id="f4e21-123">Gibt den Namen des virtuellen Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="f4e21-123">Specifies the name of the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e21-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4e21-124">CommonParameters</span></span>
<span data-ttu-id="f4e21-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4e21-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4e21-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4e21-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4e21-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f4e21-127">INPUTS</span></span>

### <span data-ttu-id="f4e21-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f4e21-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="f4e21-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f4e21-129">OUTPUTS</span></span>

### <span data-ttu-id="f4e21-130">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="f4e21-130">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="f4e21-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f4e21-131">NOTES</span></span>

## <span data-ttu-id="f4e21-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f4e21-132">RELATED LINKS</span></span>

[<span data-ttu-id="f4e21-133">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f4e21-133">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)


