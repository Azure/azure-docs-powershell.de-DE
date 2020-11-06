---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 3aed1a20a8a5878819ea3634ff5d31babba3261c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496445"
---
# <span data-ttu-id="94f5a-101">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="94f5a-101">Get-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="94f5a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="94f5a-102">SYNOPSIS</span></span>
<span data-ttu-id="94f5a-103">Ruft Informationen zu Express Route-Schaltkreis Berechtigungen ab.</span><span class="sxs-lookup"><span data-stu-id="94f5a-103">Gets information about ExpressRoute circuit authorizations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94f5a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="94f5a-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94f5a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="94f5a-105">DESCRIPTION</span></span>
<span data-ttu-id="94f5a-106">Das Cmdlet " **Get-AzureRmExpressRouteCircuitAuthorization** " Ruft Informationen zu den Berechtigungen ab, die einem Express Route-Schaltkreis zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="94f5a-106">The **Get-AzureRmExpressRouteCircuitAuthorization** cmdlet gets information about the authorizations assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="94f5a-107">Express Route-Schaltkreise verbinden Ihr lokales Netzwerk mit der Microsoft-Cloud, indem Sie einen Verbindungsanbieter anstelle des öffentlichen Internets verwenden.</span><span class="sxs-lookup"><span data-stu-id="94f5a-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="94f5a-108">Der Besitzer eines Express Route-Schaltkreises kann bis zu 10 Berechtigungen für jeden Schaltkreis erstellen. Diese Berechtigungen generieren einen Autorisierungsschlüssel, der von einem virtuellen Netzwerk Besitzer verwendet werden kann, um sein Netzwerk mit dem Schaltkreis (eine Autorisierung pro virtuelles Netzwerk) zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="94f5a-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="94f5a-109">Autorisierungsschlüssel sowie weitere Informationen zur Autorisierung können jederzeit angezeigt werden, indem **Sie Get-AzureRmExpressRouteCircuitAuthorization** ausführen.</span><span class="sxs-lookup"><span data-stu-id="94f5a-109">Authorization keys, as well as other information about the authorization, can be viewed at any time by running **Get-AzureRmExpressRouteCircuitAuthorization**.</span></span>

## <span data-ttu-id="94f5a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="94f5a-110">EXAMPLES</span></span>

### <span data-ttu-id="94f5a-111">Beispiel 1: Abrufen aller Express Route-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="94f5a-111">Example 1: Get all ExpressRoute authorizations</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit
```

<span data-ttu-id="94f5a-112">Diese Befehle geben Informationen zu allen Express Route-Berechtigungen zurück, die einem Express Route-Schaltkreis zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="94f5a-112">These commands return information about all the ExpressRoute authorizations associated with an ExpressRoute circuit.</span></span> <span data-ttu-id="94f5a-113">Der erste Befehl verwendet das Cmdlet " **Get-AzureRmExpressRouteCircuit** ", um einen Objektverweis auf einen Schaltkreis mit dem Namen ContosoCircuit zu erstellen. dieser Objektverweis wird in der Variablen $Circuit gespeichert.</span><span class="sxs-lookup"><span data-stu-id="94f5a-113">The first command uses the **Get-AzureRmExpressRouteCircuit** cmdlet to create an object reference a circuit named ContosoCircuit; that object reference is stored in the variable $Circuit.</span></span> <span data-ttu-id="94f5a-114">Der zweite Befehl verwendet dann diesen Objektverweis und das Cmdlet " **Get-AzureRmExpressRouteCircuitAuthorization** ", um Informationen zu den Berechtigungen zurückzugeben, die mit ContosoCircuit verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="94f5a-114">The second command then uses that object reference and the **Get-AzureRmExpressRouteCircuitAuthorization** cmdlet to return information about the authorizations associated with ContosoCircuit.</span></span>

### <span data-ttu-id="94f5a-115">Beispiel 2: Abrufen aller Express Route-Berechtigungen mithilfe des Where-Object-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="94f5a-115">Example 2: Get all ExpressRoute authorizations using the Where-Object cmdlet</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

<span data-ttu-id="94f5a-116">Diese Befehle stellen eine Variation der in Beispiel 1 verwendeten Befehle dar.</span><span class="sxs-lookup"><span data-stu-id="94f5a-116">These commands represent a variation on the commands used in Example 1.</span></span> <span data-ttu-id="94f5a-117">In diesem Fall werden Informationen jedoch nur für diejenigen Berechtigungen zurückgegeben, die für die Verwendung verfügbar sind (also für Berechtigungen, die nicht einem virtuellen Netzwerk zugewiesen wurden).</span><span class="sxs-lookup"><span data-stu-id="94f5a-117">In this case, however, information is returned only for those authorizations that are available for use (that is, for authorizations that have not been assigned to a virtual network).</span></span> <span data-ttu-id="94f5a-118">Zu diesem Zweck werden die Informationen zur Schaltkreis Autorisierung in Befehl 2 zurückgegeben und an das Cmdlet **Where-Object** umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="94f5a-118">To do this, the circuit authorization information is returned in command 2 and is piped to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="94f5a-119">**Where-Object** wählt dann nur die Berechtigungen aus, bei denen die *AuthorizationUseStatus* -Eigenschaft auf available festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="94f5a-119">**Where-Object** then picks out only those authorizations where the *AuthorizationUseStatus* property is set to Available.</span></span> <span data-ttu-id="94f5a-120">Verwenden Sie diese Syntax für die WHERE-Klausel, um nur die nicht verfügbaren Berechtigungen aufzulisten:</span><span class="sxs-lookup"><span data-stu-id="94f5a-120">To list only those authorizations that are not available, use this syntax for the Where clause:</span></span>

`{$_.AuthorizationUseStatus -ne "Available"}`

## <span data-ttu-id="94f5a-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="94f5a-121">PARAMETERS</span></span>

### <span data-ttu-id="94f5a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94f5a-122">-DefaultProfile</span></span>
<span data-ttu-id="94f5a-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="94f5a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94f5a-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="94f5a-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="94f5a-125">Gibt die Express Route-Schaltkreis Autorisierung an.</span><span class="sxs-lookup"><span data-stu-id="94f5a-125">Specifies the ExpressRoute circuit authorization.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94f5a-126">-Name</span><span class="sxs-lookup"><span data-stu-id="94f5a-126">-Name</span></span>
<span data-ttu-id="94f5a-127">Gibt den Namen der Express Route-Schaltkreis Autorisierung an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="94f5a-127">Specifies the name of the ExpressRoute circuit authorization that this cmdlet gets.</span></span>

<span data-ttu-id="94f5a-128">-Name "ContosoCircuitAuthorization"</span><span class="sxs-lookup"><span data-stu-id="94f5a-128">-Name "ContosoCircuitAuthorization"</span></span>

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

### <span data-ttu-id="94f5a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94f5a-129">CommonParameters</span></span>
<span data-ttu-id="94f5a-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94f5a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94f5a-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94f5a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94f5a-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="94f5a-132">INPUTS</span></span>

### <span data-ttu-id="94f5a-133">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="94f5a-133">PSExpressRouteCircuit</span></span>
<span data-ttu-id="94f5a-134">**Get-AzureRmExpressRouteCircuitAuthorization** akzeptiert Pipelineinstanzen des **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="94f5a-134">**Get-AzureRmExpressRouteCircuitAuthorization** accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="94f5a-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="94f5a-135">OUTPUTS</span></span>

### <span data-ttu-id="94f5a-136">PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="94f5a-136">PSExpressRouteCircuitAuthorization</span></span>
<span data-ttu-id="94f5a-137">**Get-AzureRmExpressRouteCircuitAuthorization** gibt Instanzen des **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization** -Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="94f5a-137">**Get-AzureRmExpressRouteCircuitAuthorization** returns instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization** object.</span></span>

## <span data-ttu-id="94f5a-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="94f5a-138">NOTES</span></span>

## <span data-ttu-id="94f5a-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="94f5a-139">RELATED LINKS</span></span>

[<span data-ttu-id="94f5a-140">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="94f5a-140">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="94f5a-141">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="94f5a-141">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="94f5a-142">Neu – AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="94f5a-142">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="94f5a-143">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="94f5a-143">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)
