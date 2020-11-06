---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: fbfcb7ae0c00c593dae58cee780fe17d87ff5650
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479697"
---
# <span data-ttu-id="01f3e-101">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="01f3e-101">New-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="01f3e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="01f3e-102">SYNOPSIS</span></span>
<span data-ttu-id="01f3e-103">Erstellt eine SKU für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="01f3e-103">Creates a SKU for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01f3e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="01f3e-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySku -Name <String> -Tier <String> -Capacity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01f3e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="01f3e-105">DESCRIPTION</span></span>
<span data-ttu-id="01f3e-106">Das Cmdlet **New-AzureRmApplicationGatewaySku** erstellt eine Lagerhaltungs Einheit (SKU) für ein Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="01f3e-106">The **New-AzureRmApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="01f3e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="01f3e-107">EXAMPLES</span></span>

### <span data-ttu-id="01f3e-108">Beispiel 1: Erstellen einer SKU für ein Azure-Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="01f3e-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="01f3e-109">Dieser Befehl erstellt eine SKU mit dem Namen Standard_Small für ein Azure Application Gateway und speichert das Ergebnis in der Variablen mit dem Namen $SKU.</span><span class="sxs-lookup"><span data-stu-id="01f3e-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="01f3e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="01f3e-110">PARAMETERS</span></span>

### <span data-ttu-id="01f3e-111">-Kapazität</span><span class="sxs-lookup"><span data-stu-id="01f3e-111">-Capacity</span></span>
<span data-ttu-id="01f3e-112">Gibt die Anzahl der Instanzen eines Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="01f3e-112">Specifies the number of instances of an application gateway.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01f3e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01f3e-113">-DefaultProfile</span></span>
<span data-ttu-id="01f3e-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="01f3e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01f3e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="01f3e-115">-Name</span></span>
<span data-ttu-id="01f3e-116">Gibt den Namen der SKU an.</span><span class="sxs-lookup"><span data-stu-id="01f3e-116">Specifies the name of the SKU.</span></span>

<span data-ttu-id="01f3e-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="01f3e-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="01f3e-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="01f3e-118">Standard_Small</span></span>
- <span data-ttu-id="01f3e-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="01f3e-119">Standard_Medium</span></span>
- <span data-ttu-id="01f3e-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="01f3e-120">Standard_Large</span></span>
- <span data-ttu-id="01f3e-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="01f3e-121">WAF_Medium</span></span>
- <span data-ttu-id="01f3e-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="01f3e-122">WAF_Large</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01f3e-123">-Tier</span><span class="sxs-lookup"><span data-stu-id="01f3e-123">-Tier</span></span>
<span data-ttu-id="01f3e-124">Gibt die Ebene der SKU an.</span><span class="sxs-lookup"><span data-stu-id="01f3e-124">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="01f3e-125">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="01f3e-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="01f3e-126">Standard</span><span class="sxs-lookup"><span data-stu-id="01f3e-126">Standard</span></span>
- <span data-ttu-id="01f3e-127">WAF</span><span class="sxs-lookup"><span data-stu-id="01f3e-127">WAF</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, WAF

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01f3e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01f3e-128">CommonParameters</span></span>
<span data-ttu-id="01f3e-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01f3e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01f3e-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01f3e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01f3e-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="01f3e-131">INPUTS</span></span>

### <span data-ttu-id="01f3e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="01f3e-132">System.String</span></span>

## <span data-ttu-id="01f3e-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="01f3e-133">OUTPUTS</span></span>

### <span data-ttu-id="01f3e-134">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="01f3e-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="01f3e-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="01f3e-135">NOTES</span></span>

## <span data-ttu-id="01f3e-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="01f3e-136">RELATED LINKS</span></span>

[<span data-ttu-id="01f3e-137">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="01f3e-137">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="01f3e-138">Satz-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="01f3e-138">Set-AzureRmApplicationGatewaySku</span></span>](./Set-AzureRmApplicationGatewaySku.md)


