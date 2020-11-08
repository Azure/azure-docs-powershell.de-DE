---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A7DFF559-188D-4CF9-9315-CA327E0C5C0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: d502ba2961e5238426228e4ac58a29b922be81f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006029"
---
# <span data-ttu-id="11793-101">Set-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="11793-101">Set-AzureRoute</span></span>

## <span data-ttu-id="11793-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="11793-102">SYNOPSIS</span></span>
<span data-ttu-id="11793-103">Erstellt eine Route in einer Route-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="11793-103">Creates a route in a route table.</span></span>

## <span data-ttu-id="11793-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="11793-104">SYNTAX</span></span>

```
Set-AzureRoute -RouteName <String> -AddressPrefix <String> -NextHopType <String> [-NextHopIpAddress <String>]
 -RouteTable <IRouteTable> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="11793-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11793-105">DESCRIPTION</span></span>
<span data-ttu-id="11793-106">Das Cmdlet " **Satz-AzureRoute** " erstellt eine Route in einer Route-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="11793-106">The **Set-AzureRoute** cmdlet creates a route in a route table.</span></span>
<span data-ttu-id="11793-107">Die neue Route wird fast sofort auf den virtuellen Computern wirksam, die der Route-Tabelle zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="11793-107">The new route takes effect almost immediately on the virtual machines that are associated with the route table.</span></span>

## <span data-ttu-id="11793-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="11793-108">EXAMPLES</span></span>

### <span data-ttu-id="11793-109">Beispiel 1: Hinzufügen einer virtuellen Appliance-Route für den nächsten Hop</span><span class="sxs-lookup"><span data-stu-id="11793-109">Example 1: Add a virtual appliance next hop route</span></span>
```
PS C:\> New-AzureRouteTable -Name "ApplianceRouteTable" -Location "Central US" -Label "Appliance Route Table" | Set-AzureRoute -RouteName "ApplianceRoute03" -AddressPrefix "10.0.0.0/24" -NextHopType VirtualAppliance -NextHopIpAddress "10.0.1.5"

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    AppRT                         Central US                    Appliance Route Table
```

<span data-ttu-id="11793-110">Dieser Befehl erstellt eine Routentabelle mit dem Namen ApplianceRouteTable an der angegebenen Position.</span><span class="sxs-lookup"><span data-stu-id="11793-110">This command creates a route table named ApplianceRouteTable in the specified location.</span></span>
<span data-ttu-id="11793-111">Der Befehl übergibt diese Routingtabelle an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11793-111">The command passes that route table to the current cmdlet.</span></span>
<span data-ttu-id="11793-112">Das aktuelle Cmdlet fügt eine Route mit dem Namen "ApplianceRoute03" hinzu, bei der es sich um einen VirtualAppliance nächsten Hop-Typ handelt.</span><span class="sxs-lookup"><span data-stu-id="11793-112">The current cmdlet adds a route named ApplianceRoute03, which is a VirtualAppliance next hop type.</span></span>
<span data-ttu-id="11793-113">Der Befehl gibt die IP-Adresse des nächsten Hop und das Adresspräfix für die Route an.</span><span class="sxs-lookup"><span data-stu-id="11793-113">The command specifies the next hop IP address and the address prefix for the route.</span></span>

### <span data-ttu-id="11793-114">Beispiel 2: Hinzufügen einer Internet Route für den nächsten Hop</span><span class="sxs-lookup"><span data-stu-id="11793-114">Example 2: Add an Internet next hop route</span></span>
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" | Set-AzureRoute -RouteName "InternetRoute" -AddressPrefix "0.0.0.0/0" -NextHopType Internet

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute, internetroute}     AppRT                         Central US                    Appliance Route Table
```

<span data-ttu-id="11793-115">Dieser Befehl ruft eine Routentabelle mit dem Namen ApplianceRouteTable ab.</span><span class="sxs-lookup"><span data-stu-id="11793-115">This command gets a route table named ApplianceRouteTable.</span></span>
<span data-ttu-id="11793-116">Der Befehl übergibt diese Routingtabelle an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11793-116">The command passes that route table to the current cmdlet.</span></span>
<span data-ttu-id="11793-117">Das aktuelle Cmdlet fügt eine Route mit dem Namen "InternetRoute" hinzu, die ein Internet-nächster Hop-Typ ist.</span><span class="sxs-lookup"><span data-stu-id="11793-117">The current cmdlet adds a route named InternetRoute, which is an Internet next hop type.</span></span>
<span data-ttu-id="11793-118">Der Befehl gibt das Adresspräfix für die Route an.</span><span class="sxs-lookup"><span data-stu-id="11793-118">The command specifies the address prefix for the route.</span></span>

## <span data-ttu-id="11793-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="11793-119">PARAMETERS</span></span>

### <span data-ttu-id="11793-120">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="11793-120">-AddressPrefix</span></span>
<span data-ttu-id="11793-121">Gibt ein Adresspräfix für die neue Route an.</span><span class="sxs-lookup"><span data-stu-id="11793-121">Specifies an address prefix for the new route.</span></span>

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

### <span data-ttu-id="11793-122">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="11793-122">-NextHopIpAddress</span></span>
<span data-ttu-id="11793-123">Gibt die IP-Adresse der Appliance an, bei der es sich um den nächsten Hop für Datenverkehr handelt, der diese Route verwendet.</span><span class="sxs-lookup"><span data-stu-id="11793-123">Specifies the IP address of the appliance that is the next hop for traffic that uses this route.</span></span>
<span data-ttu-id="11793-124">Geben Sie diesen Wert nur an, wenn Sie einen Wert von VirtualAppliance für den *NextHopType* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="11793-124">Specify this value only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11793-125">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="11793-125">-NextHopType</span></span>
<span data-ttu-id="11793-126">Gibt den Typ des nächsten Hop für Datenverkehr an, der diese Route verwendet.</span><span class="sxs-lookup"><span data-stu-id="11793-126">Specifies the next hop type for traffic that uses this route.</span></span>
<span data-ttu-id="11793-127">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="11793-127">Valid values are:</span></span> 

- <span data-ttu-id="11793-128">VPNGateway</span><span class="sxs-lookup"><span data-stu-id="11793-128">VPNGateway</span></span>
- <span data-ttu-id="11793-129">VNETLocal</span><span class="sxs-lookup"><span data-stu-id="11793-129">VNETLocal</span></span>
- <span data-ttu-id="11793-130">Internet</span><span class="sxs-lookup"><span data-stu-id="11793-130">Internet</span></span>
- <span data-ttu-id="11793-131">VirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="11793-131">VirtualAppliance</span></span>
- <span data-ttu-id="11793-132">NULL</span><span class="sxs-lookup"><span data-stu-id="11793-132">Null</span></span>

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

### <span data-ttu-id="11793-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="11793-133">-Profile</span></span>
<span data-ttu-id="11793-134">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="11793-134">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="11793-135">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="11793-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="11793-136">-Routename</span><span class="sxs-lookup"><span data-stu-id="11793-136">-RouteName</span></span>
<span data-ttu-id="11793-137">Gibt einen Namen für die neue Route an, die von diesem Cmdlet hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="11793-137">Specifies a name for the new route that this cmdlet adds.</span></span>

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

### <span data-ttu-id="11793-138">-Routel</span><span class="sxs-lookup"><span data-stu-id="11793-138">-RouteTable</span></span>
<span data-ttu-id="11793-139">Gibt die Routingtabelle an, der das Cmdlet die neue Route hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="11793-139">Specifies the route table to which this cmdlet adds the new route.</span></span>

```yaml
Type: IRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11793-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11793-140">CommonParameters</span></span>
<span data-ttu-id="11793-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11793-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11793-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11793-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11793-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="11793-143">INPUTS</span></span>

## <span data-ttu-id="11793-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="11793-144">OUTPUTS</span></span>

## <span data-ttu-id="11793-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="11793-145">NOTES</span></span>

## <span data-ttu-id="11793-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="11793-146">RELATED LINKS</span></span>

[<span data-ttu-id="11793-147">Remove-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="11793-147">Remove-AzureRoute</span></span>](./Remove-AzureRoute.md)


