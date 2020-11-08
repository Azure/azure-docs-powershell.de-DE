---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 7E40C4A2-8B9A-47E8-82AB-19208247349C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 893e03f8e59b3cd01e7d96ca2d04119ee6fb4c66
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006018"
---
# <span data-ttu-id="6f122-101">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="6f122-101">Set-AzureSubnetRouteTable</span></span>

## <span data-ttu-id="6f122-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6f122-102">SYNOPSIS</span></span>
<span data-ttu-id="6f122-103">Ordnet eine Routingtabelle einem Subnetz zu.</span><span class="sxs-lookup"><span data-stu-id="6f122-103">Associates a route table to a subnet.</span></span>

## <span data-ttu-id="6f122-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f122-104">SYNTAX</span></span>

```
Set-AzureSubnetRouteTable -VirtualNetworkName <String> -SubnetName <String> -RouteTableName <String>
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6f122-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6f122-105">DESCRIPTION</span></span>
<span data-ttu-id="6f122-106">Das Cmdlet " **Satz-AzureSubnetRouteTable** " ordnet eine Routingtabelle einem Subnetz zu.</span><span class="sxs-lookup"><span data-stu-id="6f122-106">The **Set-AzureSubnetRouteTable** cmdlet associates a route table to a subnet.</span></span>

## <span data-ttu-id="6f122-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6f122-107">EXAMPLES</span></span>

### <span data-ttu-id="6f122-108">Beispiel 1: Zuordnen einer Routentabelle zu einem Subnetz</span><span class="sxs-lookup"><span data-stu-id="6f122-108">Example 1: Associate a route table to a subnet</span></span>
```
PS C:\> Set-AzureSubnetRouteTable -VirtualNetworkName "VNetUSCentral" -SubnetName "ContosoSubnet" -RouteTableName "PublicRouteTable"
```

<span data-ttu-id="6f122-109">Dieser Befehl ordnet die Routingtabelle mit dem Namen PublicRouteTable dem Subnetz mit dem Namen ContosoSubnet zu.</span><span class="sxs-lookup"><span data-stu-id="6f122-109">This command associates the route table named PublicRouteTable to the subnet named ContosoSubnet.</span></span>

## <span data-ttu-id="6f122-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f122-110">PARAMETERS</span></span>

### <span data-ttu-id="6f122-111">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f122-111">-PassThru</span></span>
<span data-ttu-id="6f122-112">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="6f122-112">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6f122-113">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="6f122-113">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f122-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="6f122-114">-Profile</span></span>
<span data-ttu-id="6f122-115">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="6f122-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6f122-116">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="6f122-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f122-117">-RouteTableName</span><span class="sxs-lookup"><span data-stu-id="6f122-117">-RouteTableName</span></span>
<span data-ttu-id="6f122-118">Gibt den Namen der Arbeitsplan Tabelle an, die dieses Cmdlet einem Subnetz zuordnet.</span><span class="sxs-lookup"><span data-stu-id="6f122-118">Specifies the name of the route table that this cmdlet associates with a subnet.</span></span>

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

### <span data-ttu-id="6f122-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="6f122-119">-SubnetName</span></span>
<span data-ttu-id="6f122-120">Gibt das Subnetz an, dem dieses Cmdlet die Route-Tabelle zuordnet.</span><span class="sxs-lookup"><span data-stu-id="6f122-120">Specifies the subnet to which this cmdlet associates the route table.</span></span>

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

### <span data-ttu-id="6f122-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="6f122-121">-VirtualNetworkName</span></span>
<span data-ttu-id="6f122-122">Gibt den Namen eines virtuellen Netzwerks an, das das Subnetz enthält, dem dieses Cmdlet die Route-Tabelle zuordnet.</span><span class="sxs-lookup"><span data-stu-id="6f122-122">Specifies the name of a virtual network that contains the subnet to which this cmdlet associates the route table.</span></span>

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

### <span data-ttu-id="6f122-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f122-123">CommonParameters</span></span>
<span data-ttu-id="6f122-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f122-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f122-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f122-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f122-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6f122-126">INPUTS</span></span>

## <span data-ttu-id="6f122-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6f122-127">OUTPUTS</span></span>

## <span data-ttu-id="6f122-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="6f122-128">NOTES</span></span>

## <span data-ttu-id="6f122-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6f122-129">RELATED LINKS</span></span>

[<span data-ttu-id="6f122-130">Get-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="6f122-130">Get-AzureSubnetRouteTable</span></span>](./Get-AzureSubnetRouteTable.md)

[<span data-ttu-id="6f122-131">Remove-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="6f122-131">Remove-AzureSubnetRouteTable</span></span>](./Remove-AzureSubnetRouteTable.md)
