---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayprobeconfig
schema: 2.0.0
ms.openlocfilehash: cbe38933cb4c2c75b5219bf0deccc0b28052a61f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849216"
---
# <span data-ttu-id="cb7c1-101">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cb7c1-101">Get-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="cb7c1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cb7c1-102">SYNOPSIS</span></span>
<span data-ttu-id="cb7c1-103">Ruft eine vorhandene Integritäts Prüf Punkt Konfiguration von einem Anwendungs Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="cb7c1-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb7c1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb7c1-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb7c1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cb7c1-105">DESCRIPTION</span></span>
<span data-ttu-id="cb7c1-106">Das Get-AzureRmApplicationGatewayProbeConfig-Cmdlet ruft eine vorhandene Integritäts Prüf Punkt Konfiguration von einem Anwendungs Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="cb7c1-106">The Get-AzureRmApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="cb7c1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cb7c1-107">EXAMPLES</span></span>

### <span data-ttu-id="cb7c1-108">Beispiel 1: Abrufen einer vorhandenen Sonde von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="cb7c1-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="cb7c1-109">Dieser Befehl ruft den Integritätstest mit dem Namen "Probe02" aus dem Application Gateway mit dem Namen Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="cb7c1-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="cb7c1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb7c1-110">PARAMETERS</span></span>

### <span data-ttu-id="cb7c1-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb7c1-111">-ApplicationGateway</span></span>
<span data-ttu-id="cb7c1-112">Gibt das Anwendungsgateway an, für das dieses Cmdlet eine Prüf Punkt Konfiguration erhält.</span><span class="sxs-lookup"><span data-stu-id="cb7c1-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="cb7c1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb7c1-113">-DefaultProfile</span></span>
<span data-ttu-id="cb7c1-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cb7c1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb7c1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="cb7c1-115">-Name</span></span>
<span data-ttu-id="cb7c1-116">Gibt den Namen des Prüfpunkts an.</span><span class="sxs-lookup"><span data-stu-id="cb7c1-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="cb7c1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb7c1-117">CommonParameters</span></span>
<span data-ttu-id="cb7c1-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb7c1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb7c1-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb7c1-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb7c1-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cb7c1-120">INPUTS</span></span>

### <span data-ttu-id="cb7c1-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb7c1-121">PSApplicationGateway</span></span>
<span data-ttu-id="cb7c1-122">Der Parameter "ApplicationGateway" akzeptiert den Wert vom Typ "PSApplicationGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="cb7c1-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="cb7c1-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cb7c1-123">OUTPUTS</span></span>

### <span data-ttu-id="cb7c1-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="cb7c1-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

### <span data-ttu-id="cb7c1-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe]</span><span class="sxs-lookup"><span data-stu-id="cb7c1-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]</span></span>

## <span data-ttu-id="cb7c1-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="cb7c1-126">NOTES</span></span>

## <span data-ttu-id="cb7c1-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cb7c1-127">RELATED LINKS</span></span>

[<span data-ttu-id="cb7c1-128">Hinzufügen einer Sonde zu einem vorhandenen Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="cb7c1-128">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="cb7c1-129">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cb7c1-129">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="cb7c1-130">Neu – AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cb7c1-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="cb7c1-131">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cb7c1-131">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="cb7c1-132">Satz-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cb7c1-132">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

