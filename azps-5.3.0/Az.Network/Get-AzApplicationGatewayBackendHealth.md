---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D5E928C3-26B6-4B7C-8A9C-F1F602BABF75
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
ms.openlocfilehash: 378c6ee91c438bfa70ab8e89e069ad81d3515e33
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468220"
---
# <span data-ttu-id="98116-101">Get-AzApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="98116-101">Get-AzApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="98116-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98116-102">SYNOPSIS</span></span>
<span data-ttu-id="98116-103">Ruft den Integritätszustand des Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="98116-103">Gets application gateway backend health.</span></span>

## <span data-ttu-id="98116-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98116-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHealth -Name <String> -ResourceGroupName <String> [-ExpandResource <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98116-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="98116-105">DESCRIPTION</span></span>
<span data-ttu-id="98116-106">Das Get-AzApplicationGatewayBackendHealth erhält den Integritätszustand des Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="98116-106">The Get-AzApplicationGatewayBackendHealth cmdlet gets application gateway backend health.</span></span>

## <span data-ttu-id="98116-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="98116-107">EXAMPLES</span></span>

### <span data-ttu-id="98116-108">Beispiel 1: Ruft die Back-End-Integrität ohne erweiterte Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="98116-108">Example 1: Gets backend health without expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="98116-109">Dieser Befehl ruft den Back-End-Zustand des Anwendungsgateways namens ApplicationGateway01 ab, das zur Ressourcengruppe "ResourceGroup01" gehört und in der Variablen $BackendHealth speichert.</span><span class="sxs-lookup"><span data-stu-id="98116-109">This command gets the backend health of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

### <span data-ttu-id="98116-110">Beispiel 2: Ruft den Back-End-Zustand mit erweiterten Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="98116-110">Example 2: Gets backend health with expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01 -ExpandResource "backendhealth/applicationgatewayresource"
```

<span data-ttu-id="98116-111">Dieser Befehl ruft den Back-End-Integritätszustand (mit erweiterten Ressourcen) des Anwendungsgateways namens ApplicationGateway01 ab, das zur Ressourcengruppe "ResourceGroup01" gehört und in der Variablen "$BackendHealth" speichert.</span><span class="sxs-lookup"><span data-stu-id="98116-111">This command gets the backend health (with expanded resources) of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

## <span data-ttu-id="98116-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98116-112">PARAMETERS</span></span>

### <span data-ttu-id="98116-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98116-113">-AsJob</span></span>
<span data-ttu-id="98116-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="98116-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98116-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98116-115">-DefaultProfile</span></span>
<span data-ttu-id="98116-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="98116-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98116-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="98116-117">-ExpandResource</span></span>
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

### <span data-ttu-id="98116-118">-Name</span><span class="sxs-lookup"><span data-stu-id="98116-118">-Name</span></span>
<span data-ttu-id="98116-119">Gibt den Namen des Anwendungsgateways an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="98116-119">Specifies the name of the application gateway that this cmdlet gets.</span></span>

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

### <span data-ttu-id="98116-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98116-120">-ResourceGroupName</span></span>
<span data-ttu-id="98116-121">Gibt den Namen der Ressourcengruppe an, die das Anwendungsgateway enthält.</span><span class="sxs-lookup"><span data-stu-id="98116-121">Specifies the name of the resource group that contains the application gateway.</span></span>

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

### <span data-ttu-id="98116-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98116-122">CommonParameters</span></span>
<span data-ttu-id="98116-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98116-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98116-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98116-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98116-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="98116-125">INPUTS</span></span>

### <span data-ttu-id="98116-126">System.String</span><span class="sxs-lookup"><span data-stu-id="98116-126">System.String</span></span>

## <span data-ttu-id="98116-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="98116-127">OUTPUTS</span></span>

### <span data-ttu-id="98116-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="98116-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="98116-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="98116-129">NOTES</span></span>
<span data-ttu-id="98116-130">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="98116-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="98116-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="98116-131">RELATED LINKS</span></span>

[<span data-ttu-id="98116-132">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="98116-132">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

