---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallexclusionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
ms.openlocfilehash: 58060c488e778510822d9bc86a21de216447e0f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660621"
---
# <span data-ttu-id="d54b8-101">New-AzApplicationGatewayFirewallExclusionConfig</span><span class="sxs-lookup"><span data-stu-id="d54b8-101">New-AzApplicationGatewayFirewallExclusionConfig</span></span>

## <span data-ttu-id="d54b8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d54b8-102">SYNOPSIS</span></span>
<span data-ttu-id="d54b8-103">Erstellt eine neue Ausschlussregel Liste für Application Gateway WAF</span><span class="sxs-lookup"><span data-stu-id="d54b8-103">Creates a new exclusion rule list for application gateway waf</span></span>

## <span data-ttu-id="d54b8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d54b8-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallExclusionConfig -Variable <String> -Operator <String> -Selector <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d54b8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d54b8-105">DESCRIPTION</span></span>
<span data-ttu-id="d54b8-106">Das Cmdlet **New-AzApplicationGatewayFirewallExclusionConfig** eine neue Ausschlussregel Liste für Application Gateway WAF.</span><span class="sxs-lookup"><span data-stu-id="d54b8-106">The **New-AzApplicationGatewayFirewallExclusionConfig** cmdlet a new exclusion rule list for application gateway waf.</span></span>

## <span data-ttu-id="d54b8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d54b8-107">EXAMPLES</span></span>

### <span data-ttu-id="d54b8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d54b8-108">Example 1</span></span>
```powershell
PS C:\> $exclusion1 = New-AzApplicationGatewayFirewallExclusionConfig -Variable "RequestHeaderNames" -Operator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="d54b8-109">Mit diesem Befehl wird eine neue Ausschlussregel Listen-Konfiguration für die Variable mit dem Namen RequestHeaderNames und dem Operator mit dem Namen StartsWith und der Auswahl mit dem Namen XYZ erstellt.</span><span class="sxs-lookup"><span data-stu-id="d54b8-109">This command creates a new exclusion rule lists configuration for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="d54b8-110">Die Konfiguration der Ausschlussliste wird in $Exclusion 1 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d54b8-110">The exclusion list configuration is saved in $exclusion1.</span></span>

## <span data-ttu-id="d54b8-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d54b8-111">PARAMETERS</span></span>

### <span data-ttu-id="d54b8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d54b8-112">-DefaultProfile</span></span>
<span data-ttu-id="d54b8-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d54b8-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d54b8-114">-Operator</span><span class="sxs-lookup"><span data-stu-id="d54b8-114">-Operator</span></span>
<span data-ttu-id="d54b8-115">Wenn Variable eine Sammlung ist, verwenden Sie die Auswahl, um anzugeben, für welche Elemente in der Sammlung dieser Ausschluss gilt.</span><span class="sxs-lookup"><span data-stu-id="d54b8-115">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="d54b8-116">-Auswahl</span><span class="sxs-lookup"><span data-stu-id="d54b8-116">-Selector</span></span>
<span data-ttu-id="d54b8-117">Wenn Variable eine Auflistung ist, wird mit dem Operator angegeben, für welche Elemente in der Sammlung dieser Ausschluss gilt.</span><span class="sxs-lookup"><span data-stu-id="d54b8-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="d54b8-118">-Variable</span><span class="sxs-lookup"><span data-stu-id="d54b8-118">-Variable</span></span>
<span data-ttu-id="d54b8-119">Die Variable, die ausgeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d54b8-119">The variable to be excluded.</span></span>

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

### <span data-ttu-id="d54b8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d54b8-120">CommonParameters</span></span>
<span data-ttu-id="d54b8-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d54b8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d54b8-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d54b8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d54b8-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d54b8-123">INPUTS</span></span>

### <span data-ttu-id="d54b8-124">Keine</span><span class="sxs-lookup"><span data-stu-id="d54b8-124">None</span></span>

## <span data-ttu-id="d54b8-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d54b8-125">OUTPUTS</span></span>

### <span data-ttu-id="d54b8-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallExclusion</span><span class="sxs-lookup"><span data-stu-id="d54b8-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span></span>

## <span data-ttu-id="d54b8-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="d54b8-127">NOTES</span></span>

## <span data-ttu-id="d54b8-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d54b8-128">RELATED LINKS</span></span>
