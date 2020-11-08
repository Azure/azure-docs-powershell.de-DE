---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
ms.openlocfilehash: 056a6e006cc0b1b3fd703757dcc07cbb0a8be987
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995883"
---
# <span data-ttu-id="28f90-101">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="28f90-101">New-AzAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="28f90-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="28f90-102">SYNOPSIS</span></span>
<span data-ttu-id="28f90-103">Erstellt eine neue Analysis Services-Firewall-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="28f90-103">Creates a new Analysis Services firewall config</span></span> 

## <span data-ttu-id="28f90-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="28f90-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallConfig [-EnablePowerBIService]
 [-FirewallRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28f90-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28f90-105">DESCRIPTION</span></span>
<span data-ttu-id="28f90-106">Das New-AzAnalysisServicesFirewallConfig erstellt ein neues Firewall-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="28f90-106">The New-AzAnalysisServicesFirewallConfig creates a new firewall config object</span></span>

## <span data-ttu-id="28f90-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="28f90-107">EXAMPLES</span></span>

### <span data-ttu-id="28f90-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="28f90-108">Example 1</span></span>
```
PS C:\> $rule1 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> $config = New-AzAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRule $rule1,$rule2
```

<span data-ttu-id="28f90-109">Erstellt ein Firewall-Konfigurationsobjekt mit zwei Regeln, während gleichzeitig der Zugriff über den Power BI-Dienst aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="28f90-109">Creates a firewall config object with two rules while also enabling access from Power BI service.</span></span>

## <span data-ttu-id="28f90-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="28f90-110">PARAMETERS</span></span>

### <span data-ttu-id="28f90-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28f90-111">-DefaultProfile</span></span>
<span data-ttu-id="28f90-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="28f90-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28f90-113">-EnablePowerBIService</span><span class="sxs-lookup"><span data-stu-id="28f90-113">-EnablePowerBIService</span></span>
<span data-ttu-id="28f90-114">Eine Kennzeichnung, die angibt, ob die Firewall Zugriff von Power BI zulässt</span><span class="sxs-lookup"><span data-stu-id="28f90-114">A flag to indicate if the firewall is allowing access from Power BI</span></span>

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

### <span data-ttu-id="28f90-115">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="28f90-115">-FirewallRule</span></span>
<span data-ttu-id="28f90-116">Eine Liste der Firewallregeln</span><span class="sxs-lookup"><span data-stu-id="28f90-116">A list of firewall rules</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28f90-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28f90-117">CommonParameters</span></span>
<span data-ttu-id="28f90-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28f90-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28f90-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28f90-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28f90-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="28f90-120">INPUTS</span></span>

### <span data-ttu-id="28f90-121">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallRule, Microsoft. Azure. PowerShell. Cmdlets. AnalysisServices, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="28f90-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule, Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="28f90-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="28f90-122">OUTPUTS</span></span>

### <span data-ttu-id="28f90-123">Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="28f90-123">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="28f90-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="28f90-124">NOTES</span></span>

## <span data-ttu-id="28f90-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="28f90-125">RELATED LINKS</span></span>

[<span data-ttu-id="28f90-126">Neu – AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="28f90-126">New-AzAnalysisServicesFirewallRule</span></span>](./New-AzAnalysisServicesFirewallRule.md)