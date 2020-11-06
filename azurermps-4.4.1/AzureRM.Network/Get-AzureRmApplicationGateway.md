---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 77CDEE77-FD5D-4C2D-B027-FF1F6FF6618E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGateway.md
ms.openlocfilehash: 6c15f0dce8102acb609b2e7dcfb9ca4c17626906
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479133"
---
# <span data-ttu-id="37c83-101">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="37c83-101">Get-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="37c83-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="37c83-102">SYNOPSIS</span></span>
<span data-ttu-id="37c83-103">Ruft ein Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="37c83-103">Gets an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37c83-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="37c83-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGateway [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37c83-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37c83-105">DESCRIPTION</span></span>
<span data-ttu-id="37c83-106">Das Cmdlet " **Get-AzureRmApplicationGateway** " Ruft ein Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="37c83-106">The **Get-AzureRmApplicationGateway** cmdlet gets an application gateway.</span></span>

## <span data-ttu-id="37c83-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37c83-107">EXAMPLES</span></span>

### <span data-ttu-id="37c83-108">Beispiel 1: Abrufen eines angegebenen Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="37c83-108">Example 1: Get a specified application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="37c83-109">Dieser Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="37c83-109">This command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

### <span data-ttu-id="37c83-110">Beispiel 2: Abrufen einer Liste von Anwendungs Gateways in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="37c83-110">Example 2: Get a list of application gateways in a resource group</span></span>
```
PS C:\>$AppGwList = Get-AzureRmApplicationGateway -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="37c83-111">Dieser Befehl ruft eine Liste aller Anwendungs Gateways in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert Sie in der $AppGwList-Variablen.</span><span class="sxs-lookup"><span data-stu-id="37c83-111">This command gets a list of all the application gateways in the resource group named ResourceGroup01 and stores it in the $AppGwList variable.</span></span>

### <span data-ttu-id="37c83-112">Beispiel 3: Abrufen einer Liste von Anwendungs Gateways in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="37c83-112">Example 3: Get a list of application gateways in a subscription</span></span>
```
PS C:\>$AppGwList = Get-AzureRmApplicationGateway
```

<span data-ttu-id="37c83-113">Dieser Befehl ruft eine Liste aller Anwendungs Gateways im Abonnement ab und speichert Sie in der $AppGwList-Variablen.</span><span class="sxs-lookup"><span data-stu-id="37c83-113">This command gets a list of all the application gateways in the subscription and stores it in the $AppGwList variable.</span></span>

## <span data-ttu-id="37c83-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="37c83-114">PARAMETERS</span></span>

### <span data-ttu-id="37c83-115">-Name</span><span class="sxs-lookup"><span data-stu-id="37c83-115">-Name</span></span>
<span data-ttu-id="37c83-116">Gibt den Namen des Anwendungs Gateways an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="37c83-116">Specifies the name of the application gateway that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37c83-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37c83-117">-ResourceGroupName</span></span>
<span data-ttu-id="37c83-118">Gibt den Namen der Ressourcengruppe an, die das Anwendungsgateway enthält.</span><span class="sxs-lookup"><span data-stu-id="37c83-118">Specifies the name of the resource group that contains the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37c83-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37c83-119">-DefaultProfile</span></span>
<span data-ttu-id="37c83-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="37c83-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37c83-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37c83-121">CommonParameters</span></span>
<span data-ttu-id="37c83-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37c83-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37c83-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37c83-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37c83-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="37c83-124">INPUTS</span></span>

### <span data-ttu-id="37c83-125">System. String</span><span class="sxs-lookup"><span data-stu-id="37c83-125">System.String</span></span>

## <span data-ttu-id="37c83-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="37c83-126">OUTPUTS</span></span>

### <span data-ttu-id="37c83-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="37c83-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="37c83-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="37c83-128">NOTES</span></span>

## <span data-ttu-id="37c83-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="37c83-129">RELATED LINKS</span></span>

[<span data-ttu-id="37c83-130">Stopp-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="37c83-130">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


