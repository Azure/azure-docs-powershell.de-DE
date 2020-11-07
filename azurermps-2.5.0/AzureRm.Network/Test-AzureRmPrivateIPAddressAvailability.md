---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermprivateipaddressavailability
schema: 2.0.0
ms.openlocfilehash: 73924c1d1308a4cf457033e27e49ad7f9e19392e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848659"
---
# <span data-ttu-id="a8e11-101">Test-AzureRmPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="a8e11-101">Test-AzureRmPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="a8e11-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a8e11-102">SYNOPSIS</span></span>
<span data-ttu-id="a8e11-103">Testen der Verfügbarkeit einer privaten IP-Adresse in einem virtuellen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="a8e11-103">Test availability of a private IP address in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8e11-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8e11-104">SYNTAX</span></span>

### <span data-ttu-id="a8e11-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="a8e11-105">TestByResource</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8e11-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="a8e11-106">TestByResourceId</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8e11-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8e11-107">DESCRIPTION</span></span>
<span data-ttu-id="a8e11-108">Das Cmdlet **Test-AzureRmPrivateIPAddressAvailability** testet, ob eine angegebene private IP-Adresse in einem virtuellen Netzwerk zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="a8e11-108">The **Test-AzureRmPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="a8e11-109">Dieses Cmdlet gibt eine Liste der verfügbaren privaten IP-Adressen zurück, wenn die angeforderte private IP-Adresse übernommen wird.</span><span class="sxs-lookup"><span data-stu-id="a8e11-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="a8e11-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a8e11-110">EXAMPLES</span></span>

### <span data-ttu-id="a8e11-111">Beispiel 1: testen, ob eine IP-Adresse über die Pipeline verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="a8e11-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzureRmVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzureRmPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="a8e11-112">Dieser Befehl ruft ein virtuelles Netzwerk ab und verwendet den Pipelineoperator, um ihn an **Test-AzureRmPrivateIPAddressAvailability** zu übergeben, wodurch überprüft wird, ob die angegebene private IP-Adresse verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a8e11-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzureRmPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="a8e11-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8e11-113">PARAMETERS</span></span>

### <span data-ttu-id="a8e11-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8e11-114">-DefaultProfile</span></span>
<span data-ttu-id="a8e11-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a8e11-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8e11-116">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="a8e11-116">-IPAddress</span></span>
<span data-ttu-id="a8e11-117">Gibt die zu testende IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="a8e11-117">Specifies the IP address to test.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8e11-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8e11-118">-ResourceGroupName</span></span>
<span data-ttu-id="a8e11-119">Gibt den Namen der Ressourcengruppe für das virtuelle Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="a8e11-119">Specifies the name of the resource group for the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: TestByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8e11-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a8e11-120">-VirtualNetwork</span></span>
<span data-ttu-id="a8e11-121">Gibt ein **PSVirtualNetwork** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a8e11-121">Specifies a **PSVirtualNetwork** object.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: TestByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e11-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="a8e11-122">-VirtualNetworkName</span></span>
<span data-ttu-id="a8e11-123">Gibt den Namen des virtuellen Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="a8e11-123">Specifies the name of the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: TestByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8e11-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8e11-124">CommonParameters</span></span>
<span data-ttu-id="a8e11-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8e11-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8e11-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8e11-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8e11-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a8e11-127">INPUTS</span></span>

### <span data-ttu-id="a8e11-128">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a8e11-128">PSVirtualNetwork</span></span>
<span data-ttu-id="a8e11-129">Der Parameter "VirtualNetwork" akzeptiert den Wert vom Typ "PSVirtualNetwork" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a8e11-129">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="a8e11-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a8e11-130">OUTPUTS</span></span>

### <span data-ttu-id="a8e11-131">Microsoft. Azure. Commands. Network. Models. PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="a8e11-131">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="a8e11-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="a8e11-132">NOTES</span></span>

## <span data-ttu-id="a8e11-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a8e11-133">RELATED LINKS</span></span>

[<span data-ttu-id="a8e11-134">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a8e11-134">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)


