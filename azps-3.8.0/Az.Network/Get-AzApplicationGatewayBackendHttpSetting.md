---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 5aeae0fe7a3efe4513869991d1e53ac429f52401
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003776"
---
# <span data-ttu-id="992ee-101">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="992ee-101">Get-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="992ee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="992ee-102">SYNOPSIS</span></span>
<span data-ttu-id="992ee-103">Ruft die Back-End-HTTP-Einstellungen eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="992ee-103">Gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="992ee-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="992ee-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHttpSetting [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="992ee-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="992ee-105">DESCRIPTION</span></span>
<span data-ttu-id="992ee-106">Das Get-AzApplicationGatewayBackendHttpSetting-Cmdlet ruft die HTTP-Back-End-Einstellungen eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="992ee-106">The Get-AzApplicationGatewayBackendHttpSetting cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="992ee-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="992ee-107">EXAMPLES</span></span>

### <span data-ttu-id="992ee-108">Beispiel 1: Abrufen von HTTP-Back-End-Einstellungen nach Name</span><span class="sxs-lookup"><span data-stu-id="992ee-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSetting -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="992ee-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen. Der zweite Befehl ruft die http-Einstellungen mit dem Namen Settings01 für $AppGw ab und speichert die Einstellungen in der $Settings-Variablen.</span><span class="sxs-lookup"><span data-stu-id="992ee-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="992ee-110">Beispiel 2: Abrufen einer Sammlung von Back-End-HTTP-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="992ee-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw
```

<span data-ttu-id="992ee-111">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen. Der zweite Befehl ruft die Sammlung von http-Einstellungen für $AppGw ab und speichert die Einstellungen in der $SettingsList-Variablen.</span><span class="sxs-lookup"><span data-stu-id="992ee-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="992ee-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="992ee-112">PARAMETERS</span></span>

### <span data-ttu-id="992ee-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="992ee-113">-ApplicationGateway</span></span>
<span data-ttu-id="992ee-114">Gibt ein Application Gateway-Objekt an, das Back-End-HTTP-Einstellungen enthält.</span><span class="sxs-lookup"><span data-stu-id="992ee-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

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

### <span data-ttu-id="992ee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="992ee-115">-DefaultProfile</span></span>
<span data-ttu-id="992ee-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="992ee-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="992ee-117">-Name</span><span class="sxs-lookup"><span data-stu-id="992ee-117">-Name</span></span>
<span data-ttu-id="992ee-118">Gibt den Namen der HTTP-Back-End-Einstellungen an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="992ee-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="992ee-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="992ee-119">CommonParameters</span></span>
<span data-ttu-id="992ee-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="992ee-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="992ee-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="992ee-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="992ee-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="992ee-122">INPUTS</span></span>

### <span data-ttu-id="992ee-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="992ee-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="992ee-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="992ee-124">OUTPUTS</span></span>

### <span data-ttu-id="992ee-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="992ee-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="992ee-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="992ee-126">NOTES</span></span>

## <span data-ttu-id="992ee-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="992ee-127">RELATED LINKS</span></span>

[<span data-ttu-id="992ee-128">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="992ee-128">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="992ee-129">Neu – AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="992ee-129">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="992ee-130">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="992ee-130">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="992ee-131">Satz-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="992ee-131">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

