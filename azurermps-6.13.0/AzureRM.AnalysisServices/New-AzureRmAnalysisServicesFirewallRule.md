---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
ms.openlocfilehash: 2a47c97ea189d4064edae7a871e21465d866f1f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482613"
---
# <span data-ttu-id="0df04-101">New-AzureRmAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0df04-101">New-AzureRmAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="0df04-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0df04-102">SYNOPSIS</span></span>
<span data-ttu-id="0df04-103">Erstellt eine neue Analysis Services-Firewallregel</span><span class="sxs-lookup"><span data-stu-id="0df04-103">Creates a new Analysis Services firewall rule</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0df04-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0df04-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String>
 [-RangeEnd] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0df04-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0df04-105">DESCRIPTION</span></span>
<span data-ttu-id="0df04-106">Das New-AzureRmAnalysisServicesFirewallRule erstellt ein neues Firewallregel-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0df04-106">The New-AzureRmAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="0df04-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0df04-107">EXAMPLES</span></span>

### <span data-ttu-id="0df04-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0df04-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="0df04-109">Erstellt eine Firewallregel mit dem Namen "rule1" mit dem Anfangsbereich 0.0.0.0 und dem Endbereich 255.255.255.255</span><span class="sxs-lookup"><span data-stu-id="0df04-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="0df04-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0df04-110">PARAMETERS</span></span>

### <span data-ttu-id="0df04-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0df04-111">-DefaultProfile</span></span>
<span data-ttu-id="0df04-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0df04-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0df04-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="0df04-113">-FirewallRuleName</span></span>
<span data-ttu-id="0df04-114">Name der Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="0df04-114">Name of firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0df04-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="0df04-115">-RangeEnd</span></span>
<span data-ttu-id="0df04-116">Das Bereichsende einer Firewallregel</span><span class="sxs-lookup"><span data-stu-id="0df04-116">The range end of a firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0df04-117">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="0df04-117">-RangeStart</span></span>
<span data-ttu-id="0df04-118">Der Bereichsanfang einer Firewallregel</span><span class="sxs-lookup"><span data-stu-id="0df04-118">The range start of a firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0df04-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0df04-119">CommonParameters</span></span>
<span data-ttu-id="0df04-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0df04-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0df04-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0df04-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0df04-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0df04-122">INPUTS</span></span>

### <span data-ttu-id="0df04-123">System. String</span><span class="sxs-lookup"><span data-stu-id="0df04-123">System.String</span></span>

## <span data-ttu-id="0df04-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0df04-124">OUTPUTS</span></span>

### <span data-ttu-id="0df04-125">Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0df04-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="0df04-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="0df04-126">NOTES</span></span>

## <span data-ttu-id="0df04-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0df04-127">RELATED LINKS</span></span>

[<span data-ttu-id="0df04-128">Neu – AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="0df04-128">New-AzureRmAnalysisServicesFirewallConfig</span></span>](./New-AzureRmAnalysisServicesFirewallConfig.md)
