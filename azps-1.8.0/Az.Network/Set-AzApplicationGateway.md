---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
ms.openlocfilehash: 34f3de9e2dafe3cfb9b15aad1dda7d75bab67c20
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660279"
---
# <span data-ttu-id="24099-101">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="24099-101">Set-AzApplicationGateway</span></span>

## <span data-ttu-id="24099-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="24099-102">SYNOPSIS</span></span>
<span data-ttu-id="24099-103">Aktualisiert ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="24099-103">Updates an application gateway.</span></span>

## <span data-ttu-id="24099-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="24099-104">SYNTAX</span></span>

```
Set-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24099-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="24099-105">DESCRIPTION</span></span>
<span data-ttu-id="24099-106">Das Cmdlet " **Satz-AzApplicationGateway** " aktualisiert ein Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="24099-106">The **Set-AzApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="24099-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="24099-107">EXAMPLES</span></span>

### <span data-ttu-id="24099-108">Beispiel 1: Aktualisieren eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="24099-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$UpdatedAppGw = Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="24099-109">Dieser Befehl aktualisiert das Anwendungsgateway mit den Einstellungen in der $AppGw Variablen und speichert das aktualisierte Gateway in der $UpdatedAppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="24099-109">This command updates the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="24099-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="24099-110">PARAMETERS</span></span>

### <span data-ttu-id="24099-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="24099-111">-ApplicationGateway</span></span>
<span data-ttu-id="24099-112">Gibt ein Application Gateway-Objekt an, das den Zustand darstellt, in dem das Anwendungsgateway festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="24099-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="24099-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24099-113">-AsJob</span></span>
<span data-ttu-id="24099-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="24099-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24099-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24099-115">-DefaultProfile</span></span>
<span data-ttu-id="24099-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="24099-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24099-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24099-117">CommonParameters</span></span>
<span data-ttu-id="24099-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24099-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24099-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24099-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24099-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="24099-120">INPUTS</span></span>

### <span data-ttu-id="24099-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="24099-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="24099-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="24099-122">OUTPUTS</span></span>

### <span data-ttu-id="24099-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="24099-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="24099-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="24099-124">NOTES</span></span>

## <span data-ttu-id="24099-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="24099-125">RELATED LINKS</span></span>

[<span data-ttu-id="24099-126">Anfang-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="24099-126">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


