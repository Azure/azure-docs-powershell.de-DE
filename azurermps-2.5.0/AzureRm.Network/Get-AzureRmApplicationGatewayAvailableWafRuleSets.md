---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablewafrulesets
schema: 2.0.0
ms.openlocfilehash: 83ee8e673271079690c24691f22badfe5193ba50
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849251"
---
# <span data-ttu-id="698b2-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span><span class="sxs-lookup"><span data-stu-id="698b2-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span></span>

## <span data-ttu-id="698b2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="698b2-102">SYNOPSIS</span></span>
<span data-ttu-id="698b2-103">Ruft alle verfügbaren Webanwendungs-Firewallregel-Regelsätze ab.</span><span class="sxs-lookup"><span data-stu-id="698b2-103">Gets all available web application firewall rule sets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="698b2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="698b2-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableWafRuleSets [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="698b2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="698b2-105">DESCRIPTION</span></span>
<span data-ttu-id="698b2-106">Das Cmdlet " **Get-AzureRmApplicationGatewayAvailableWafRuleSets** " ruft alle verfügbaren Firewall-Regelsätze für Webanwendungen ab.</span><span class="sxs-lookup"><span data-stu-id="698b2-106">The **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="698b2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="698b2-107">EXAMPLES</span></span>

### <span data-ttu-id="698b2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="698b2-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzureRmApplicationGatewayAvailableWafRuleSets
```

<span data-ttu-id="698b2-109">Diese Befehle gibt alle verfügbaren Firewall-Regelsätze für Webanwendungen zurück.</span><span class="sxs-lookup"><span data-stu-id="698b2-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="698b2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="698b2-110">PARAMETERS</span></span>

### <span data-ttu-id="698b2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="698b2-111">-DefaultProfile</span></span>
<span data-ttu-id="698b2-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="698b2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="698b2-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="698b2-113">CommonParameters</span></span>
<span data-ttu-id="698b2-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="698b2-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="698b2-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="698b2-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="698b2-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="698b2-116">INPUTS</span></span>

### <span data-ttu-id="698b2-117">Keine</span><span class="sxs-lookup"><span data-stu-id="698b2-117">None</span></span>

## <span data-ttu-id="698b2-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="698b2-118">OUTPUTS</span></span>

### <span data-ttu-id="698b2-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="698b2-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="698b2-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="698b2-120">NOTES</span></span>
<span data-ttu-id="698b2-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** ist ein Alias für das Cmdlet **Get-AzureRmApplicationGatewayAvailableWafRuleSets** .</span><span class="sxs-lookup"><span data-stu-id="698b2-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet.</span></span>

## <span data-ttu-id="698b2-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="698b2-122">RELATED LINKS</span></span>

