---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 6ea379b1ad1629dc0ba3e7d747256c86153c651d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504837"
---
# <span data-ttu-id="b46c6-101">New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="b46c6-101">New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="b46c6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b46c6-102">SYNOPSIS</span></span>
<span data-ttu-id="b46c6-103">Erstellt eine neue deaktivierte Regelgruppen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b46c6-103">Creates a new disabled rule group configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b46c6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b46c6-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String>
 [-Rules <System.Collections.Generic.List`1[System.Int32]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b46c6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b46c6-105">DESCRIPTION</span></span>
<span data-ttu-id="b46c6-106">Das Cmdlet **New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig** erstellt eine neue deaktivierte Regelgruppen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b46c6-106">The **New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="b46c6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b46c6-107">EXAMPLES</span></span>

### <span data-ttu-id="b46c6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b46c6-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="b46c6-109">Der Befehl erstellt eine neue deaktivierte Regelgruppen Konfiguration für die Regelgruppe mit dem Namen "Request-942-Application-Attack-SQLI" mit der Regel 942130 und der Regel 942140, die deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="b46c6-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="b46c6-110">Die Konfiguration der neuen deaktivierten Regelgruppe wird in $disabledRuleGroup 1 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b46c6-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="b46c6-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b46c6-111">PARAMETERS</span></span>

### <span data-ttu-id="b46c6-112">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="b46c6-112">-RuleGroupName</span></span>
<span data-ttu-id="b46c6-113">Der Name der Regelgruppe, die deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b46c6-113">The name of the rule group that will be disabled.</span></span>

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

### <span data-ttu-id="b46c6-114">-Regeln</span><span class="sxs-lookup"><span data-stu-id="b46c6-114">-Rules</span></span>
<span data-ttu-id="b46c6-115">Die Liste der Regeln, die deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="b46c6-115">The list of rules that will be disabled.</span></span>
<span data-ttu-id="b46c6-116">Ist NULL, werden alle Regeln der Regelgruppe deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b46c6-116">If null, all rules of the rule group will be disabled.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b46c6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b46c6-117">-DefaultProfile</span></span>
<span data-ttu-id="b46c6-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b46c6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b46c6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b46c6-119">CommonParameters</span></span>
<span data-ttu-id="b46c6-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b46c6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b46c6-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b46c6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b46c6-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b46c6-122">INPUTS</span></span>

### <span data-ttu-id="b46c6-123">Keine</span><span class="sxs-lookup"><span data-stu-id="b46c6-123">None</span></span>

## <span data-ttu-id="b46c6-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b46c6-124">OUTPUTS</span></span>

### <span data-ttu-id="b46c6-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="b46c6-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="b46c6-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="b46c6-126">NOTES</span></span>

## <span data-ttu-id="b46c6-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b46c6-127">RELATED LINKS</span></span>

[<span data-ttu-id="b46c6-128">Neu – AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="b46c6-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="b46c6-129">Satz-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="b46c6-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

