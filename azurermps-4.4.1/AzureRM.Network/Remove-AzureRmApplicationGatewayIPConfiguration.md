---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 4ef644fb92bf3f872a9e80aef2674a3ffb56747b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497070"
---
# <span data-ttu-id="56651-101">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="56651-101">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="56651-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="56651-102">SYNOPSIS</span></span>
<span data-ttu-id="56651-103">Entfernt eine IP-Konfiguration von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="56651-103">Removes an IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56651-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="56651-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56651-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56651-105">DESCRIPTION</span></span>
<span data-ttu-id="56651-106">Das Cmdlet **Remove-AzureRmApplicationGatewayIPConfiguration** entfernt eine IP-Konfiguration von einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="56651-106">The **Remove-AzureRmApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="56651-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="56651-107">EXAMPLES</span></span>

### <span data-ttu-id="56651-108">Beispiel 1: Entfernen einer IP-Konfiguration von einem Azure Application Gateway</span><span class="sxs-lookup"><span data-stu-id="56651-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="56651-109">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="56651-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="56651-110">Der zweite Befehl entfernt die IP-Konfiguration mit dem Namen Subnet02 aus dem Anwendungsgateway, das in $AppGw gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="56651-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="56651-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="56651-111">PARAMETERS</span></span>

### <span data-ttu-id="56651-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="56651-112">-ApplicationGateway</span></span>
<span data-ttu-id="56651-113">Gibt das Anwendungsgateway an, aus dem eine IP-Konfiguration entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="56651-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="56651-114">-Name</span><span class="sxs-lookup"><span data-stu-id="56651-114">-Name</span></span>
<span data-ttu-id="56651-115">Gibt den Namen der zu entfernenden IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="56651-115">Specifies the name of the IP configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56651-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56651-116">-DefaultProfile</span></span>
<span data-ttu-id="56651-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="56651-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56651-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56651-118">CommonParameters</span></span>
<span data-ttu-id="56651-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56651-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56651-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56651-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56651-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="56651-121">INPUTS</span></span>

### <span data-ttu-id="56651-122">System. String</span><span class="sxs-lookup"><span data-stu-id="56651-122">System.String</span></span>

## <span data-ttu-id="56651-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="56651-123">OUTPUTS</span></span>

### <span data-ttu-id="56651-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="56651-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="56651-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="56651-125">NOTES</span></span>

## <span data-ttu-id="56651-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="56651-126">RELATED LINKS</span></span>

[<span data-ttu-id="56651-127">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="56651-127">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="56651-128">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="56651-128">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="56651-129">Neu – AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="56651-129">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="56651-130">Satz-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="56651-130">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


