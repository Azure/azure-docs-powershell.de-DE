---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGateway.md
ms.openlocfilehash: d9eb7f4783f950ba001be5b173fca9614422ce9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503477"
---
# <span data-ttu-id="1ae68-101">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ae68-101">Set-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="1ae68-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1ae68-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae68-103">Aktualisiert ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="1ae68-103">Updates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ae68-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ae68-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ae68-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1ae68-105">DESCRIPTION</span></span>
<span data-ttu-id="1ae68-106">Das Cmdlet " **Satz-AzureRmApplicationGateway** " aktualisiert ein Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="1ae68-106">The **Set-AzureRmApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="1ae68-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1ae68-107">EXAMPLES</span></span>

### <span data-ttu-id="1ae68-108">Beispiel 1: Aktualisieren eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="1ae68-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$UpdatedAppGw = Set-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="1ae68-109">Dieser Befehl aktualisiert das Anwendungsgateway mit den Einstellungen in der $AppGw Variablen und speichert das aktualisierte Gateway in der $UpdatedAppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="1ae68-109">This command updates the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="1ae68-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ae68-110">PARAMETERS</span></span>

### <span data-ttu-id="1ae68-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ae68-111">-ApplicationGateway</span></span>
<span data-ttu-id="1ae68-112">Gibt ein Application Gateway-Objekt an, das den Zustand darstellt, in dem das Anwendungsgateway festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1ae68-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="1ae68-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ae68-113">-AsJob</span></span>
<span data-ttu-id="1ae68-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1ae68-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1ae68-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ae68-115">-DefaultProfile</span></span>
<span data-ttu-id="1ae68-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1ae68-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ae68-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae68-117">CommonParameters</span></span>
<span data-ttu-id="1ae68-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ae68-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae68-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ae68-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae68-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1ae68-120">INPUTS</span></span>

### <span data-ttu-id="1ae68-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ae68-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="1ae68-122">Parameter: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1ae68-122">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="1ae68-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1ae68-123">OUTPUTS</span></span>

### <span data-ttu-id="1ae68-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ae68-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1ae68-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="1ae68-125">NOTES</span></span>

## <span data-ttu-id="1ae68-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1ae68-126">RELATED LINKS</span></span>

[<span data-ttu-id="1ae68-127">Anfang-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ae68-127">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


