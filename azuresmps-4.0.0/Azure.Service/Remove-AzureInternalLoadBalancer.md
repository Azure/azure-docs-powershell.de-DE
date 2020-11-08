---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3F939FE9-5D42-4EA1-90DC-E6D60158CADE
online version: ''
schema: 2.0.0
ms.openlocfilehash: f2eb6fe50566a5de97f00876bdaa7061bbaf0587
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006681"
---
# <span data-ttu-id="94423-101">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="94423-101">Remove-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="94423-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="94423-102">SYNOPSIS</span></span>
<span data-ttu-id="94423-103">Entfernt eine interne Load Balancer-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="94423-103">Removes an internal load balancer configuration.</span></span>

## <span data-ttu-id="94423-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="94423-104">SYNTAX</span></span>

```
Remove-AzureInternalLoadBalancer [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="94423-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="94423-105">DESCRIPTION</span></span>
<span data-ttu-id="94423-106">Das Cmdlet **Remove-AzureInternalLoadBalancer** entfernt die Konfiguration des internen Lastenausgleichsmoduls aus einem Azure-Dienst.</span><span class="sxs-lookup"><span data-stu-id="94423-106">The **Remove-AzureInternalLoadBalancer** cmdlet removes the internal load balancer configuration from an Azure service.</span></span>
<span data-ttu-id="94423-107">Wenn sich ein Endpunkt derzeit auf das interne Lastenausgleichsmodul bezieht, kann dieses Cmdlet die Konfiguration nicht entfernen.</span><span class="sxs-lookup"><span data-stu-id="94423-107">If any endpoint currently refers to the internal load balancer, this cmdlet cannot remove the configuration.</span></span>

## <span data-ttu-id="94423-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="94423-108">EXAMPLES</span></span>

### <span data-ttu-id="94423-109">Beispiel 1: Entfernen einer internen Load Balancer-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="94423-109">Example 1: Remove an internal load balancer configuration</span></span>
```
PS C:\> Remove-AzureInternalLoadBalancer -ServiceName "ContosoService"
```

<span data-ttu-id="94423-110">Dieser Befehl entfernt die Konfiguration des internen Lastenausgleichs für den Dienst mit dem Namen ContosoService.</span><span class="sxs-lookup"><span data-stu-id="94423-110">This command removes the internal load balancer configuration for the service named ContosoService.</span></span>

## <span data-ttu-id="94423-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="94423-111">PARAMETERS</span></span>

### <span data-ttu-id="94423-112">-Information</span><span class="sxs-lookup"><span data-stu-id="94423-112">-InformationAction</span></span>
<span data-ttu-id="94423-113">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="94423-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="94423-114">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="94423-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="94423-115">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="94423-115">Continue</span></span>
- <span data-ttu-id="94423-116">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="94423-116">Ignore</span></span>
- <span data-ttu-id="94423-117">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="94423-117">Inquire</span></span>
- <span data-ttu-id="94423-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="94423-118">SilentlyContinue</span></span>
- <span data-ttu-id="94423-119">Beenden</span><span class="sxs-lookup"><span data-stu-id="94423-119">Stop</span></span>
- <span data-ttu-id="94423-120">Anhalten</span><span class="sxs-lookup"><span data-stu-id="94423-120">Suspend</span></span>

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

### <span data-ttu-id="94423-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="94423-121">-InformationVariable</span></span>
<span data-ttu-id="94423-122">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="94423-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="94423-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="94423-123">-Profile</span></span>
<span data-ttu-id="94423-124">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="94423-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="94423-125">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="94423-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="94423-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="94423-126">-ServiceName</span></span>
<span data-ttu-id="94423-127">Gibt den Namen des Diensts an, von dem dieses Cmdlet ein internes Lastenausgleichsmodul entfernt.</span><span class="sxs-lookup"><span data-stu-id="94423-127">Specifies the name of the service from which this cmdlet removes an internal load balancer.</span></span>

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

### <span data-ttu-id="94423-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94423-128">CommonParameters</span></span>
<span data-ttu-id="94423-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94423-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94423-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94423-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94423-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="94423-131">INPUTS</span></span>

## <span data-ttu-id="94423-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="94423-132">OUTPUTS</span></span>

### <span data-ttu-id="94423-133">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="94423-133">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="94423-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="94423-134">NOTES</span></span>

## <span data-ttu-id="94423-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="94423-135">RELATED LINKS</span></span>

[<span data-ttu-id="94423-136">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="94423-136">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="94423-137">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="94423-137">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="94423-138">Neu – AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="94423-138">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="94423-139">Satz-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="94423-139">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


