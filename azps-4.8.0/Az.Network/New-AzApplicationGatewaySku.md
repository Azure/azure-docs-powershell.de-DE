---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 212ba438a701b9abbd2fd290f4fb0f867b551497
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174589"
---
# <span data-ttu-id="07f00-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="07f00-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="07f00-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="07f00-102">SYNOPSIS</span></span>
<span data-ttu-id="07f00-103">Erstellt eine SKU für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="07f00-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="07f00-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="07f00-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> [-Capacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07f00-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07f00-105">DESCRIPTION</span></span>
<span data-ttu-id="07f00-106">Das Cmdlet **New-AzApplicationGatewaySku** erstellt eine Lagerhaltungs Einheit (SKU) für ein Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="07f00-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="07f00-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07f00-107">EXAMPLES</span></span>

### <span data-ttu-id="07f00-108">Beispiel 1: Erstellen einer SKU für ein Azure-Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="07f00-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="07f00-109">Dieser Befehl erstellt eine SKU mit dem Namen Standard_Small für ein Azure Application Gateway und speichert das Ergebnis in der Variablen mit dem Namen $SKU.</span><span class="sxs-lookup"><span data-stu-id="07f00-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="07f00-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="07f00-110">PARAMETERS</span></span>

### <span data-ttu-id="07f00-111">-Kapazität</span><span class="sxs-lookup"><span data-stu-id="07f00-111">-Capacity</span></span>
<span data-ttu-id="07f00-112">Gibt die Anzahl der Instanzen eines Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="07f00-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="07f00-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07f00-113">-DefaultProfile</span></span>
<span data-ttu-id="07f00-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="07f00-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07f00-115">-Name</span><span class="sxs-lookup"><span data-stu-id="07f00-115">-Name</span></span>
<span data-ttu-id="07f00-116">Gibt den Namen der SKU an.</span><span class="sxs-lookup"><span data-stu-id="07f00-116">Specifies the name of the SKU.</span></span>
<span data-ttu-id="07f00-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="07f00-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="07f00-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="07f00-118">Standard_Small</span></span>
- <span data-ttu-id="07f00-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="07f00-119">Standard_Medium</span></span>
- <span data-ttu-id="07f00-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="07f00-120">Standard_Large</span></span>
- <span data-ttu-id="07f00-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="07f00-121">WAF_Medium</span></span>
- <span data-ttu-id="07f00-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="07f00-122">WAF_Large</span></span>
- <span data-ttu-id="07f00-123">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="07f00-123">Standard_v2</span></span>
- <span data-ttu-id="07f00-124">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="07f00-124">WAF_v2</span></span>

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

### <span data-ttu-id="07f00-125">-Tier</span><span class="sxs-lookup"><span data-stu-id="07f00-125">-Tier</span></span>
<span data-ttu-id="07f00-126">Gibt die Ebene der SKU an.</span><span class="sxs-lookup"><span data-stu-id="07f00-126">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="07f00-127">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="07f00-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="07f00-128">Standard</span><span class="sxs-lookup"><span data-stu-id="07f00-128">Standard</span></span>
- <span data-ttu-id="07f00-129">WAF</span><span class="sxs-lookup"><span data-stu-id="07f00-129">WAF</span></span>
- <span data-ttu-id="07f00-130">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="07f00-130">Standard_v2</span></span>
- <span data-ttu-id="07f00-131">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="07f00-131">WAF_v2</span></span>

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

### <span data-ttu-id="07f00-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07f00-132">CommonParameters</span></span>
<span data-ttu-id="07f00-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07f00-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07f00-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07f00-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07f00-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="07f00-135">INPUTS</span></span>

### <span data-ttu-id="07f00-136">Keine</span><span class="sxs-lookup"><span data-stu-id="07f00-136">None</span></span>

## <span data-ttu-id="07f00-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="07f00-137">OUTPUTS</span></span>

### <span data-ttu-id="07f00-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="07f00-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="07f00-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="07f00-139">NOTES</span></span>

## <span data-ttu-id="07f00-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="07f00-140">RELATED LINKS</span></span>

[<span data-ttu-id="07f00-141">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="07f00-141">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="07f00-142">Satz-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="07f00-142">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


