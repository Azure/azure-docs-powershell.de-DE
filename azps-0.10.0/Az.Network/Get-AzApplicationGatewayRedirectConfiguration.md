---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: c9443c93745c1f6db9372b8f845f3ac399e51398
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841715"
---
# <span data-ttu-id="cc898-101">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="cc898-101">Get-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="cc898-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cc898-102">SYNOPSIS</span></span>
<span data-ttu-id="cc898-103">Ruft eine vorhandene Umleitungs Konfiguration von einem Anwendungs Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="cc898-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="cc898-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc898-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc898-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cc898-105">DESCRIPTION</span></span>
<span data-ttu-id="cc898-106">Das Cmdlet " **Get-AzApplicationGatewayRedirectConfiguration** " Ruft eine vorhandene Umleitungs Konfiguration von einem Anwendungs Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="cc898-106">The **Get-AzApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="cc898-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cc898-107">EXAMPLES</span></span>

### <span data-ttu-id="cc898-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cc898-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="cc898-109">Der erste Befehl ruft das Anwendungs Gateway mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen mit dem Namen $AppGW.</span><span class="sxs-lookup"><span data-stu-id="cc898-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="cc898-110">Der zweite Befehl ruft die Umleitungs Konfiguration mit dem Namen Redirect01 aus dem Anwendungs Gateway ab, das in der Variablen mit dem Namen $AppGW gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="cc898-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="cc898-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc898-111">PARAMETERS</span></span>

### <span data-ttu-id="cc898-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cc898-112">-ApplicationGateway</span></span>
<span data-ttu-id="cc898-113">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="cc898-113">The applicationGateway</span></span>

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

### <span data-ttu-id="cc898-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc898-114">-DefaultProfile</span></span>
<span data-ttu-id="cc898-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cc898-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc898-116">-Name</span><span class="sxs-lookup"><span data-stu-id="cc898-116">-Name</span></span>
<span data-ttu-id="cc898-117">Der Name der Anforderungs Routingregel</span><span class="sxs-lookup"><span data-stu-id="cc898-117">The name of the request routing rule</span></span>

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

### <span data-ttu-id="cc898-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc898-118">CommonParameters</span></span>
<span data-ttu-id="cc898-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc898-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc898-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc898-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc898-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cc898-121">INPUTS</span></span>

### <span data-ttu-id="cc898-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cc898-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cc898-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cc898-123">OUTPUTS</span></span>

### <span data-ttu-id="cc898-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="cc898-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>
<span data-ttu-id="cc898-125">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration, Microsoft. Azure. Commands. Network, Version = 4.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="cc898-125">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="cc898-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="cc898-126">NOTES</span></span>

## <span data-ttu-id="cc898-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cc898-127">RELATED LINKS</span></span>

