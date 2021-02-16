---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 5aeae0fe7a3efe4513869991d1e53ac429f52401
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157084"
---
# <span data-ttu-id="47e02-101">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="47e02-101">Get-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="47e02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47e02-102">SYNOPSIS</span></span>
<span data-ttu-id="47e02-103">Ruft die Back-End-HTTP-Einstellungen eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="47e02-103">Gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="47e02-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47e02-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHttpSetting [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47e02-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47e02-105">DESCRIPTION</span></span>
<span data-ttu-id="47e02-106">Das Get-AzApplicationGatewayBackendHttpSetting ruft die Back-End-HTTP-Einstellungen eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="47e02-106">The Get-AzApplicationGatewayBackendHttpSetting cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="47e02-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="47e02-107">EXAMPLES</span></span>

### <span data-ttu-id="47e02-108">Beispiel 1: Erhalten der Back-End-HTTP-Einstellungen nach Name</span><span class="sxs-lookup"><span data-stu-id="47e02-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSetting -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="47e02-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variable. Der zweite Befehl ruft die HTTP-Einstellungen namens "Settings01" für $AppGw und speichert die Einstellungen in der $Settings Variable.</span><span class="sxs-lookup"><span data-stu-id="47e02-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="47e02-110">Beispiel 2: Erhalten einer Sammlung von Back-End-HTTP-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="47e02-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw
```

<span data-ttu-id="47e02-111">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variable. Der zweite Befehl ruft die Sammlung der HTTP-Einstellungen für $AppGw und speichert die Einstellungen in der $SettingsList Variable.</span><span class="sxs-lookup"><span data-stu-id="47e02-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="47e02-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47e02-112">PARAMETERS</span></span>

### <span data-ttu-id="47e02-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47e02-113">-ApplicationGateway</span></span>
<span data-ttu-id="47e02-114">Gibt ein Anwendungsgatewayobjekt an, das back-end-HTTP-Einstellungen enthält.</span><span class="sxs-lookup"><span data-stu-id="47e02-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

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

### <span data-ttu-id="47e02-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47e02-115">-DefaultProfile</span></span>
<span data-ttu-id="47e02-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47e02-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47e02-117">-Name</span><span class="sxs-lookup"><span data-stu-id="47e02-117">-Name</span></span>
<span data-ttu-id="47e02-118">Gibt den Namen der BACK-End-HTTP-Einstellungen an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="47e02-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="47e02-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47e02-119">CommonParameters</span></span>
<span data-ttu-id="47e02-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47e02-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47e02-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47e02-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47e02-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="47e02-122">INPUTS</span></span>

### <span data-ttu-id="47e02-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47e02-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="47e02-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="47e02-124">OUTPUTS</span></span>

### <span data-ttu-id="47e02-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="47e02-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="47e02-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="47e02-126">NOTES</span></span>

## <span data-ttu-id="47e02-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="47e02-127">RELATED LINKS</span></span>

[<span data-ttu-id="47e02-128">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="47e02-128">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="47e02-129">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="47e02-129">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="47e02-130">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="47e02-130">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="47e02-131">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="47e02-131">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

