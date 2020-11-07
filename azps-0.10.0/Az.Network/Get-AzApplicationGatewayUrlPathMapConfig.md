---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 92d970d87b79b1a392b6da73c567d6e8445cfd90
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841691"
---
# <span data-ttu-id="03142-101">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="03142-101">Get-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="03142-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="03142-102">SYNOPSIS</span></span>
<span data-ttu-id="03142-103">Ruft ein Array von URL-Pfad Zuordnungen zu einem Back-End-Serverpool ab.</span><span class="sxs-lookup"><span data-stu-id="03142-103">Gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="03142-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="03142-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03142-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="03142-105">DESCRIPTION</span></span>
<span data-ttu-id="03142-106">Das Cmdlet " **Get-AzApplicationGatewayURLPathMapConfig** " Ruft ein Array von URL-Pfad Zuordnungen zu einem Back-End-Serverpool ab.</span><span class="sxs-lookup"><span data-stu-id="03142-106">The **Get-AzApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="03142-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="03142-107">EXAMPLES</span></span>

### <span data-ttu-id="03142-108">Beispiel 1: Abrufen einer URL-Pfad Zuordnungskonfiguration</span><span class="sxs-lookup"><span data-stu-id="03142-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="03142-109">Dieser Befehl ruft die URL-Pfad Zuordnungs Konfigurationen vom Back-End-Server ab, der sich auf dem Application Gateway mit dem Namen Gateway befindet.</span><span class="sxs-lookup"><span data-stu-id="03142-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="03142-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="03142-110">PARAMETERS</span></span>

### <span data-ttu-id="03142-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="03142-111">-ApplicationGateway</span></span>
<span data-ttu-id="03142-112">Gibt das Anwendungsgateway an, für das dieses Cmdlet eine URL-Pfad Zuordnungskonfiguration erhält.</span><span class="sxs-lookup"><span data-stu-id="03142-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="03142-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03142-113">-DefaultProfile</span></span>
<span data-ttu-id="03142-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="03142-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03142-115">-Name</span><span class="sxs-lookup"><span data-stu-id="03142-115">-Name</span></span>
<span data-ttu-id="03142-116">Gibt den URL-Pfad Zuordnungsnamen an, in dem dieses Cmdlet die Pfad Zuordnungskonfiguration erhält.</span><span class="sxs-lookup"><span data-stu-id="03142-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03142-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03142-117">CommonParameters</span></span>
<span data-ttu-id="03142-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03142-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03142-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03142-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03142-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="03142-120">INPUTS</span></span>

### <span data-ttu-id="03142-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="03142-121">PSApplicationGateway</span></span>
<span data-ttu-id="03142-122">Der Parameter "ApplicationGateway" akzeptiert den Wert vom Typ "PSApplicationGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="03142-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="03142-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="03142-123">OUTPUTS</span></span>

### <span data-ttu-id="03142-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="03142-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

### <span data-ttu-id="03142-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap]</span><span class="sxs-lookup"><span data-stu-id="03142-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]</span></span>

## <span data-ttu-id="03142-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="03142-126">NOTES</span></span>

## <span data-ttu-id="03142-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="03142-127">RELATED LINKS</span></span>

[<span data-ttu-id="03142-128">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="03142-128">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="03142-129">Neu – AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="03142-129">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="03142-130">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="03142-130">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="03142-131">Satz-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="03142-131">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


