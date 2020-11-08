---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
ms.openlocfilehash: d701e563e05f33b3cb0ed99a2e62fbcd54935987
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178298"
---
# <span data-ttu-id="37d9e-101">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="37d9e-101">Set-AzApplicationGateway</span></span>

## <span data-ttu-id="37d9e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="37d9e-102">SYNOPSIS</span></span>
<span data-ttu-id="37d9e-103">Aktualisiert ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="37d9e-103">Updates an application gateway.</span></span>

## <span data-ttu-id="37d9e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="37d9e-104">SYNTAX</span></span>

```
Set-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37d9e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37d9e-105">DESCRIPTION</span></span>
<span data-ttu-id="37d9e-106">Das Cmdlet " **Satz-AzApplicationGateway** " aktualisiert ein Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="37d9e-106">The **Set-AzApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="37d9e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37d9e-107">EXAMPLES</span></span>

### <span data-ttu-id="37d9e-108">Beispiel 1: Aktualisieren eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="37d9e-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name Test -ResourceGroupName Appgwtest
PS C:\>$AppGw.Tag = @{"key"="value"}
PS C:\>$UpdatedAppGw = Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="37d9e-109">Diese Befehle aktualisieren das Anwendungsgateway mit den Einstellungen in der $AppGw Variablen und speichern das aktualisierte Gateway in der $UpdatedAppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="37d9e-109">These commands update the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="37d9e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="37d9e-110">PARAMETERS</span></span>

### <span data-ttu-id="37d9e-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="37d9e-111">-ApplicationGateway</span></span>
<span data-ttu-id="37d9e-112">Gibt ein Application Gateway-Objekt an, das den Zustand darstellt, in dem das Anwendungsgateway festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="37d9e-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="37d9e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37d9e-113">-AsJob</span></span>
<span data-ttu-id="37d9e-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="37d9e-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37d9e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37d9e-115">-DefaultProfile</span></span>
<span data-ttu-id="37d9e-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="37d9e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37d9e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37d9e-117">CommonParameters</span></span>
<span data-ttu-id="37d9e-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37d9e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37d9e-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37d9e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37d9e-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="37d9e-120">INPUTS</span></span>

### <span data-ttu-id="37d9e-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="37d9e-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="37d9e-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="37d9e-122">OUTPUTS</span></span>

### <span data-ttu-id="37d9e-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="37d9e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="37d9e-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="37d9e-124">NOTES</span></span>

## <span data-ttu-id="37d9e-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="37d9e-125">RELATED LINKS</span></span>

[<span data-ttu-id="37d9e-126">Anfang-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="37d9e-126">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


