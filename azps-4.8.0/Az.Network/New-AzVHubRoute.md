---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
ms.openlocfilehash: 7dce18ce266bbd2e92f09039b1772acfc618dbdd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165206"
---
# <span data-ttu-id="cde6c-101">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="cde6c-101">New-AzVHubRoute</span></span>

## <span data-ttu-id="cde6c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cde6c-102">SYNOPSIS</span></span>
<span data-ttu-id="cde6c-103">Erstellt ein VHubRoute-Objekt, das als Parameter an den Befehl New-AzVHubRouteTable übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="cde6c-103">Creates a VHubRoute object which can be passed as parameter to the New-AzVHubRouteTable command.</span></span>

## <span data-ttu-id="cde6c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cde6c-104">SYNTAX</span></span>

```powershell
New-AzVHubRoute -Name <String> -Destination <String[]> -DestinationType <String> -NextHop <String> -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cde6c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cde6c-105">DESCRIPTION</span></span>

<span data-ttu-id="cde6c-106">Erstellt ein VHubRoute-Objekt.</span><span class="sxs-lookup"><span data-stu-id="cde6c-106">Creates a VHubRoute object.</span></span>

## <span data-ttu-id="cde6c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cde6c-107">EXAMPLES</span></span>

### <span data-ttu-id="cde6c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cde6c-108">Example 1</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $firewallName = "testFirewall"
PS C:\> $firewall = Get-AzFirewall -Name $firewallName -ResourceGroupName $rgName
PS C:\> New-AzVHubRoute -Name "private-traffic" -Destination @("10.30.0.0/16", "10.40.0.0/16") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"

Name            : private-traffic
DestinationType : CIDR
Destinations    : {10.30.0.0/16, 10.40.0.0/16}
NextHopType     : ResourceId
NextHop         : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall
```

<span data-ttu-id="cde6c-109">Mit dem obigen Befehl wird ein VHubRoute-Objekt mit nextHop als angegebenen Firewall erstellt, das dann einer VHubRouteTable-Ressource hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="cde6c-109">The above command will create a VHubRoute object with nextHop as the specified Firewall which can then be added to a VHubRouteTable resource.</span></span>

### <span data-ttu-id="cde6c-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="cde6c-110">Example 2</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $hubName = "testHub"
PS C:\> $hubVnetConnName = "testHubVnetConn"
PS C:\> $hubVnetConnection = Get-AzVirtualHubVnetConnection -Name $hubVnetConnName -ParentResourceName $hubName -ResourceGroupName $rgName
PS C:\> New-AzVHubRoute -Name "nva-traffic" -Destination @("10.20.0.0/16", "10.50.0.0/16") -DestinationType "CIDR" -NextHop $hubVnetConnection.Id -NextHopType "ResourceId"

Name            : private-traffic
DestinationType : CIDR
Destinations    : {10.30.0.0/16, 10.40.0.0/16}
NextHopType     : ResourceId
NextHop         : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubVirtualNetworkConnections/testHubVnetConn
```

<span data-ttu-id="cde6c-111">Der obige Befehl erstellt ein VHubRoute-Objekt mit nextHop als angegebenen hubVnetConnection, das dann einer VHubRouteTable-Ressource hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="cde6c-111">The above command will create a VHubRoute object with nextHop as the specified hubVnetConnection which can then be added to a VHubRouteTable resource.</span></span>

## <span data-ttu-id="cde6c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="cde6c-112">PARAMETERS</span></span>

### <span data-ttu-id="cde6c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cde6c-113">-DefaultProfile</span></span>
<span data-ttu-id="cde6c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cde6c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cde6c-115">-Ziel</span><span class="sxs-lookup"><span data-stu-id="cde6c-115">-Destination</span></span>
<span data-ttu-id="cde6c-116">Liste der Ziele.</span><span class="sxs-lookup"><span data-stu-id="cde6c-116">List of Destinations.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cde6c-117">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="cde6c-117">-DestinationType</span></span>
<span data-ttu-id="cde6c-118">Art der Ziele.</span><span class="sxs-lookup"><span data-stu-id="cde6c-118">Type of Destinations.</span></span>

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

### <span data-ttu-id="cde6c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="cde6c-119">-Name</span></span>
<span data-ttu-id="cde6c-120">Der Name der Route.</span><span class="sxs-lookup"><span data-stu-id="cde6c-120">The route name.</span></span>

```yaml
Type: String
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cde6c-121">-NextHop</span><span class="sxs-lookup"><span data-stu-id="cde6c-121">-NextHop</span></span>
<span data-ttu-id="cde6c-122">Nächster Hop.</span><span class="sxs-lookup"><span data-stu-id="cde6c-122">The next hop.</span></span>

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

### <span data-ttu-id="cde6c-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="cde6c-123">-NextHopType</span></span>
<span data-ttu-id="cde6c-124">Der nächste Hop-Typ.</span><span class="sxs-lookup"><span data-stu-id="cde6c-124">The Next Hop type.</span></span>

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

### <span data-ttu-id="cde6c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cde6c-125">CommonParameters</span></span>
<span data-ttu-id="cde6c-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cde6c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cde6c-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cde6c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cde6c-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cde6c-128">INPUTS</span></span>

### <span data-ttu-id="cde6c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="cde6c-129">System.String</span></span>

## <span data-ttu-id="cde6c-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cde6c-130">OUTPUTS</span></span>

### <span data-ttu-id="cde6c-131">Microsoft. Azure. Commands. Network. Models. PSVHubRoute</span><span class="sxs-lookup"><span data-stu-id="cde6c-131">Microsoft.Azure.Commands.Network.Models.PSVHubRoute</span></span>

## <span data-ttu-id="cde6c-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="cde6c-132">NOTES</span></span>

## <span data-ttu-id="cde6c-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cde6c-133">RELATED LINKS</span></span>

[<span data-ttu-id="cde6c-134">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cde6c-134">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="cde6c-135">Neu – AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cde6c-135">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="cde6c-136">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cde6c-136">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="cde6c-137">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cde6c-137">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)