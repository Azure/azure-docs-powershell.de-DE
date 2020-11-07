---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0780CB09-9C3B-468A-A718-3A646FE3D152
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivateipaddressavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzPrivateIPAddressAvailability.md
ms.openlocfilehash: 6a5ee3b03a4242c3c11d5c34da4a333ee7c82843
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843504"
---
# <span data-ttu-id="2243b-101">Test-AzPrivateIPAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="2243b-101">Test-AzPrivateIPAddressAvailability</span></span>

## <span data-ttu-id="2243b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2243b-102">SYNOPSIS</span></span>
<span data-ttu-id="2243b-103">Testen der Verfügbarkeit einer privaten IP-Adresse in einem virtuellen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="2243b-103">Test availability of a private IP address in a virtual network.</span></span>

## <span data-ttu-id="2243b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2243b-104">SYNTAX</span></span>

### <span data-ttu-id="2243b-105">TestByResource</span><span class="sxs-lookup"><span data-stu-id="2243b-105">TestByResource</span></span>
```
Test-AzPrivateIPAddressAvailability -VirtualNetwork <PSVirtualNetwork> -IPAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2243b-106">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="2243b-106">TestByResourceId</span></span>
```
Test-AzPrivateIPAddressAvailability -ResourceGroupName <String> -VirtualNetworkName <String>
 -IPAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2243b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2243b-107">DESCRIPTION</span></span>
<span data-ttu-id="2243b-108">Das Cmdlet **Test-AzPrivateIPAddressAvailability** testet, ob eine angegebene private IP-Adresse in einem virtuellen Netzwerk zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="2243b-108">The **Test-AzPrivateIPAddressAvailability** cmdlet tests whether a specified private IP address is available in a virtual network.</span></span>
<span data-ttu-id="2243b-109">Dieses Cmdlet gibt eine Liste der verfügbaren privaten IP-Adressen zurück, wenn die angeforderte private IP-Adresse übernommen wird.</span><span class="sxs-lookup"><span data-stu-id="2243b-109">This cmdlet returns a list of available private IP addresses if the requested private IP address is taken.</span></span>

## <span data-ttu-id="2243b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2243b-110">EXAMPLES</span></span>

### <span data-ttu-id="2243b-111">Beispiel 1: testen, ob eine IP-Adresse über die Pipeline verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="2243b-111">Example 1: Test whether an IP address is available using the pipeline</span></span>
```
PS C:\>Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $rgname | Test-AzPrivateIPAddressAvailability -IPAddress "10.0.1.10"
```

<span data-ttu-id="2243b-112">Dieser Befehl ruft ein virtuelles Netzwerk ab und verwendet den Pipelineoperator, um ihn an **Test-AzPrivateIPAddressAvailability** zu übergeben, wodurch überprüft wird, ob die angegebene private IP-Adresse verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="2243b-112">This command gets a virtual network and uses the pipeline operator to pass it to **Test-AzPrivateIPAddressAvailability** , which tests whether the specified private IP address is available.</span></span>

## <span data-ttu-id="2243b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2243b-113">PARAMETERS</span></span>

### <span data-ttu-id="2243b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2243b-114">-DefaultProfile</span></span>
<span data-ttu-id="2243b-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2243b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2243b-116">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="2243b-116">-IPAddress</span></span>
<span data-ttu-id="2243b-117">Gibt die zu testende IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="2243b-117">Specifies the IP address to test.</span></span>

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

### <span data-ttu-id="2243b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2243b-118">-ResourceGroupName</span></span>
<span data-ttu-id="2243b-119">Gibt den Namen der Ressourcengruppe für das virtuelle Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="2243b-119">Specifies the name of the resource group for the virtual network.</span></span>

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

### <span data-ttu-id="2243b-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2243b-120">-VirtualNetwork</span></span>
<span data-ttu-id="2243b-121">Gibt ein **PSVirtualNetwork** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="2243b-121">Specifies a **PSVirtualNetwork** object.</span></span>

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

### <span data-ttu-id="2243b-122">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="2243b-122">-VirtualNetworkName</span></span>
<span data-ttu-id="2243b-123">Gibt den Namen des virtuellen Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="2243b-123">Specifies the name of the virtual network.</span></span>

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

### <span data-ttu-id="2243b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2243b-124">CommonParameters</span></span>
<span data-ttu-id="2243b-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2243b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2243b-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2243b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2243b-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2243b-127">INPUTS</span></span>

### <span data-ttu-id="2243b-128">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2243b-128">PSVirtualNetwork</span></span>
<span data-ttu-id="2243b-129">Der Parameter "VirtualNetwork" akzeptiert den Wert vom Typ "PSVirtualNetwork" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="2243b-129">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="2243b-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2243b-130">OUTPUTS</span></span>

### <span data-ttu-id="2243b-131">Microsoft. Azure. Commands. Network. Models. PSIPAddressAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="2243b-131">Microsoft.Azure.Commands.Network.Models.PSIPAddressAvailabilityResult</span></span>

## <span data-ttu-id="2243b-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="2243b-132">NOTES</span></span>

## <span data-ttu-id="2243b-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2243b-133">RELATED LINKS</span></span>

[<span data-ttu-id="2243b-134">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2243b-134">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)


