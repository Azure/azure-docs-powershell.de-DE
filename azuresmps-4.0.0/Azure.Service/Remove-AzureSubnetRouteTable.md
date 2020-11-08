---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AA2F2793-03A5-41D9-8021-D18BE98DB044
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9bf26bd23ecc3dcb9e6973baf4c5eecf3d544402
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006662"
---
# <span data-ttu-id="3a3c7-101">Remove-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="3a3c7-101">Remove-AzureSubnetRouteTable</span></span>

## <span data-ttu-id="3a3c7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3a3c7-102">SYNOPSIS</span></span>
<span data-ttu-id="3a3c7-103">Entfernt eine Routingtabellen Zuordnung aus einem Subnetz.</span><span class="sxs-lookup"><span data-stu-id="3a3c7-103">Removes a route table association from a subnet.</span></span>

## <span data-ttu-id="3a3c7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a3c7-104">SYNTAX</span></span>

```
Remove-AzureSubnetRouteTable -VirtualNetworkName <String> -SubnetName <String> [-Force] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3a3c7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a3c7-105">DESCRIPTION</span></span>
<span data-ttu-id="3a3c7-106">Das Cmdlet **Remove-AzureSubnetRouteTable** entfernt eine Routingtabellen Zuordnung aus einem Subnetz.</span><span class="sxs-lookup"><span data-stu-id="3a3c7-106">The **Remove-AzureSubnetRouteTable** cmdlet removes a route table association from a subnet.</span></span>

## <span data-ttu-id="3a3c7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3a3c7-107">EXAMPLES</span></span>

### <span data-ttu-id="3a3c7-108">Beispiel 1: Entfernen einer Zuordnung zwischen einer Routingtabelle und einem Subnetz</span><span class="sxs-lookup"><span data-stu-id="3a3c7-108">Example 1: Remove an association between a route table and a subnet</span></span>
```
PS C:\> Remove-AzureSubnetRouteTable -VirtualNetworkName "VNetUSCentral" -SubnetName "ContosoSubnet"
```

<span data-ttu-id="3a3c7-109">Mit diesem Befehl wird die Zuordnung der Route-Tabelle mit dem Namen PublicRouteTable zum Subnetz mit dem Namen ContosoSubnet entfernt.</span><span class="sxs-lookup"><span data-stu-id="3a3c7-109">This command removes the association of the route table named PublicRouteTable to the subnet named ContosoSubnet.</span></span>

## <span data-ttu-id="3a3c7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a3c7-110">PARAMETERS</span></span>

### <span data-ttu-id="3a3c7-111">-Force</span><span class="sxs-lookup"><span data-stu-id="3a3c7-111">-Force</span></span>
<span data-ttu-id="3a3c7-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="3a3c7-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3a3c7-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a3c7-113">-PassThru</span></span>
<span data-ttu-id="3a3c7-114">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="3a3c7-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="3a3c7-115">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="3a3c7-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3a3c7-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="3a3c7-116">-Profile</span></span>
<span data-ttu-id="3a3c7-117">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="3a3c7-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="3a3c7-118">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="3a3c7-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3a3c7-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="3a3c7-119">-SubnetName</span></span>
<span data-ttu-id="3a3c7-120">Gibt das Subnetz an, für das dieses Cmdlet die Route-Tabelle entfernt.</span><span class="sxs-lookup"><span data-stu-id="3a3c7-120">Specifies the subnet for which this cmdlet removes the route table.</span></span>

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

### <span data-ttu-id="3a3c7-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="3a3c7-121">-VirtualNetworkName</span></span>
<span data-ttu-id="3a3c7-122">Gibt den Namen eines virtuellen Netzwerks an, das das Subnetz enthält, für das dieses Cmdlet die Route-Tabelle entfernt.</span><span class="sxs-lookup"><span data-stu-id="3a3c7-122">Specifies the name of a virtual network that contains the subnet for which this cmdlet removes the route table.</span></span>

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

### <span data-ttu-id="3a3c7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a3c7-123">CommonParameters</span></span>
<span data-ttu-id="3a3c7-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a3c7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a3c7-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a3c7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a3c7-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3a3c7-126">INPUTS</span></span>

## <span data-ttu-id="3a3c7-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3a3c7-127">OUTPUTS</span></span>

## <span data-ttu-id="3a3c7-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="3a3c7-128">NOTES</span></span>

## <span data-ttu-id="3a3c7-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3a3c7-129">RELATED LINKS</span></span>

[<span data-ttu-id="3a3c7-130">Get-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="3a3c7-130">Get-AzureSubnetRouteTable</span></span>](./Get-AzureSubnetRouteTable.md)

[<span data-ttu-id="3a3c7-131">Satz-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="3a3c7-131">Set-AzureSubnetRouteTable</span></span>](./Set-AzureSubnetRouteTable.md)


