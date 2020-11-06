---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmPrivateIPAddressAvailability.md
ms.openlocfilehash: 769f8a5f8f95e5a97af8a495e0edbaba6b75a5d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496378"
---
# <span data-ttu-id="3adea-101">Test-AzureRmPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="3adea-101">Test-AzureRmPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="3adea-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3adea-102">SYNOPSIS</span></span>
<span data-ttu-id="3adea-103">Testen der Verfügbarkeit einer privaten IP-Adresse in einem virtuellen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="3adea-103">Test availability of a private IP address in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3adea-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3adea-104">SYNTAX</span></span>

### <span data-ttu-id="3adea-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="3adea-105">TestByResource</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3adea-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="3adea-106">TestByResourceId</span></span>
```
Test-AzureRmPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3adea-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3adea-107">DESCRIPTION</span></span>
<span data-ttu-id="3adea-108">Das Cmdlet **Test-AzureRmPrivateIPAddressAvailability** testet, ob eine angegebene private IP-Adresse in einem virtuellen Netzwerk zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="3adea-108">The **Test-AzureRmPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="3adea-109">Dieses Cmdlet gibt eine Liste der verfügbaren privaten IP-Adressen zurück, wenn die angeforderte private IP-Adresse übernommen wird.</span><span class="sxs-lookup"><span data-stu-id="3adea-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="3adea-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3adea-110">EXAMPLES</span></span>

### <span data-ttu-id="3adea-111">Beispiel 1: testen, ob eine IP-Adresse über die Pipeline verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="3adea-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzureRmVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzureRmPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="3adea-112">Dieser Befehl ruft ein virtuelles Netzwerk ab und verwendet den Pipelineoperator, um ihn an **Test-AzureRmPrivateIPAddressAvailability** zu übergeben, wodurch überprüft wird, ob die angegebene private IP-Adresse verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3adea-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzureRmPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="3adea-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="3adea-113">PARAMETERS</span></span>

### <span data-ttu-id="3adea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3adea-114">-DefaultProfile</span></span>
<span data-ttu-id="3adea-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3adea-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3adea-116">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="3adea-116">-IPAddress</span></span>
<span data-ttu-id="3adea-117">Gibt die zu testende IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="3adea-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="3adea-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3adea-118">-ResourceGroupName</span></span>
<span data-ttu-id="3adea-119">Gibt den Namen der Ressourcengruppe für das virtuelle Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="3adea-119">Specifies the name of the resource group for the virtual network.</span></span>

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

### <span data-ttu-id="3adea-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3adea-120">-VirtualNetwork</span></span>
<span data-ttu-id="3adea-121">Gibt ein **PSVirtualNetwork** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="3adea-121">Specifies a **PSVirtualNetwork** object.</span></span>

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

### <span data-ttu-id="3adea-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="3adea-122">-VirtualNetworkName</span></span>
<span data-ttu-id="3adea-123">Gibt den Namen des virtuellen Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="3adea-123">Specifies the name of the virtual network.</span></span>

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

### <span data-ttu-id="3adea-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3adea-124">CommonParameters</span></span>
<span data-ttu-id="3adea-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3adea-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3adea-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3adea-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3adea-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3adea-127">INPUTS</span></span>

### <span data-ttu-id="3adea-128">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3adea-128">PSVirtualNetwork</span></span>
<span data-ttu-id="3adea-129">Der Parameter "VirtualNetwork" akzeptiert den Wert vom Typ "PSVirtualNetwork" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="3adea-129">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="3adea-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3adea-130">OUTPUTS</span></span>

### <span data-ttu-id="3adea-131">Microsoft. Azure. Commands. Network. Models. PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="3adea-131">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="3adea-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="3adea-132">NOTES</span></span>

## <span data-ttu-id="3adea-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3adea-133">RELATED LINKS</span></span>

[<span data-ttu-id="3adea-134">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3adea-134">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)


