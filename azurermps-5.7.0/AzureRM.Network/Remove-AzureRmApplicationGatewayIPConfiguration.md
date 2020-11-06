---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 823b4ce458e4308965b4c5bea1ad5739708f7aff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504534"
---
# <span data-ttu-id="28e62-101">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="28e62-101">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="28e62-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="28e62-102">SYNOPSIS</span></span>
<span data-ttu-id="28e62-103">Entfernt eine IP-Konfiguration von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="28e62-103">Removes an IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28e62-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="28e62-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28e62-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28e62-105">DESCRIPTION</span></span>
<span data-ttu-id="28e62-106">Das Cmdlet **Remove-AzureRmApplicationGatewayIPConfiguration** entfernt eine IP-Konfiguration von einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="28e62-106">The **Remove-AzureRmApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="28e62-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="28e62-107">EXAMPLES</span></span>

### <span data-ttu-id="28e62-108">Beispiel 1: Entfernen einer IP-Konfiguration von einem Azure Application Gateway</span><span class="sxs-lookup"><span data-stu-id="28e62-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="28e62-109">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="28e62-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="28e62-110">Der zweite Befehl entfernt die IP-Konfiguration mit dem Namen Subnet02 aus dem Anwendungsgateway, das in $AppGw gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="28e62-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="28e62-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="28e62-111">PARAMETERS</span></span>

### <span data-ttu-id="28e62-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="28e62-112">-ApplicationGateway</span></span>
<span data-ttu-id="28e62-113">Gibt das Anwendungsgateway an, aus dem eine IP-Konfiguration entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="28e62-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="28e62-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28e62-114">-DefaultProfile</span></span>
<span data-ttu-id="28e62-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="28e62-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28e62-116">-Name</span><span class="sxs-lookup"><span data-stu-id="28e62-116">-Name</span></span>
<span data-ttu-id="28e62-117">Gibt den Namen der zu entfernenden IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="28e62-117">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="28e62-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28e62-118">CommonParameters</span></span>
<span data-ttu-id="28e62-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28e62-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28e62-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28e62-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28e62-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="28e62-121">INPUTS</span></span>

### <span data-ttu-id="28e62-122">System. String</span><span class="sxs-lookup"><span data-stu-id="28e62-122">System.String</span></span>

## <span data-ttu-id="28e62-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="28e62-123">OUTPUTS</span></span>

### <span data-ttu-id="28e62-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="28e62-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="28e62-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="28e62-125">NOTES</span></span>

## <span data-ttu-id="28e62-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="28e62-126">RELATED LINKS</span></span>

[<span data-ttu-id="28e62-127">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="28e62-127">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="28e62-128">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="28e62-128">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="28e62-129">Neu – AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="28e62-129">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="28e62-130">Satz-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="28e62-130">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


