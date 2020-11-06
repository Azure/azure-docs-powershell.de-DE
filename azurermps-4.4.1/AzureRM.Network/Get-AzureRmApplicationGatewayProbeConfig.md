---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 6583856eb6d44fa170b53a855e43db71602534a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479098"
---
# <span data-ttu-id="9fac6-101">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9fac6-101">Get-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="9fac6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9fac6-102">SYNOPSIS</span></span>
<span data-ttu-id="9fac6-103">Ruft eine vorhandene Integritäts Prüf Punkt Konfiguration von einem Anwendungs Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="9fac6-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fac6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9fac6-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fac6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9fac6-105">DESCRIPTION</span></span>
<span data-ttu-id="9fac6-106">Das Get-AzureRmApplicationGatewayProbeConfig-Cmdlet ruft eine vorhandene Integritäts Prüf Punkt Konfiguration von einem Anwendungs Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="9fac6-106">The Get-AzureRmApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="9fac6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9fac6-107">EXAMPLES</span></span>

### <span data-ttu-id="9fac6-108">Beispiel 1: Abrufen einer vorhandenen Sonde von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="9fac6-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="9fac6-109">Dieser Befehl ruft den Integritätstest mit dem Namen "Probe02" aus dem Application Gateway mit dem Namen Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="9fac6-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="9fac6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9fac6-110">PARAMETERS</span></span>

### <span data-ttu-id="9fac6-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9fac6-111">-ApplicationGateway</span></span>
<span data-ttu-id="9fac6-112">Gibt das Anwendungsgateway an, für das dieses Cmdlet eine Prüf Punkt Konfiguration erhält.</span><span class="sxs-lookup"><span data-stu-id="9fac6-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fac6-113">-Name</span><span class="sxs-lookup"><span data-stu-id="9fac6-113">-Name</span></span>
<span data-ttu-id="9fac6-114">Gibt den Namen des Prüfpunkts an.</span><span class="sxs-lookup"><span data-stu-id="9fac6-114">Specifies the name of the probe.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fac6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fac6-115">-DefaultProfile</span></span>
<span data-ttu-id="9fac6-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9fac6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fac6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fac6-117">CommonParameters</span></span>
<span data-ttu-id="9fac6-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fac6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fac6-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fac6-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fac6-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9fac6-120">INPUTS</span></span>

### <span data-ttu-id="9fac6-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9fac6-121">PSApplicationGateway</span></span>
<span data-ttu-id="9fac6-122">Der Parameter "ApplicationGateway" akzeptiert den Wert vom Typ "PSApplicationGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="9fac6-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="9fac6-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9fac6-123">OUTPUTS</span></span>

### <span data-ttu-id="9fac6-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="9fac6-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

### <span data-ttu-id="9fac6-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe]</span><span class="sxs-lookup"><span data-stu-id="9fac6-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]</span></span>

## <span data-ttu-id="9fac6-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="9fac6-126">NOTES</span></span>

## <span data-ttu-id="9fac6-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9fac6-127">RELATED LINKS</span></span>

[<span data-ttu-id="9fac6-128">Hinzufügen einer Sonde zu einem vorhandenen Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="9fac6-128">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="9fac6-129">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9fac6-129">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="9fac6-130">Neu – AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9fac6-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="9fac6-131">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9fac6-131">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="9fac6-132">Satz-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9fac6-132">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

