---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 62ed11a2819a2b0c31756c90ce4ab623a1feae91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502034"
---
# <span data-ttu-id="ece99-101">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ece99-101">Add-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="ece99-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ece99-102">SYNOPSIS</span></span>
<span data-ttu-id="ece99-103">Fügt eine Prüf Punkt Konfiguration zu einem Lastenausgleichsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="ece99-103">Adds a probe configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ece99-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ece99-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ece99-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ece99-105">DESCRIPTION</span></span>
<span data-ttu-id="ece99-106">Das Cmdlet **Add-AzureRmLoadBalancerProbeConfig** fügt eine Prüf Punkt Konfiguration zu einem Azure-Lastenausgleichsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="ece99-106">The **Add-AzureRmLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="ece99-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ece99-107">EXAMPLES</span></span>

### <span data-ttu-id="ece99-108">Beispiel 1 Hinzufügen einer Prüf Punkt Konfiguration zu einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="ece99-108">Example 1 Add a probe configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzureRmLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzureRmLoadBalancer
```

<span data-ttu-id="ece99-109">Dieser Befehl ruft das Lastenausgleichsmodul mit dem Namen myLb ab, fügt die angegebene Prüf Punkt Konfiguration hinzu und verwendet dann das Cmdlet " **Satz-AzureRmLoadBalancer** ", um das Lastenausgleichsmodul zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ece99-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="ece99-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ece99-110">PARAMETERS</span></span>

### <span data-ttu-id="ece99-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ece99-111">-DefaultProfile</span></span>
<span data-ttu-id="ece99-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ece99-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ece99-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="ece99-113">-IntervalInSeconds</span></span>
<span data-ttu-id="ece99-114">Gibt das Intervall in Sekunden zwischen Prüfpunkten für jede Instanz des Lastenausgleichsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="ece99-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ece99-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ece99-115">-LoadBalancer</span></span>
<span data-ttu-id="ece99-116">Gibt ein **LoadBalancer** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="ece99-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="ece99-117">Dieses Cmdlet fügt dem Load Balancer eine Prüf Punkt Konfiguration hinzu, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ece99-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ece99-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ece99-118">-Name</span></span>
<span data-ttu-id="ece99-119">Gibt den Namen der zu hinzuzufügenden Prüf Punkt Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="ece99-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="ece99-120">-Port</span><span class="sxs-lookup"><span data-stu-id="ece99-120">-Port</span></span>
<span data-ttu-id="ece99-121">Gibt den Port an, an dem die Sonden mit einem Dienst mit Lastenausgleich verbunden werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ece99-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ece99-122">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="ece99-122">-ProbeCount</span></span>
<span data-ttu-id="ece99-123">Gibt an, wie viele aufeinanderfolgende Fehler pro Instanz auftreten, damit eine Instanz als unschädlich eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="ece99-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ece99-124">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="ece99-124">-Protocol</span></span>
<span data-ttu-id="ece99-125">Gibt das für den Prüfpunkt zu verwendende Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="ece99-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="ece99-126">Die zulässigen Werte für diesen Parameter lauten: TCP oder http.</span><span class="sxs-lookup"><span data-stu-id="ece99-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ece99-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="ece99-127">-RequestPath</span></span>
<span data-ttu-id="ece99-128">Gibt den Pfad im Lastenausgleichsdienst an, der zum Ermitteln der Integrität überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="ece99-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ece99-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ece99-129">-Confirm</span></span>
<span data-ttu-id="ece99-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ece99-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ece99-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ece99-131">-WhatIf</span></span>
<span data-ttu-id="ece99-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ece99-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ece99-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ece99-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ece99-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ece99-134">CommonParameters</span></span>
<span data-ttu-id="ece99-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ece99-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ece99-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ece99-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ece99-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ece99-137">INPUTS</span></span>

### <span data-ttu-id="ece99-138">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ece99-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="ece99-139">Parameter: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ece99-139">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="ece99-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ece99-140">OUTPUTS</span></span>

### <span data-ttu-id="ece99-141">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ece99-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ece99-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="ece99-142">NOTES</span></span>

## <span data-ttu-id="ece99-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ece99-143">RELATED LINKS</span></span>

[<span data-ttu-id="ece99-144">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ece99-144">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="ece99-145">Neu – AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ece99-145">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="ece99-146">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ece99-146">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="ece99-147">Satz-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ece99-147">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="ece99-148">Satz-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ece99-148">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


