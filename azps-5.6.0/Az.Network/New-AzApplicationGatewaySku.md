---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 1f99fe982496fc6cef3ee9579d8e0be555880aaa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945911"
---
# <span data-ttu-id="056b9-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="056b9-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="056b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="056b9-102">SYNOPSIS</span></span>
<span data-ttu-id="056b9-103">Erstellt eine SKU für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="056b9-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="056b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="056b9-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> [-Capacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="056b9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="056b9-105">DESCRIPTION</span></span>
<span data-ttu-id="056b9-106">Das **Cmdlet New-AzApplicationGatewaySku** erstellt eine Bestandshaltungseinheit (Stock Keeping Unit, SKU) für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="056b9-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="056b9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="056b9-107">EXAMPLES</span></span>

### <span data-ttu-id="056b9-108">Beispiel 1: Erstellen einer SKU für ein Azure-Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="056b9-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="056b9-109">Dieser Befehl erstellt eine SKU mit Standard_Small für ein Azure-Anwendungsgateway und speichert das Ergebnis in der Variablen namens $SKU.</span><span class="sxs-lookup"><span data-stu-id="056b9-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="056b9-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="056b9-110">PARAMETERS</span></span>

### <span data-ttu-id="056b9-111">-Kapazität</span><span class="sxs-lookup"><span data-stu-id="056b9-111">-Capacity</span></span>
<span data-ttu-id="056b9-112">Gibt die Anzahl der Instanzen eines Anwendungsgateways an.</span><span class="sxs-lookup"><span data-stu-id="056b9-112">Specifies the number of instances of an application gateway.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="056b9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="056b9-113">-DefaultProfile</span></span>
<span data-ttu-id="056b9-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="056b9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="056b9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="056b9-115">-Name</span></span>
<span data-ttu-id="056b9-116">Gibt den Namen der SKU an.</span><span class="sxs-lookup"><span data-stu-id="056b9-116">Specifies the name of the SKU.</span></span>
<span data-ttu-id="056b9-117">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="056b9-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="056b9-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="056b9-118">Standard_Small</span></span>
- <span data-ttu-id="056b9-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="056b9-119">Standard_Medium</span></span>
- <span data-ttu-id="056b9-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="056b9-120">Standard_Large</span></span>
- <span data-ttu-id="056b9-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="056b9-121">WAF_Medium</span></span>
- <span data-ttu-id="056b9-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="056b9-122">WAF_Large</span></span>
- <span data-ttu-id="056b9-123">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="056b9-123">Standard_v2</span></span>
- <span data-ttu-id="056b9-124">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="056b9-124">WAF_v2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large, Standard_v2, WAF_v2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="056b9-125">-Tier</span><span class="sxs-lookup"><span data-stu-id="056b9-125">-Tier</span></span>
<span data-ttu-id="056b9-126">Gibt die Ebene der SKU an.</span><span class="sxs-lookup"><span data-stu-id="056b9-126">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="056b9-127">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="056b9-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="056b9-128">Standard</span><span class="sxs-lookup"><span data-stu-id="056b9-128">Standard</span></span>
- <span data-ttu-id="056b9-129">WAF</span><span class="sxs-lookup"><span data-stu-id="056b9-129">WAF</span></span>
- <span data-ttu-id="056b9-130">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="056b9-130">Standard_v2</span></span>
- <span data-ttu-id="056b9-131">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="056b9-131">WAF_v2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, WAF, Standard_v2, WAF_v2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="056b9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="056b9-132">CommonParameters</span></span>
<span data-ttu-id="056b9-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="056b9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="056b9-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="056b9-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="056b9-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="056b9-135">INPUTS</span></span>

### <span data-ttu-id="056b9-136">Keine</span><span class="sxs-lookup"><span data-stu-id="056b9-136">None</span></span>

## <span data-ttu-id="056b9-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="056b9-137">OUTPUTS</span></span>

### <span data-ttu-id="056b9-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="056b9-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="056b9-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="056b9-139">NOTES</span></span>

## <span data-ttu-id="056b9-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="056b9-140">RELATED LINKS</span></span>

[<span data-ttu-id="056b9-141">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="056b9-141">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="056b9-142">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="056b9-142">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


