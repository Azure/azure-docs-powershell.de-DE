---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 320588b81791c033b94a07261f769fa0886d2f2c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841196"
---
# <span data-ttu-id="bc216-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bc216-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="bc216-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bc216-102">SYNOPSIS</span></span>
<span data-ttu-id="bc216-103">Entfernt einen Integritäts Prüf Punkt aus einem vorhandenen Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="bc216-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="bc216-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc216-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc216-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bc216-105">DESCRIPTION</span></span>
<span data-ttu-id="bc216-106">Das Remove-AzApplicationGatewayProbeConfig-Cmdlet entfernt eine Heath-Sonde aus einem vorhandenen Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="bc216-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="bc216-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bc216-107">EXAMPLES</span></span>

### <span data-ttu-id="bc216-108">Beispiel 1: Entfernen einer Integritätsprüfung von einem vorhandenen Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="bc216-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="bc216-109">Mit diesem Befehl wird der Integritätstest mit dem Namen Probe04 aus dem Application Gateway mit dem Namen Gateway entfernt.</span><span class="sxs-lookup"><span data-stu-id="bc216-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="bc216-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc216-110">PARAMETERS</span></span>

### <span data-ttu-id="bc216-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bc216-111">-ApplicationGateway</span></span>
<span data-ttu-id="bc216-112">Gibt das Anwendungsgateway an, für das dieses Cmdlet einen Prüfpunkt entfernt.</span><span class="sxs-lookup"><span data-stu-id="bc216-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc216-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc216-113">-DefaultProfile</span></span>
<span data-ttu-id="bc216-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bc216-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc216-115">-Name</span><span class="sxs-lookup"><span data-stu-id="bc216-115">-Name</span></span>
<span data-ttu-id="bc216-116">Gibt den Namen des Prüfpunkts an, für den dieses Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="bc216-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="bc216-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc216-117">CommonParameters</span></span>
<span data-ttu-id="bc216-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc216-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc216-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc216-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc216-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bc216-120">INPUTS</span></span>

### <span data-ttu-id="bc216-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bc216-121">PSApplicationGateway</span></span>
<span data-ttu-id="bc216-122">Der Parameter "ApplicationGateway" akzeptiert den Wert vom Typ "PSApplicationGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="bc216-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="bc216-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bc216-123">OUTPUTS</span></span>

### <span data-ttu-id="bc216-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bc216-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bc216-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="bc216-125">NOTES</span></span>

## <span data-ttu-id="bc216-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bc216-126">RELATED LINKS</span></span>

[<span data-ttu-id="bc216-127">Entfernen eines Prüfpunkts aus einem vorhandenen Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="bc216-127">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="bc216-128">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bc216-128">Add-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="bc216-129">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bc216-129">Get-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="bc216-130">Neu – AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bc216-130">New-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="bc216-131">Satz-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bc216-131">Set-AzApplicationGatewayProbeConfig</span></span>]()

