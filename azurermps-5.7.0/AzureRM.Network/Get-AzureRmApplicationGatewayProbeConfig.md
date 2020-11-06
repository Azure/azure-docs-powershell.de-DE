---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: d8086718ef9d4b009bc785a3017c38e8d29047c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496446"
---
# <span data-ttu-id="de4cd-101">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="de4cd-101">Get-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="de4cd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="de4cd-102">SYNOPSIS</span></span>
<span data-ttu-id="de4cd-103">Ruft eine vorhandene Integritäts Prüf Punkt Konfiguration von einem Anwendungs Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="de4cd-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de4cd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="de4cd-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de4cd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="de4cd-105">DESCRIPTION</span></span>
<span data-ttu-id="de4cd-106">Das Get-AzureRmApplicationGatewayProbeConfig-Cmdlet ruft eine vorhandene Integritäts Prüf Punkt Konfiguration von einem Anwendungs Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="de4cd-106">The Get-AzureRmApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="de4cd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="de4cd-107">EXAMPLES</span></span>

### <span data-ttu-id="de4cd-108">Beispiel 1: Abrufen einer vorhandenen Sonde von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="de4cd-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="de4cd-109">Dieser Befehl ruft den Integritätstest mit dem Namen "Probe02" aus dem Application Gateway mit dem Namen Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="de4cd-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="de4cd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="de4cd-110">PARAMETERS</span></span>

### <span data-ttu-id="de4cd-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="de4cd-111">-ApplicationGateway</span></span>
<span data-ttu-id="de4cd-112">Gibt das Anwendungsgateway an, für das dieses Cmdlet eine Prüf Punkt Konfiguration erhält.</span><span class="sxs-lookup"><span data-stu-id="de4cd-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="de4cd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de4cd-113">-DefaultProfile</span></span>
<span data-ttu-id="de4cd-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="de4cd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de4cd-115">-Name</span><span class="sxs-lookup"><span data-stu-id="de4cd-115">-Name</span></span>
<span data-ttu-id="de4cd-116">Gibt den Namen des Prüfpunkts an.</span><span class="sxs-lookup"><span data-stu-id="de4cd-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="de4cd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de4cd-117">CommonParameters</span></span>
<span data-ttu-id="de4cd-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de4cd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de4cd-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de4cd-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de4cd-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="de4cd-120">INPUTS</span></span>

### <span data-ttu-id="de4cd-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="de4cd-121">PSApplicationGateway</span></span>
<span data-ttu-id="de4cd-122">Der Parameter "ApplicationGateway" akzeptiert den Wert vom Typ "PSApplicationGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="de4cd-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="de4cd-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="de4cd-123">OUTPUTS</span></span>

### <span data-ttu-id="de4cd-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="de4cd-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

### <span data-ttu-id="de4cd-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe]</span><span class="sxs-lookup"><span data-stu-id="de4cd-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]</span></span>

## <span data-ttu-id="de4cd-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="de4cd-126">NOTES</span></span>

## <span data-ttu-id="de4cd-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="de4cd-127">RELATED LINKS</span></span>

[<span data-ttu-id="de4cd-128">Hinzufügen einer Sonde zu einem vorhandenen Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="de4cd-128">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="de4cd-129">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="de4cd-129">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="de4cd-130">Neu – AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="de4cd-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="de4cd-131">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="de4cd-131">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="de4cd-132">Satz-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="de4cd-132">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

