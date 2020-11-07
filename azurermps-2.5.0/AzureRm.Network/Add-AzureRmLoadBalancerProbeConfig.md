---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerprobeconfig
schema: 2.0.0
ms.openlocfilehash: a6fe4515fe6e6df213abb667eb83bccfa9ac6095
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850791"
---
# <span data-ttu-id="c99e6-101">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c99e6-101">Add-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="c99e6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c99e6-102">SYNOPSIS</span></span>
<span data-ttu-id="c99e6-103">Fügt eine Prüf Punkt Konfiguration zu einem Lastenausgleichsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="c99e6-103">Adds a probe configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c99e6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c99e6-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerProbeConfig -Name <String> -LoadBalancer <PSLoadBalancer> [-RequestPath <String>]
 [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c99e6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c99e6-105">DESCRIPTION</span></span>
<span data-ttu-id="c99e6-106">Das Cmdlet **Add-AzureRmLoadBalancerProbeConfig** fügt eine Prüf Punkt Konfiguration zu einem Azure-Lastenausgleichsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="c99e6-106">The **Add-AzureRmLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="c99e6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c99e6-107">EXAMPLES</span></span>

### <span data-ttu-id="c99e6-108">Beispiel 1 Hinzufügen einer Prüf Punkt Konfiguration zu einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="c99e6-108">Example 1 Add a probe configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzureRmLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzureRmLoadBalancer
```

<span data-ttu-id="c99e6-109">Dieser Befehl ruft das Lastenausgleichsmodul mit dem Namen myLb ab, fügt die angegebene Prüf Punkt Konfiguration hinzu und verwendet dann das Cmdlet " **Satz-AzureRmLoadBalancer** ", um das Lastenausgleichsmodul zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c99e6-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="c99e6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c99e6-110">PARAMETERS</span></span>

### <span data-ttu-id="c99e6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c99e6-111">-DefaultProfile</span></span>
<span data-ttu-id="c99e6-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c99e6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c99e6-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="c99e6-113">-IntervalInSeconds</span></span>
<span data-ttu-id="c99e6-114">Gibt das Intervall in Sekunden zwischen Prüfpunkten für jede Instanz des Lastenausgleichsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="c99e6-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c99e6-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c99e6-115">-LoadBalancer</span></span>
<span data-ttu-id="c99e6-116">Gibt ein **LoadBalancer** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="c99e6-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="c99e6-117">Dieses Cmdlet fügt dem Load Balancer eine Prüf Punkt Konfiguration hinzu, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="c99e6-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c99e6-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c99e6-118">-Name</span></span>
<span data-ttu-id="c99e6-119">Gibt den Namen der zu hinzuzufügenden Prüf Punkt Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="c99e6-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="c99e6-120">-Port</span><span class="sxs-lookup"><span data-stu-id="c99e6-120">-Port</span></span>
<span data-ttu-id="c99e6-121">Gibt den Port an, an dem die Sonden mit einem Dienst mit Lastenausgleich verbunden werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c99e6-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c99e6-122">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="c99e6-122">-ProbeCount</span></span>
<span data-ttu-id="c99e6-123">Gibt an, wie viele aufeinanderfolgende Fehler pro Instanz auftreten, damit eine Instanz als unschädlich eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="c99e6-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c99e6-124">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="c99e6-124">-Protocol</span></span>
<span data-ttu-id="c99e6-125">Gibt das für den Prüfpunkt zu verwendende Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="c99e6-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="c99e6-126">Die zulässigen Werte für diesen Parameter lauten: TCP oder http.</span><span class="sxs-lookup"><span data-stu-id="c99e6-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c99e6-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="c99e6-127">-RequestPath</span></span>
<span data-ttu-id="c99e6-128">Gibt den Pfad im Lastenausgleichsdienst an, der zum Ermitteln der Integrität überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="c99e6-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="c99e6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c99e6-129">CommonParameters</span></span>
<span data-ttu-id="c99e6-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c99e6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c99e6-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c99e6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c99e6-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c99e6-132">INPUTS</span></span>

### <span data-ttu-id="c99e6-133">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c99e6-133">PSLoadBalancer</span></span>
<span data-ttu-id="c99e6-134">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c99e6-134">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="c99e6-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c99e6-135">OUTPUTS</span></span>

### <span data-ttu-id="c99e6-136">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c99e6-136">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c99e6-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="c99e6-137">NOTES</span></span>

## <span data-ttu-id="c99e6-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c99e6-138">RELATED LINKS</span></span>

[<span data-ttu-id="c99e6-139">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c99e6-139">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="c99e6-140">Neu – AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c99e6-140">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="c99e6-141">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c99e6-141">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="c99e6-142">Satz-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c99e6-142">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="c99e6-143">Satz-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c99e6-143">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


