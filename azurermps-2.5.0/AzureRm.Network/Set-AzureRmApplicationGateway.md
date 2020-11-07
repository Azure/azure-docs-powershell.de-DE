---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 1b852be30b513963f5d311940162078bdf6f692a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850587"
---
# <span data-ttu-id="41167-101">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="41167-101">Set-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="41167-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="41167-102">SYNOPSIS</span></span>
<span data-ttu-id="41167-103">Aktualisiert ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="41167-103">Updates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41167-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="41167-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41167-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="41167-105">DESCRIPTION</span></span>
<span data-ttu-id="41167-106">Das Cmdlet " **Satz-AzureRmApplicationGateway** " aktualisiert ein Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="41167-106">The **Set-AzureRmApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="41167-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="41167-107">EXAMPLES</span></span>

### <span data-ttu-id="41167-108">Beispiel 1: Aktualisieren eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="41167-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$UpdatedAppGw = Set-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="41167-109">Dieser Befehl aktualisiert das Anwendungsgateway mit den Einstellungen in der $AppGw Variablen und speichert das aktualisierte Gateway in der $UpdatedAppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="41167-109">This command updates the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="41167-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="41167-110">PARAMETERS</span></span>

### <span data-ttu-id="41167-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="41167-111">-ApplicationGateway</span></span>
<span data-ttu-id="41167-112">Gibt ein Application Gateway-Objekt an, das den Zustand darstellt, in dem das Anwendungsgateway festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="41167-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="41167-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41167-113">-AsJob</span></span>
<span data-ttu-id="41167-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="41167-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41167-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41167-115">-DefaultProfile</span></span>
<span data-ttu-id="41167-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="41167-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41167-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41167-117">CommonParameters</span></span>
<span data-ttu-id="41167-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41167-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41167-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41167-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41167-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="41167-120">INPUTS</span></span>

### <span data-ttu-id="41167-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="41167-121">PSApplicationGateway</span></span>
<span data-ttu-id="41167-122">Der Parameter "ApplicationGateway" akzeptiert den Wert vom Typ "PSApplicationGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="41167-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="41167-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="41167-123">OUTPUTS</span></span>

### <span data-ttu-id="41167-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="41167-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="41167-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="41167-125">NOTES</span></span>

## <span data-ttu-id="41167-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="41167-126">RELATED LINKS</span></span>

[<span data-ttu-id="41167-127">Anfang-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="41167-127">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


