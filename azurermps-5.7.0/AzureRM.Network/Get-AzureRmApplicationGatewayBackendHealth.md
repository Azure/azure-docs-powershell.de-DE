---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D5E928C3-26B6-4B7C-8A9C-F1F602BABF75
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHealth.md
ms.openlocfilehash: 6e6a2bef9ea6bc237db97139bcc7e9e7a0624fd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478446"
---
# <span data-ttu-id="912f1-101">Get-AzureRmApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="912f1-101">Get-AzureRmApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="912f1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="912f1-102">SYNOPSIS</span></span>
<span data-ttu-id="912f1-103">Ruft den Back-End-Zustand des Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="912f1-103">Gets application gateway backend health.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="912f1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="912f1-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendHealth -Name <String> -ResourceGroupName <String>
 [-ExpandResource <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="912f1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="912f1-105">DESCRIPTION</span></span>
<span data-ttu-id="912f1-106">Das Get-AzureRmApplicationGatewayBackendHealth-Cmdlet ruft das Back-End-Zustand des Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="912f1-106">The Get-AzureRmApplicationGatewayBackendHealth cmdlet gets application gateway backend health.</span></span>

## <span data-ttu-id="912f1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="912f1-107">EXAMPLES</span></span>

### <span data-ttu-id="912f1-108">--------------------------Beispiel 1: Ruft die Back-End-Integrität ohne erweiterte Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="912f1-108">--------------------------  Example 1: Gets backend health without expanded resources.</span></span>  --------------------------
```
PS C:\>$BackendHealth = Get-AzureRmApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="912f1-109">Dieser Befehl ruft die Back-End-Integrität des Anwendungs Gateways mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $BackendHealth-Variablen.</span><span class="sxs-lookup"><span data-stu-id="912f1-109">This command gets the backend health of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

### <span data-ttu-id="912f1-110">--------------------------Beispiel 1: Ruft die Back-End-Integrität mit erweiterten Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="912f1-110">--------------------------  Example 1: Gets backend health with expanded resources.</span></span>  --------------------------
```
PS C:\>$BackendHealth = Get-AzureRmApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01 -ExpandResource "backendhealth/applicationgatewayresource"
```

<span data-ttu-id="912f1-111">Dieser Befehl ruft den Back-End-Status (mit erweiterten Ressourcen) des Anwendungs Gateways mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $BackendHealth-Variablen.</span><span class="sxs-lookup"><span data-stu-id="912f1-111">This command gets the backend health (with expanded resources) of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

## <span data-ttu-id="912f1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="912f1-112">PARAMETERS</span></span>

### <span data-ttu-id="912f1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="912f1-113">-AsJob</span></span>
<span data-ttu-id="912f1-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="912f1-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="912f1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="912f1-115">-DefaultProfile</span></span>
<span data-ttu-id="912f1-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="912f1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="912f1-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="912f1-117">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="912f1-118">-Name</span><span class="sxs-lookup"><span data-stu-id="912f1-118">-Name</span></span>
<span data-ttu-id="912f1-119">Gibt den Namen des Anwendungs Gateways an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="912f1-119">Specifies the name of the application gateway that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="912f1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="912f1-120">-ResourceGroupName</span></span>
<span data-ttu-id="912f1-121">Gibt den Namen der Ressourcengruppe an, die das Anwendungsgateway enthält.</span><span class="sxs-lookup"><span data-stu-id="912f1-121">Specifies the name of the resource group that contains the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="912f1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="912f1-122">CommonParameters</span></span>
<span data-ttu-id="912f1-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="912f1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="912f1-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="912f1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="912f1-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="912f1-125">INPUTS</span></span>

### <span data-ttu-id="912f1-126">System. String</span><span class="sxs-lookup"><span data-stu-id="912f1-126">System.String</span></span>

## <span data-ttu-id="912f1-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="912f1-127">OUTPUTS</span></span>

### <span data-ttu-id="912f1-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="912f1-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="912f1-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="912f1-129">NOTES</span></span>
<span data-ttu-id="912f1-130">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="912f1-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="912f1-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="912f1-131">RELATED LINKS</span></span>

[<span data-ttu-id="912f1-132">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="912f1-132">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

