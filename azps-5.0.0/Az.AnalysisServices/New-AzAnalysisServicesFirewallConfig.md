---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
ms.openlocfilehash: 056a6e006cc0b1b3fd703757dcc07cbb0a8be987
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302266"
---
# <span data-ttu-id="f786a-101">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="f786a-101">New-AzAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="f786a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f786a-102">SYNOPSIS</span></span>
<span data-ttu-id="f786a-103">Erstellt eine neue Analysis Services-Firewall-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="f786a-103">Creates a new Analysis Services firewall config</span></span> 

## <span data-ttu-id="f786a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f786a-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallConfig [-EnablePowerBIService]
 [-FirewallRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f786a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f786a-105">DESCRIPTION</span></span>
<span data-ttu-id="f786a-106">Das New-AzAnalysisServicesFirewallConfig erstellt ein neues Firewall-Konfigurationsobjekt</span><span class="sxs-lookup"><span data-stu-id="f786a-106">The New-AzAnalysisServicesFirewallConfig creates a new firewall config object</span></span>

## <span data-ttu-id="f786a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f786a-107">EXAMPLES</span></span>

### <span data-ttu-id="f786a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f786a-108">Example 1</span></span>
```
PS C:\> $rule1 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> $config = New-AzAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRule $rule1,$rule2
```

<span data-ttu-id="f786a-109">Erstellt ein Firewall-Konfigurationsobjekt mit zwei Regeln, während gleichzeitig der Zugriff über den Power BI-Dienst aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="f786a-109">Creates a firewall config object with two rules while also enabling access from Power BI service.</span></span>

## <span data-ttu-id="f786a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f786a-110">PARAMETERS</span></span>

### <span data-ttu-id="f786a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f786a-111">-DefaultProfile</span></span>
<span data-ttu-id="f786a-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f786a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f786a-113">-EnablePowerBIService</span><span class="sxs-lookup"><span data-stu-id="f786a-113">-EnablePowerBIService</span></span>
<span data-ttu-id="f786a-114">Eine Kennzeichnung, die angibt, ob die Firewall Zugriff von Power BI zulässt</span><span class="sxs-lookup"><span data-stu-id="f786a-114">A flag to indicate if the firewall is allowing access from Power BI</span></span>

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

### <span data-ttu-id="f786a-115">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="f786a-115">-FirewallRule</span></span>
<span data-ttu-id="f786a-116">Eine Liste der Firewallregeln</span><span class="sxs-lookup"><span data-stu-id="f786a-116">A list of firewall rules</span></span>

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

### <span data-ttu-id="f786a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f786a-117">CommonParameters</span></span>
<span data-ttu-id="f786a-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f786a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f786a-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f786a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f786a-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f786a-120">INPUTS</span></span>

### <span data-ttu-id="f786a-121">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallRule, Microsoft. Azure. PowerShell. Cmdlets. AnalysisServices, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f786a-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule, Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f786a-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f786a-122">OUTPUTS</span></span>

### <span data-ttu-id="f786a-123">Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="f786a-123">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="f786a-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="f786a-124">NOTES</span></span>

## <span data-ttu-id="f786a-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f786a-125">RELATED LINKS</span></span>

[<span data-ttu-id="f786a-126">Neu – AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f786a-126">New-AzAnalysisServicesFirewallRule</span></span>](./New-AzAnalysisServicesFirewallRule.md)