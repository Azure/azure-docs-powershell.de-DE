---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 66da90ea590c4d2359dbe7e703667f9fe7189fba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662413"
---
# <span data-ttu-id="8be10-101">Get-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="8be10-101">Get-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="8be10-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8be10-102">SYNOPSIS</span></span>
<span data-ttu-id="8be10-103">Ruft eine vorhandene Umleitungs Konfiguration von einem Anwendungs Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="8be10-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8be10-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8be10-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8be10-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8be10-105">DESCRIPTION</span></span>
<span data-ttu-id="8be10-106">Das Cmdlet " **Get-AzureRmApplicationGatewayRedirectConfiguration** " Ruft eine vorhandene Umleitungs Konfiguration von einem Anwendungs Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="8be10-106">The **Get-AzureRmApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="8be10-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8be10-107">EXAMPLES</span></span>

### <span data-ttu-id="8be10-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8be10-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="8be10-109">Der erste Befehl ruft das Anwendungs Gateway mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen mit dem Namen $AppGW.</span><span class="sxs-lookup"><span data-stu-id="8be10-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="8be10-110">Der zweite Befehl ruft die Umleitungs Konfiguration mit dem Namen Redirect01 aus dem Anwendungs Gateway ab, das in der Variablen mit dem Namen $AppGW gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="8be10-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="8be10-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="8be10-111">PARAMETERS</span></span>

### <span data-ttu-id="8be10-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8be10-112">-ApplicationGateway</span></span>
<span data-ttu-id="8be10-113">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="8be10-113">The applicationGateway</span></span>

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

### <span data-ttu-id="8be10-114">-Name</span><span class="sxs-lookup"><span data-stu-id="8be10-114">-Name</span></span>
<span data-ttu-id="8be10-115">Der Name der Anforderungs Routingregel</span><span class="sxs-lookup"><span data-stu-id="8be10-115">The name of the request routing rule</span></span>

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

### <span data-ttu-id="8be10-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8be10-116">-DefaultProfile</span></span>
<span data-ttu-id="8be10-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8be10-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8be10-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8be10-118">CommonParameters</span></span>
<span data-ttu-id="8be10-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8be10-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8be10-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8be10-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8be10-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8be10-121">INPUTS</span></span>

### <span data-ttu-id="8be10-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8be10-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8be10-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8be10-123">OUTPUTS</span></span>

### <span data-ttu-id="8be10-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="8be10-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>
<span data-ttu-id="8be10-125">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration, Microsoft. Azure. Commands. Network, Version = 4.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="8be10-125">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8be10-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="8be10-126">NOTES</span></span>

## <span data-ttu-id="8be10-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8be10-127">RELATED LINKS</span></span>

