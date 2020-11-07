---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 77CDEE77-FD5D-4C2D-B027-FF1F6FF6618E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGateway.md
ms.openlocfilehash: 61547a4ee5f60fccc371ca7b2c426ca1a4bbb005
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841772"
---
# <span data-ttu-id="60665-101">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="60665-101">Get-AzApplicationGateway</span></span>

## <span data-ttu-id="60665-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="60665-102">SYNOPSIS</span></span>
<span data-ttu-id="60665-103">Ruft ein Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="60665-103">Gets an application gateway.</span></span>

## <span data-ttu-id="60665-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="60665-104">SYNTAX</span></span>

```
Get-AzApplicationGateway [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60665-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60665-105">DESCRIPTION</span></span>
<span data-ttu-id="60665-106">Das Cmdlet " **Get-AzApplicationGateway** " Ruft ein Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="60665-106">The **Get-AzApplicationGateway** cmdlet gets an application gateway.</span></span>

## <span data-ttu-id="60665-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="60665-107">EXAMPLES</span></span>

### <span data-ttu-id="60665-108">Beispiel 1: Abrufen eines angegebenen Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="60665-108">Example 1: Get a specified application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="60665-109">Dieser Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="60665-109">This command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

### <span data-ttu-id="60665-110">Beispiel 2: Abrufen einer Liste von Anwendungs Gateways in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="60665-110">Example 2: Get a list of application gateways in a resource group</span></span>
```
PS C:\>$AppGwList = Get-AzApplicationGateway -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="60665-111">Dieser Befehl ruft eine Liste aller Anwendungs Gateways in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert Sie in der $AppGwList-Variablen.</span><span class="sxs-lookup"><span data-stu-id="60665-111">This command gets a list of all the application gateways in the resource group named ResourceGroup01 and stores it in the $AppGwList variable.</span></span>

### <span data-ttu-id="60665-112">Beispiel 3: Abrufen einer Liste von Anwendungs Gateways in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="60665-112">Example 3: Get a list of application gateways in a subscription</span></span>
```
PS C:\>$AppGwList = Get-AzApplicationGateway
```

<span data-ttu-id="60665-113">Dieser Befehl ruft eine Liste aller Anwendungs Gateways im Abonnement ab und speichert Sie in der $AppGwList-Variablen.</span><span class="sxs-lookup"><span data-stu-id="60665-113">This command gets a list of all the application gateways in the subscription and stores it in the $AppGwList variable.</span></span>

## <span data-ttu-id="60665-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="60665-114">PARAMETERS</span></span>

### <span data-ttu-id="60665-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60665-115">-DefaultProfile</span></span>
<span data-ttu-id="60665-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="60665-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60665-117">-Name</span><span class="sxs-lookup"><span data-stu-id="60665-117">-Name</span></span>
<span data-ttu-id="60665-118">Gibt den Namen des Anwendungs Gateways an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="60665-118">Specifies the name of the application gateway that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60665-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60665-119">-ResourceGroupName</span></span>
<span data-ttu-id="60665-120">Gibt den Namen der Ressourcengruppe an, die das Anwendungsgateway enthält.</span><span class="sxs-lookup"><span data-stu-id="60665-120">Specifies the name of the resource group that contains the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60665-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60665-121">CommonParameters</span></span>
<span data-ttu-id="60665-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60665-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60665-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60665-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60665-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="60665-124">INPUTS</span></span>

### <span data-ttu-id="60665-125">System. String</span><span class="sxs-lookup"><span data-stu-id="60665-125">System.String</span></span>

## <span data-ttu-id="60665-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="60665-126">OUTPUTS</span></span>

### <span data-ttu-id="60665-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="60665-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="60665-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="60665-128">NOTES</span></span>

## <span data-ttu-id="60665-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="60665-129">RELATED LINKS</span></span>

[<span data-ttu-id="60665-130">Stopp-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="60665-130">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


