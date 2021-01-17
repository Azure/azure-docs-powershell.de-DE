---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
ms.openlocfilehash: 38a9d9d36d4abdf85149fe9d7da5387468985daf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468831"
---
# <span data-ttu-id="c8027-101">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c8027-101">Set-AzApplicationGateway</span></span>

## <span data-ttu-id="c8027-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8027-102">SYNOPSIS</span></span>
<span data-ttu-id="c8027-103">Aktualisiert ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="c8027-103">Updates an application gateway.</span></span>

## <span data-ttu-id="c8027-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8027-104">SYNTAX</span></span>

```
Set-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8027-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c8027-105">DESCRIPTION</span></span>
<span data-ttu-id="c8027-106">Das **Cmdlet Set-AzApplicationGateway** aktualisiert ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="c8027-106">The **Set-AzApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="c8027-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c8027-107">EXAMPLES</span></span>

### <span data-ttu-id="c8027-108">Beispiel 1: Aktualisieren eines Anwendungsgateways</span><span class="sxs-lookup"><span data-stu-id="c8027-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name Test -ResourceGroupName Appgwtest
PS C:\>$AppGw.Tag = @{"key"="value"}
PS C:\>$UpdatedAppGw = Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="c8027-109">Mit diesen Befehlen wird das Anwendungsgateway mit den Einstellungen in der Variablen $AppGw aktualisiert und das aktualisierte Gateway in der variablen $UpdatedAppGw gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c8027-109">These commands update the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="c8027-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8027-110">PARAMETERS</span></span>

### <span data-ttu-id="c8027-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c8027-111">-ApplicationGateway</span></span>
<span data-ttu-id="c8027-112">Gibt ein Anwendungsgatewayobjekt an, das den Zustand darstellt, in dem das Anwendungsgateway festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8027-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="c8027-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8027-113">-AsJob</span></span>
<span data-ttu-id="c8027-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c8027-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8027-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8027-115">-DefaultProfile</span></span>
<span data-ttu-id="c8027-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8027-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8027-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8027-117">CommonParameters</span></span>
<span data-ttu-id="c8027-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8027-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8027-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8027-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8027-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c8027-120">INPUTS</span></span>

### <span data-ttu-id="c8027-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c8027-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c8027-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c8027-122">OUTPUTS</span></span>

### <span data-ttu-id="c8027-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c8027-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c8027-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c8027-124">NOTES</span></span>

## <span data-ttu-id="c8027-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c8027-125">RELATED LINKS</span></span>

[<span data-ttu-id="c8027-126">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c8027-126">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


