---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
ms.openlocfilehash: 3130aec4a5032fd62423aa35dec73d7acd6e14b2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660132"
---
# <span data-ttu-id="a00a8-101">Test-AzPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="a00a8-101">Test-AzPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="a00a8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a00a8-102">SYNOPSIS</span></span>
<span data-ttu-id="a00a8-103">Testen der Verfügbarkeit einer privaten IP-Adresse in einem virtuellen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="a00a8-103">Test availability of a private IP address in a virtual network.</span></span>

## <span data-ttu-id="a00a8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a00a8-104">SYNTAX</span></span>

### <span data-ttu-id="a00a8-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="a00a8-105">TestByResource</span></span>
```
Test-AzPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a00a8-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="a00a8-106">TestByResourceId</span></span>
```
Test-AzPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a00a8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a00a8-107">DESCRIPTION</span></span>
<span data-ttu-id="a00a8-108">Das Cmdlet **Test-AzPrivateIPAddressAvailability** testet, ob eine angegebene private IP-Adresse in einem virtuellen Netzwerk zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="a00a8-108">The **Test-AzPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="a00a8-109">Dieses Cmdlet gibt eine Liste der verfügbaren privaten IP-Adressen zurück, wenn die angeforderte private IP-Adresse übernommen wird.</span><span class="sxs-lookup"><span data-stu-id="a00a8-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="a00a8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a00a8-110">EXAMPLES</span></span>

### <span data-ttu-id="a00a8-111">Beispiel 1: testen, ob eine IP-Adresse über die Pipeline verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="a00a8-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="a00a8-112">Dieser Befehl ruft ein virtuelles Netzwerk ab und verwendet den Pipelineoperator, um ihn an **Test-AzPrivateIPAddressAvailability** zu übergeben, wodurch überprüft wird, ob die angegebene private IP-Adresse verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a00a8-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="a00a8-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a00a8-113">PARAMETERS</span></span>

### <span data-ttu-id="a00a8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a00a8-114">-DefaultProfile</span></span>
<span data-ttu-id="a00a8-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a00a8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a00a8-116">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="a00a8-116">-IPAddress</span></span>
<span data-ttu-id="a00a8-117">Gibt die zu testende IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="a00a8-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="a00a8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a00a8-118">-ResourceGroupName</span></span>
<span data-ttu-id="a00a8-119">Gibt den Namen der Ressourcengruppe für das virtuelle Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="a00a8-119">Specifies the name of the resource group for the virtual network.</span></span>

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

### <span data-ttu-id="a00a8-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a00a8-120">-VirtualNetwork</span></span>
<span data-ttu-id="a00a8-121">Gibt ein **PSVirtualNetwork** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a00a8-121">Specifies a **PSVirtualNetwork** object.</span></span>

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

### <span data-ttu-id="a00a8-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="a00a8-122">-VirtualNetworkName</span></span>
<span data-ttu-id="a00a8-123">Gibt den Namen des virtuellen Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="a00a8-123">Specifies the name of the virtual network.</span></span>

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

### <span data-ttu-id="a00a8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a00a8-124">CommonParameters</span></span>
<span data-ttu-id="a00a8-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a00a8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a00a8-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a00a8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a00a8-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a00a8-127">INPUTS</span></span>

### <span data-ttu-id="a00a8-128">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a00a8-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="a00a8-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a00a8-129">OUTPUTS</span></span>

### <span data-ttu-id="a00a8-130">Microsoft. Azure. Commands. Network. Models. PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="a00a8-130">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="a00a8-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="a00a8-131">NOTES</span></span>

## <span data-ttu-id="a00a8-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a00a8-132">RELATED LINKS</span></span>

[<span data-ttu-id="a00a8-133">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a00a8-133">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)


