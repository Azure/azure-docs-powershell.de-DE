---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A439ADC4-991E-4860-82AA-7BED315991B9
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9f28659835fef4778eac729ccd020eb82f563bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006546"
---
# <span data-ttu-id="79f7e-101">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79f7e-101">Get-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="79f7e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="79f7e-102">SYNOPSIS</span></span>
<span data-ttu-id="79f7e-103">Ruft die Details der Konfiguration des internen Lastenausgleichsmoduls ab.</span><span class="sxs-lookup"><span data-stu-id="79f7e-103">Gets the details of the internal load balancer configuration.</span></span>

## <span data-ttu-id="79f7e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="79f7e-104">SYNTAX</span></span>

```
Get-AzureInternalLoadBalancer [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="79f7e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="79f7e-105">DESCRIPTION</span></span>
<span data-ttu-id="79f7e-106">Das Cmdlet " **Get-AzureInternalLoadBalancer** " Ruft die Details der internen Load Balancer-Konfiguration für einen Azure-Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="79f7e-106">The **Get-AzureInternalLoadBalancer** cmdlet gets the details of the internal load balancer configuration for an Azure service.</span></span>

## <span data-ttu-id="79f7e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="79f7e-107">EXAMPLES</span></span>

### <span data-ttu-id="79f7e-108">Beispiel 1: Abrufen von Details für ein internes Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="79f7e-108">Example 1: Get details for an internal load balancer</span></span>
```
PS C:\> Get-AzureService -ServiceName "ContosoService" | Get-AzureInternalLoadBalancer
```

<span data-ttu-id="79f7e-109">Dieser Befehl ruft den Dienst mit dem Namen ContosoService mit dem Cmdlet **Get-AzureService** ab.</span><span class="sxs-lookup"><span data-stu-id="79f7e-109">This command gets the service named ContosoService by using the **Get-AzureService** cmdlet.</span></span>
<span data-ttu-id="79f7e-110">Der Befehl übergibt diesen Dienst mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79f7e-110">The command passes that service to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="79f7e-111">Das aktuelle Cmdlet ruft Details für das interne Lastenausgleichsmodul für diesen Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="79f7e-111">The current cmdlet gets details for the internal load balancer for that service.</span></span>

## <span data-ttu-id="79f7e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="79f7e-112">PARAMETERS</span></span>

### <span data-ttu-id="79f7e-113">-Information</span><span class="sxs-lookup"><span data-stu-id="79f7e-113">-InformationAction</span></span>
<span data-ttu-id="79f7e-114">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="79f7e-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="79f7e-115">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="79f7e-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="79f7e-116">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="79f7e-116">Continue</span></span>
- <span data-ttu-id="79f7e-117">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="79f7e-117">Ignore</span></span>
- <span data-ttu-id="79f7e-118">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="79f7e-118">Inquire</span></span>
- <span data-ttu-id="79f7e-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="79f7e-119">SilentlyContinue</span></span>
- <span data-ttu-id="79f7e-120">Beenden</span><span class="sxs-lookup"><span data-stu-id="79f7e-120">Stop</span></span>
- <span data-ttu-id="79f7e-121">Anhalten</span><span class="sxs-lookup"><span data-stu-id="79f7e-121">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79f7e-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="79f7e-122">-InformationVariable</span></span>
<span data-ttu-id="79f7e-123">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="79f7e-123">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79f7e-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="79f7e-124">-Profile</span></span>
<span data-ttu-id="79f7e-125">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="79f7e-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="79f7e-126">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="79f7e-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="79f7e-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="79f7e-127">-ServiceName</span></span>
<span data-ttu-id="79f7e-128">Gibt den Namen des Diensts an, für den dieses Cmdlet Details für ein internes Lastenausgleichsmodul erhält.</span><span class="sxs-lookup"><span data-stu-id="79f7e-128">Specifies the name of the service for which this cmdlet gets details for an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79f7e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79f7e-129">CommonParameters</span></span>
<span data-ttu-id="79f7e-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79f7e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79f7e-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79f7e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79f7e-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="79f7e-132">INPUTS</span></span>

## <span data-ttu-id="79f7e-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="79f7e-133">OUTPUTS</span></span>

### <span data-ttu-id="79f7e-134">Microsoft. WindowsAzure. Commands. Servicemanagement. Model. InternalLoadBalancerContext</span><span class="sxs-lookup"><span data-stu-id="79f7e-134">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.InternalLoadBalancerContext</span></span>

## <span data-ttu-id="79f7e-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="79f7e-135">NOTES</span></span>

## <span data-ttu-id="79f7e-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="79f7e-136">RELATED LINKS</span></span>

[<span data-ttu-id="79f7e-137">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79f7e-137">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="79f7e-138">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="79f7e-138">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="79f7e-139">Neu – AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="79f7e-139">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="79f7e-140">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79f7e-140">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)

[<span data-ttu-id="79f7e-141">Satz-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79f7e-141">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


