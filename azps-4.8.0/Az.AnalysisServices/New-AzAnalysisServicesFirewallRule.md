---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
ms.openlocfilehash: 9aecede69497bd1a8723720200ed73e12b4aa776
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010107"
---
# <span data-ttu-id="4e33f-101">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4e33f-101">New-AzAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="4e33f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4e33f-102">SYNOPSIS</span></span>
<span data-ttu-id="4e33f-103">Erstellt eine neue Analysis Services-Firewallregel</span><span class="sxs-lookup"><span data-stu-id="4e33f-103">Creates a new Analysis Services firewall rule</span></span>

## <span data-ttu-id="4e33f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e33f-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e33f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4e33f-105">DESCRIPTION</span></span>
<span data-ttu-id="4e33f-106">Das New-AzAnalysisServicesFirewallRule erstellt ein neues Firewallregel-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4e33f-106">The New-AzAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="4e33f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4e33f-107">EXAMPLES</span></span>

### <span data-ttu-id="4e33f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4e33f-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="4e33f-109">Erstellt eine Firewallregel mit dem Namen "rule1" mit dem Anfangsbereich 0.0.0.0 und dem Endbereich 255.255.255.255</span><span class="sxs-lookup"><span data-stu-id="4e33f-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="4e33f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e33f-110">PARAMETERS</span></span>

### <span data-ttu-id="4e33f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e33f-111">-DefaultProfile</span></span>
<span data-ttu-id="4e33f-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4e33f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e33f-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="4e33f-113">-FirewallRuleName</span></span>
<span data-ttu-id="4e33f-114">Name der Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="4e33f-114">Name of firewall rule</span></span>

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

### <span data-ttu-id="4e33f-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="4e33f-115">-RangeEnd</span></span>
<span data-ttu-id="4e33f-116">Das Bereichsende einer Firewallregel</span><span class="sxs-lookup"><span data-stu-id="4e33f-116">The range end of a firewall rule</span></span>

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

### <span data-ttu-id="4e33f-117">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="4e33f-117">-RangeStart</span></span>
<span data-ttu-id="4e33f-118">Der Bereichsanfang einer Firewallregel</span><span class="sxs-lookup"><span data-stu-id="4e33f-118">The range start of a firewall rule</span></span>

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

### <span data-ttu-id="4e33f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e33f-119">CommonParameters</span></span>
<span data-ttu-id="4e33f-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e33f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e33f-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e33f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e33f-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4e33f-122">INPUTS</span></span>

### <span data-ttu-id="4e33f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="4e33f-123">System.String</span></span>

## <span data-ttu-id="4e33f-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4e33f-124">OUTPUTS</span></span>

### <span data-ttu-id="4e33f-125">Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4e33f-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="4e33f-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="4e33f-126">NOTES</span></span>

## <span data-ttu-id="4e33f-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4e33f-127">RELATED LINKS</span></span>

[<span data-ttu-id="4e33f-128">Neu – AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="4e33f-128">New-AzAnalysisServicesFirewallConfig</span></span>](./New-AzAnalysisServicesFirewallConfig.md)