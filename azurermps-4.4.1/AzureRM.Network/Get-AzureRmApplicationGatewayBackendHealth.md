---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D5E928C3-26B6-4B7C-8A9C-F1F602BABF75
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHealth.md
ms.openlocfilehash: d3f5114243828623ba6c55e9694cc4250ae12657
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479113"
---
# <span data-ttu-id="29761-101">Get-AzureRmApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="29761-101">Get-AzureRmApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="29761-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="29761-102">SYNOPSIS</span></span>
<span data-ttu-id="29761-103">Ruft den Back-End-Zustand des Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="29761-103">Gets application gateway backend health.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29761-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="29761-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendHealth -Name <String> -ResourceGroupName <String>
 [-ExpandResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29761-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29761-105">DESCRIPTION</span></span>
<span data-ttu-id="29761-106">Das Get-AzureRmApplicationGatewayBackendHealth-Cmdlet ruft das Back-End-Zustand des Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="29761-106">The Get-AzureRmApplicationGatewayBackendHealth cmdlet gets application gateway backend health.</span></span>

## <span data-ttu-id="29761-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="29761-107">EXAMPLES</span></span>

### <span data-ttu-id="29761-108">--------------------------Beispiel 1: Ruft die Back-End-Integrität ohne erweiterte Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="29761-108">--------------------------  Example 1: Gets backend health without expanded resources.</span></span>  --------------------------
<span data-ttu-id="29761-109">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="29761-109">@{paragraph=PS C:\\\>}</span></span>



















```
PS C:\>$BackendHealth = Get-AzureRmApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="29761-110">Dieser Befehl ruft die Back-End-Integrität des Anwendungs Gateways mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $BackendHealth-Variablen.</span><span class="sxs-lookup"><span data-stu-id="29761-110">This command gets the backend health of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

### <span data-ttu-id="29761-111">--------------------------Beispiel 1: Ruft die Back-End-Integrität mit erweiterten Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="29761-111">--------------------------  Example 1: Gets backend health with expanded resources.</span></span>  --------------------------
<span data-ttu-id="29761-112">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="29761-112">@{paragraph=PS C:\\\>}</span></span>



















```
PS C:\>$BackendHealth = Get-AzureRmApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01 -ExpandResource "backendhealth/applicationgatewayresource"
```

<span data-ttu-id="29761-113">Dieser Befehl ruft den Back-End-Status (mit erweiterten Ressourcen) des Anwendungs Gateways mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $BackendHealth-Variablen.</span><span class="sxs-lookup"><span data-stu-id="29761-113">This command gets the backend health (with expanded resources) of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

## <span data-ttu-id="29761-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="29761-114">PARAMETERS</span></span>

### <span data-ttu-id="29761-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="29761-115">-ExpandResource</span></span>
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

### <span data-ttu-id="29761-116">-Name</span><span class="sxs-lookup"><span data-stu-id="29761-116">-Name</span></span>
<span data-ttu-id="29761-117">Gibt den Namen des Anwendungs Gateways an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="29761-117">Specifies the name of the application gateway that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29761-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29761-118">-ResourceGroupName</span></span>
<span data-ttu-id="29761-119">Gibt den Namen der Ressourcengruppe an, die das Anwendungsgateway enthält.</span><span class="sxs-lookup"><span data-stu-id="29761-119">Specifies the name of the resource group that contains the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29761-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29761-120">-DefaultProfile</span></span>
<span data-ttu-id="29761-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="29761-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29761-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29761-122">CommonParameters</span></span>
<span data-ttu-id="29761-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29761-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29761-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29761-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29761-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="29761-125">INPUTS</span></span>

### <span data-ttu-id="29761-126">System. String</span><span class="sxs-lookup"><span data-stu-id="29761-126">System.String</span></span>

## <span data-ttu-id="29761-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="29761-127">OUTPUTS</span></span>

### <span data-ttu-id="29761-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="29761-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="29761-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="29761-129">NOTES</span></span>
<span data-ttu-id="29761-130">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="29761-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="29761-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="29761-131">RELATED LINKS</span></span>

[<span data-ttu-id="29761-132">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="29761-132">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

