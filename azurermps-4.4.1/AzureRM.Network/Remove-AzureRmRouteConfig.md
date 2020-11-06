---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteConfig.md
ms.openlocfilehash: b64fe52b95fb116b08aade300f622b8ea612dcc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504038"
---
# <span data-ttu-id="dc48a-101">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="dc48a-101">Remove-AzureRmRouteConfig</span></span>

## <span data-ttu-id="dc48a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dc48a-102">SYNOPSIS</span></span>
<span data-ttu-id="dc48a-103">Entfernt eine Route aus einer Route-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="dc48a-103">Removes a route from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc48a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc48a-104">SYNTAX</span></span>

```
Remove-AzureRmRouteConfig -Name <String> -RouteTable <PSRouteTable> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc48a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc48a-105">DESCRIPTION</span></span>
<span data-ttu-id="dc48a-106">Das Cmdlet **Remove-AzureRmRouteConfig** entfernt eine Route aus einer Azure Route-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="dc48a-106">The **Remove-AzureRmRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="dc48a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dc48a-107">EXAMPLES</span></span>

### <span data-ttu-id="dc48a-108">Beispiel 1: Entfernen einer Route</span><span class="sxs-lookup"><span data-stu-id="dc48a-108">Example 1: Remove a route</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Remove-AzureRmRouteConfig -Name "Route02" | Set-AzureRmRouteTable
Name              : RouteTable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"47099b62-60ec-4bc1-b87b-fad56cb8bed1"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"47099b62-60ec-4bc1-b87b-fad56cb8bed1\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="dc48a-109">Dieser Befehl ruft die Routingtabelle mit dem Namen RouteTable01 mit dem Cmdlet **Get-AzureRmRouteTable** ab.</span><span class="sxs-lookup"><span data-stu-id="dc48a-109">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="dc48a-110">Der Befehl übergibt diese Tabelle mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc48a-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="dc48a-111">Das aktuelle Cmdlet entfernt die Route mit dem Namen "Route02" und übergibt das Ergebnis an das Cmdlet " **setAzureRmRouteTable** ", das die Tabelle so aktualisiert, dass die Änderungen wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="dc48a-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="dc48a-112">Die Tabelle enthält nicht mehr die Route mit dem Namen Route02.</span><span class="sxs-lookup"><span data-stu-id="dc48a-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="dc48a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc48a-113">PARAMETERS</span></span>

### <span data-ttu-id="dc48a-114">-Name</span><span class="sxs-lookup"><span data-stu-id="dc48a-114">-Name</span></span>
<span data-ttu-id="dc48a-115">Gibt den Namen der Route an, die dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="dc48a-115">Specifies the name of the route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dc48a-116">-Routel</span><span class="sxs-lookup"><span data-stu-id="dc48a-116">-RouteTable</span></span>
<span data-ttu-id="dc48a-117">Gibt die Route-Tabelle an, die die Route enthält, die dieses Cmdlet löscht.</span><span class="sxs-lookup"><span data-stu-id="dc48a-117">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc48a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc48a-118">-DefaultProfile</span></span>
<span data-ttu-id="dc48a-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dc48a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc48a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc48a-120">CommonParameters</span></span>
<span data-ttu-id="dc48a-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc48a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc48a-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc48a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc48a-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dc48a-123">INPUTS</span></span>

### <span data-ttu-id="dc48a-124">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="dc48a-124">PSRouteTable</span></span>
<span data-ttu-id="dc48a-125">Der Parameter "routeable" akzeptiert den Wert vom Typ "PSRouteTable" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="dc48a-125">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="dc48a-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dc48a-126">OUTPUTS</span></span>

### <span data-ttu-id="dc48a-127">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="dc48a-127">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="dc48a-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="dc48a-128">NOTES</span></span>

## <span data-ttu-id="dc48a-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dc48a-129">RELATED LINKS</span></span>

[<span data-ttu-id="dc48a-130">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="dc48a-130">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="dc48a-131">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="dc48a-131">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="dc48a-132">Neu – AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="dc48a-132">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="dc48a-133">Satz-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="dc48a-133">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


