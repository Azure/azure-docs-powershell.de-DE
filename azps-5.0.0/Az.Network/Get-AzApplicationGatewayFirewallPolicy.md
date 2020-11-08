---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: fdcd725c79a6f789879ab3103cec90b09c828e74
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180213"
---
# <span data-ttu-id="303f5-101">Get-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="303f5-101">Get-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="303f5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="303f5-102">SYNOPSIS</span></span>
<span data-ttu-id="303f5-103">Ruft eine Firewall-Richtlinie für Application Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="303f5-103">Gets an application gateway firewall policy.</span></span>

## <span data-ttu-id="303f5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="303f5-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFirewallPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="303f5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="303f5-105">DESCRIPTION</span></span>
<span data-ttu-id="303f5-106">Das Cmdlet " **Get-AzApplicationGatewayFirewallPolicy** " Ruft eine Firewall-Richtlinie für Application Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="303f5-106">The **Get-AzApplicationGatewayFirewallPolicy** cmdlet gets an application gateway firewall policy..</span></span>

## <span data-ttu-id="303f5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="303f5-107">EXAMPLES</span></span>

### <span data-ttu-id="303f5-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="303f5-108">Example 1</span></span>
```powershell
PS C:\> $AppGwFirewallPolicy = Get-AzApplicationGatewayFirewallPolicy -Name "FirewallPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="303f5-109">Dieser Befehl ruft die Firewall-Richtlinie des Anwendungs Gateways mit dem Namen FirewallPolicy1 ab, die zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert Sie in der $AppGwFirewallPolicy-Variablen.</span><span class="sxs-lookup"><span data-stu-id="303f5-109">This command gets the application gateway firewall policy named FirewallPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="303f5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="303f5-110">PARAMETERS</span></span>

### <span data-ttu-id="303f5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="303f5-111">-DefaultProfile</span></span>
<span data-ttu-id="303f5-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="303f5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="303f5-113">-Name</span><span class="sxs-lookup"><span data-stu-id="303f5-113">-Name</span></span>
<span data-ttu-id="303f5-114">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="303f5-114">The resource name.</span></span>

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

### <span data-ttu-id="303f5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="303f5-115">-ResourceGroupName</span></span>
<span data-ttu-id="303f5-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="303f5-116">The resource group name.</span></span>

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

### <span data-ttu-id="303f5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="303f5-117">CommonParameters</span></span>
<span data-ttu-id="303f5-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="303f5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="303f5-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="303f5-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="303f5-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="303f5-120">INPUTS</span></span>

### <span data-ttu-id="303f5-121">System. String</span><span class="sxs-lookup"><span data-stu-id="303f5-121">System.String</span></span>

## <span data-ttu-id="303f5-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="303f5-122">OUTPUTS</span></span>

### <span data-ttu-id="303f5-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="303f5-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="303f5-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="303f5-124">NOTES</span></span>

## <span data-ttu-id="303f5-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="303f5-125">RELATED LINKS</span></span>
