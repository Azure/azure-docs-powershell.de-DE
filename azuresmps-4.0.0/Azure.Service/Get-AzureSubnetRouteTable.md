---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AEFC9094-144F-4E29-AC5A-DBFDA175A920
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8e56496c1fdf04b5227121f5ac39193938a2214e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005748"
---
# <span data-ttu-id="6941a-101">Get-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="6941a-101">Get-AzureSubnetRouteTable</span></span>

## <span data-ttu-id="6941a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6941a-102">SYNOPSIS</span></span>
<span data-ttu-id="6941a-103">Ruft eine Routentabelle für ein Subnetz ab.</span><span class="sxs-lookup"><span data-stu-id="6941a-103">Gets a route table for a subnet.</span></span>

## <span data-ttu-id="6941a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6941a-104">SYNTAX</span></span>

```
Get-AzureSubnetRouteTable -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6941a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6941a-105">DESCRIPTION</span></span>
<span data-ttu-id="6941a-106">Das Cmdlet " **Get-AzureSubnetRouteTable** " Ruft die Routingtabelle ab, die einem Subnetz zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6941a-106">The **Get-AzureSubnetRouteTable** cmdlet gets the route table that is associated with a subnet.</span></span>

## <span data-ttu-id="6941a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6941a-107">EXAMPLES</span></span>

### <span data-ttu-id="6941a-108">Beispiel 1: Anzeigen von Routen für ein Subnetz</span><span class="sxs-lookup"><span data-stu-id="6941a-108">Example 1: Display routes for a subnet</span></span>
```
PS C:\> Get-AzureSubnetRouteTable -VirtualNetworkName "VNetUSCentral" -SubnetName "ContosoSubnet" -Detailed
Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{internetroute}               PublicRT                      Central US                    Sample RT in Central US
```

<span data-ttu-id="6941a-109">Dieser Befehl zeigt die Routen im Namen der Routingtabelle an, die dem Subnetz mit dem Namen ContosoSubnet zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6941a-109">This command displays the routes in the route table name that is associated with subnet named ContosoSubnet.</span></span>

## <span data-ttu-id="6941a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6941a-110">PARAMETERS</span></span>

### <span data-ttu-id="6941a-111">-Detailliert</span><span class="sxs-lookup"><span data-stu-id="6941a-111">-Detailed</span></span>
<span data-ttu-id="6941a-112">Gibt an, dass dieses Cmdlet die Routen in der Routingtabelle anzeigt, die dem Subnetz zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6941a-112">Indicates that this cmdlet displays the routes in the route table that is associated with the subnet.</span></span>

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

### <span data-ttu-id="6941a-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="6941a-113">-Profile</span></span>
<span data-ttu-id="6941a-114">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="6941a-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="6941a-115">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="6941a-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6941a-116">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="6941a-116">-SubnetName</span></span>
<span data-ttu-id="6941a-117">Gibt das Subnetz an, für das dieses Cmdlet die Route-Tabelle abruft.</span><span class="sxs-lookup"><span data-stu-id="6941a-117">Specifies the subnet for which this cmdlet gets the route table.</span></span>

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

### <span data-ttu-id="6941a-118">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="6941a-118">-VirtualNetworkName</span></span>
<span data-ttu-id="6941a-119">Gibt den Namen eines virtuellen Netzwerks an, das das Subnetz enthält, für das dieses Cmdlet die Route-Tabelle erhält.</span><span class="sxs-lookup"><span data-stu-id="6941a-119">Specifies the name of a virtual network that contains the subnet for which this cmdlet gets the route table.</span></span>

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

### <span data-ttu-id="6941a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6941a-120">CommonParameters</span></span>
<span data-ttu-id="6941a-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6941a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6941a-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6941a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6941a-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6941a-123">INPUTS</span></span>

## <span data-ttu-id="6941a-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6941a-124">OUTPUTS</span></span>

## <span data-ttu-id="6941a-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="6941a-125">NOTES</span></span>

## <span data-ttu-id="6941a-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6941a-126">RELATED LINKS</span></span>

[<span data-ttu-id="6941a-127">Remove-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="6941a-127">Remove-AzureSubnetRouteTable</span></span>](./Remove-AzureSubnetRouteTable.md)

[<span data-ttu-id="6941a-128">Satz-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="6941a-128">Set-AzureSubnetRouteTable</span></span>](./Set-AzureSubnetRouteTable.md)


