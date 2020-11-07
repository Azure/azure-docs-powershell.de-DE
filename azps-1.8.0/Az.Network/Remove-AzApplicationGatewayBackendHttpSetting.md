---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 6c5729ec4d450ad122e359b9bd009000212e3b0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660436"
---
# <span data-ttu-id="05bfd-101">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="05bfd-101">Remove-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="05bfd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="05bfd-102">SYNOPSIS</span></span>
<span data-ttu-id="05bfd-103">Entfernt die Back-End-HTTP-Einstellungen von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="05bfd-103">Removes back-end HTTP settings from an application gateway.</span></span>

## <span data-ttu-id="05bfd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="05bfd-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendHttpSetting -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05bfd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="05bfd-105">DESCRIPTION</span></span>
<span data-ttu-id="05bfd-106">Das Remove-AzApplicationGatewayBackendHttpSetting-Cmdlet entfernt http-Einstellungen (Back-End-Hypertext-Übertragungsprotokoll) von einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="05bfd-106">The Remove-AzApplicationGatewayBackendHttpSetting cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="05bfd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="05bfd-107">EXAMPLES</span></span>

### <span data-ttu-id="05bfd-108">Beispiel 1: Entfernen von Back-End-HTTP-Einstellungen von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="05bfd-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="05bfd-109">Der erste Befehl ruft ein Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="05bfd-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="05bfd-110">Der zweite Befehl entfernt die Back-End-HTTP-Einstellung mit dem Namen BackEndSetting02 aus dem Anwendungsgateway, das in $AppGw gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="05bfd-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="05bfd-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="05bfd-111">PARAMETERS</span></span>

### <span data-ttu-id="05bfd-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="05bfd-112">-ApplicationGateway</span></span>
<span data-ttu-id="05bfd-113">Gibt das Anwendungsgateway an, von dem dieses Cmdlet die Back-End-HTTP-Einstellungen entfernt.</span><span class="sxs-lookup"><span data-stu-id="05bfd-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

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

### <span data-ttu-id="05bfd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05bfd-114">-DefaultProfile</span></span>
<span data-ttu-id="05bfd-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="05bfd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05bfd-116">-Name</span><span class="sxs-lookup"><span data-stu-id="05bfd-116">-Name</span></span>
<span data-ttu-id="05bfd-117">Gibt den Namen der Back-End-HTTP-Einstellungen an, die von diesem Cmdlet entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="05bfd-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

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

### <span data-ttu-id="05bfd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05bfd-118">CommonParameters</span></span>
<span data-ttu-id="05bfd-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05bfd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05bfd-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05bfd-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05bfd-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="05bfd-121">INPUTS</span></span>

### <span data-ttu-id="05bfd-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="05bfd-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="05bfd-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="05bfd-123">OUTPUTS</span></span>

### <span data-ttu-id="05bfd-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="05bfd-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="05bfd-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="05bfd-125">NOTES</span></span>

## <span data-ttu-id="05bfd-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="05bfd-126">RELATED LINKS</span></span>

[<span data-ttu-id="05bfd-127">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="05bfd-127">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="05bfd-128">Neu – AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="05bfd-128">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="05bfd-129">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="05bfd-129">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="05bfd-130">Satz-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="05bfd-130">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

