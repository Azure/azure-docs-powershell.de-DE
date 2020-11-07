---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 51428d44c2fc5ce29259924f71617317b163ac29
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841176"
---
# <span data-ttu-id="5409a-101">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5409a-101">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="5409a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5409a-102">SYNOPSIS</span></span>
<span data-ttu-id="5409a-103">Entfernt URL-Pfad Zuordnungen zu einem Back-End-Serverpool.</span><span class="sxs-lookup"><span data-stu-id="5409a-103">Removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="5409a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5409a-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5409a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5409a-105">DESCRIPTION</span></span>
<span data-ttu-id="5409a-106">Das Cmdlet **Remove-AzApplicationGatewayUrlPathMapConfig** entfernt URL-Pfad Zuordnungen zu einem Back-End-Serverpool.</span><span class="sxs-lookup"><span data-stu-id="5409a-106">The **Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="5409a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5409a-107">EXAMPLES</span></span>

### <span data-ttu-id="5409a-108">1:</span><span class="sxs-lookup"><span data-stu-id="5409a-108">1:</span></span>
```

```

## <span data-ttu-id="5409a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5409a-109">PARAMETERS</span></span>

### <span data-ttu-id="5409a-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5409a-110">-ApplicationGateway</span></span>
<span data-ttu-id="5409a-111">Gibt das Anwendungsgateway an, auf das dieses Cmdlet die URL-Pfad Zuordnungskonfiguration entfernt.</span><span class="sxs-lookup"><span data-stu-id="5409a-111">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="5409a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5409a-112">-DefaultProfile</span></span>
<span data-ttu-id="5409a-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5409a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5409a-114">-Name</span><span class="sxs-lookup"><span data-stu-id="5409a-114">-Name</span></span>
<span data-ttu-id="5409a-115">Gibt den URL-Pfad Zuordnungsnamen an, den dieses Cmdlet vom Back-End-Server entfernt.</span><span class="sxs-lookup"><span data-stu-id="5409a-115">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5409a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5409a-116">CommonParameters</span></span>
<span data-ttu-id="5409a-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5409a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5409a-118">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5409a-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5409a-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5409a-119">INPUTS</span></span>

### <span data-ttu-id="5409a-120">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5409a-120">PSApplicationGateway</span></span>
<span data-ttu-id="5409a-121">Der Parameter "ApplicationGateway" akzeptiert den Wert vom Typ "PSApplicationGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5409a-121">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="5409a-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5409a-122">OUTPUTS</span></span>

### <span data-ttu-id="5409a-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5409a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5409a-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="5409a-124">NOTES</span></span>

## <span data-ttu-id="5409a-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5409a-125">RELATED LINKS</span></span>

[<span data-ttu-id="5409a-126">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5409a-126">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5409a-127">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5409a-127">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5409a-128">Neu – AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5409a-128">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5409a-129">Satz-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5409a-129">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


