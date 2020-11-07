---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 8a49bdeed095ee277d632559402c55ca3baf784c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846204"
---
# <span data-ttu-id="7d900-101">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d900-101">Get-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="7d900-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7d900-102">SYNOPSIS</span></span>
<span data-ttu-id="7d900-103">Ruft eine vorhandene Umleitungs Konfiguration von einem Anwendungs Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="7d900-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="7d900-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d900-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d900-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7d900-105">DESCRIPTION</span></span>
<span data-ttu-id="7d900-106">Das Cmdlet " **Get-AzApplicationGatewayRedirectConfiguration** " Ruft eine vorhandene Umleitungs Konfiguration von einem Anwendungs Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="7d900-106">The **Get-AzApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="7d900-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7d900-107">EXAMPLES</span></span>

### <span data-ttu-id="7d900-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7d900-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="7d900-109">Der erste Befehl ruft das Anwendungs Gateway mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen mit dem Namen $AppGW.</span><span class="sxs-lookup"><span data-stu-id="7d900-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="7d900-110">Der zweite Befehl ruft die Umleitungs Konfiguration mit dem Namen Redirect01 aus dem Anwendungs Gateway ab, das in der Variablen mit dem Namen $AppGW gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="7d900-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="7d900-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d900-111">PARAMETERS</span></span>

### <span data-ttu-id="7d900-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7d900-112">-ApplicationGateway</span></span>
<span data-ttu-id="7d900-113">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="7d900-113">The applicationGateway</span></span>

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

### <span data-ttu-id="7d900-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d900-114">-DefaultProfile</span></span>
<span data-ttu-id="7d900-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7d900-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d900-116">-Name</span><span class="sxs-lookup"><span data-stu-id="7d900-116">-Name</span></span>
<span data-ttu-id="7d900-117">Der Name der Anforderungs Routingregel</span><span class="sxs-lookup"><span data-stu-id="7d900-117">The name of the request routing rule</span></span>

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

### <span data-ttu-id="7d900-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d900-118">CommonParameters</span></span>
<span data-ttu-id="7d900-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d900-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d900-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d900-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d900-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7d900-121">INPUTS</span></span>

### <span data-ttu-id="7d900-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7d900-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7d900-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7d900-123">OUTPUTS</span></span>

### <span data-ttu-id="7d900-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d900-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="7d900-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="7d900-125">NOTES</span></span>

## <span data-ttu-id="7d900-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7d900-126">RELATED LINKS</span></span>

[<span data-ttu-id="7d900-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d900-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="7d900-128">Neu – AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d900-128">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="7d900-129">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d900-129">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="7d900-130">Satz-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d900-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
