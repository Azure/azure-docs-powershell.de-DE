---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: e965f2cdbd9909003a07ea6c6addd198110e456f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841200"
---
# <span data-ttu-id="020e7-101">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="020e7-101">Remove-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="020e7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="020e7-102">SYNOPSIS</span></span>
<span data-ttu-id="020e7-103">Entfernt eine Umleitungs Konfiguration von einem vorhandenen Anwendungs Gateway.</span><span class="sxs-lookup"><span data-stu-id="020e7-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="020e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="020e7-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="020e7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="020e7-105">DESCRIPTION</span></span>
<span data-ttu-id="020e7-106">Das Cmdlet **Remove-AzApplicationGatewayRedirectConfiguration** entfernt eine Umleitungs Konfiguration von einem vorhandenen Anwendungs Gateway.</span><span class="sxs-lookup"><span data-stu-id="020e7-106">The **Remove-AzApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="020e7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="020e7-107">EXAMPLES</span></span>

### <span data-ttu-id="020e7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="020e7-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="020e7-109">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="020e7-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="020e7-110">Mit dem zweiten Befehl wird die Umleitungs Konfiguration mit dem Namen Redirect01 aus dem Anwendungsgateway entfernt, das in $AppGw gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="020e7-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="020e7-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="020e7-111">PARAMETERS</span></span>

### <span data-ttu-id="020e7-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="020e7-112">-ApplicationGateway</span></span>
<span data-ttu-id="020e7-113">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="020e7-113">The applicationGateway</span></span>

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

### <span data-ttu-id="020e7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="020e7-114">-DefaultProfile</span></span>
<span data-ttu-id="020e7-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="020e7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="020e7-116">-Name</span><span class="sxs-lookup"><span data-stu-id="020e7-116">-Name</span></span>
<span data-ttu-id="020e7-117">Der Name der Umleitungs Konfiguration</span><span class="sxs-lookup"><span data-stu-id="020e7-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="020e7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="020e7-118">CommonParameters</span></span>
<span data-ttu-id="020e7-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="020e7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="020e7-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="020e7-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="020e7-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="020e7-121">INPUTS</span></span>

### <span data-ttu-id="020e7-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="020e7-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="020e7-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="020e7-123">OUTPUTS</span></span>

### <span data-ttu-id="020e7-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="020e7-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="020e7-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="020e7-125">NOTES</span></span>

## <span data-ttu-id="020e7-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="020e7-126">RELATED LINKS</span></span>

