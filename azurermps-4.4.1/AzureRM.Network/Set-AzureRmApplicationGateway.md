---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGateway.md
ms.openlocfilehash: f755c08b880a9ec97315931843d6dca6f5fc3229
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505885"
---
# <span data-ttu-id="9d7db-101">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9d7db-101">Set-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="9d7db-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9d7db-102">SYNOPSIS</span></span>
<span data-ttu-id="9d7db-103">Aktualisiert ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="9d7db-103">Updates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d7db-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d7db-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d7db-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d7db-105">DESCRIPTION</span></span>
<span data-ttu-id="9d7db-106">Das Cmdlet " **Satz-AzureRmApplicationGateway** " aktualisiert ein Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="9d7db-106">The **Set-AzureRmApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="9d7db-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9d7db-107">EXAMPLES</span></span>

### <span data-ttu-id="9d7db-108">Beispiel 1: Aktualisieren eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="9d7db-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$UpdatedAppGw = Set-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="9d7db-109">Dieser Befehl aktualisiert das Anwendungsgateway mit den Einstellungen in der $AppGw Variablen und speichert das aktualisierte Gateway in der $UpdatedAppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="9d7db-109">This command updates the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="9d7db-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d7db-110">PARAMETERS</span></span>

### <span data-ttu-id="9d7db-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9d7db-111">-ApplicationGateway</span></span>
<span data-ttu-id="9d7db-112">Gibt ein Application Gateway-Objekt an, das den Zustand darstellt, in dem das Anwendungsgateway festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9d7db-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="9d7db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d7db-113">-DefaultProfile</span></span>
<span data-ttu-id="9d7db-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9d7db-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d7db-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d7db-115">CommonParameters</span></span>
<span data-ttu-id="9d7db-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d7db-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d7db-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d7db-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d7db-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9d7db-118">INPUTS</span></span>

### <span data-ttu-id="9d7db-119">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9d7db-119">PSApplicationGateway</span></span>
<span data-ttu-id="9d7db-120">Der Parameter "ApplicationGateway" akzeptiert den Wert vom Typ "PSApplicationGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="9d7db-120">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="9d7db-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9d7db-121">OUTPUTS</span></span>

### <span data-ttu-id="9d7db-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9d7db-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9d7db-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="9d7db-123">NOTES</span></span>

## <span data-ttu-id="9d7db-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9d7db-124">RELATED LINKS</span></span>

[<span data-ttu-id="9d7db-125">Anfang-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9d7db-125">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


