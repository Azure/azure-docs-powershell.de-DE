---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: b3e2b3ea03ca0bae0db1bea1606e4ae6b94a597e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841723"
---
# <span data-ttu-id="0b80e-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0b80e-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="0b80e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0b80e-102">SYNOPSIS</span></span>
<span data-ttu-id="0b80e-103">Ruft eine vorhandene Integritäts Prüf Punkt Konfiguration von einem Anwendungs Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="0b80e-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="0b80e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b80e-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b80e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b80e-105">DESCRIPTION</span></span>
<span data-ttu-id="0b80e-106">Das Get-AzApplicationGatewayProbeConfig-Cmdlet ruft eine vorhandene Integritäts Prüf Punkt Konfiguration von einem Anwendungs Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="0b80e-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="0b80e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b80e-107">EXAMPLES</span></span>

### <span data-ttu-id="0b80e-108">Beispiel 1: Abrufen einer vorhandenen Sonde von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="0b80e-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="0b80e-109">Dieser Befehl ruft den Integritätstest mit dem Namen "Probe02" aus dem Application Gateway mit dem Namen Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="0b80e-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="0b80e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b80e-110">PARAMETERS</span></span>

### <span data-ttu-id="0b80e-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0b80e-111">-ApplicationGateway</span></span>
<span data-ttu-id="0b80e-112">Gibt das Anwendungsgateway an, für das dieses Cmdlet eine Prüf Punkt Konfiguration erhält.</span><span class="sxs-lookup"><span data-stu-id="0b80e-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="0b80e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b80e-113">-DefaultProfile</span></span>
<span data-ttu-id="0b80e-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0b80e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b80e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0b80e-115">-Name</span></span>
<span data-ttu-id="0b80e-116">Gibt den Namen des Prüfpunkts an.</span><span class="sxs-lookup"><span data-stu-id="0b80e-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="0b80e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b80e-117">CommonParameters</span></span>
<span data-ttu-id="0b80e-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b80e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b80e-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b80e-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b80e-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0b80e-120">INPUTS</span></span>

### <span data-ttu-id="0b80e-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0b80e-121">PSApplicationGateway</span></span>
<span data-ttu-id="0b80e-122">Der Parameter "ApplicationGateway" akzeptiert den Wert vom Typ "PSApplicationGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0b80e-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="0b80e-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0b80e-123">OUTPUTS</span></span>

### <span data-ttu-id="0b80e-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="0b80e-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

### <span data-ttu-id="0b80e-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe]</span><span class="sxs-lookup"><span data-stu-id="0b80e-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]</span></span>

## <span data-ttu-id="0b80e-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="0b80e-126">NOTES</span></span>

## <span data-ttu-id="0b80e-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0b80e-127">RELATED LINKS</span></span>

[<span data-ttu-id="0b80e-128">Hinzufügen einer Sonde zu einem vorhandenen Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="0b80e-128">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="0b80e-129">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0b80e-129">Add-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="0b80e-130">Neu – AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0b80e-130">New-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="0b80e-131">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0b80e-131">Remove-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="0b80e-132">Satz-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0b80e-132">Set-AzApplicationGatewayProbeConfig</span></span>]()

