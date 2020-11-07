---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoormanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorManagedRuleObject.md
ms.openlocfilehash: 236cb9ff263f97ae52ea5d3226f4defec00c662a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663136"
---
# <span data-ttu-id="95f9d-101">New-AzureRmFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="95f9d-101">New-AzureRmFrontDoorManagedRuleObject</span></span>

## <span data-ttu-id="95f9d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="95f9d-102">SYNOPSIS</span></span>
<span data-ttu-id="95f9d-103">Erstellen eines ManagedRule-Objekts für die WAF-Richtlinienerstellung</span><span class="sxs-lookup"><span data-stu-id="95f9d-103">Create ManagedRule Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95f9d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="95f9d-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorManagedRuleObject -Priority <Int32> [-Version <String>]
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="95f9d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95f9d-105">DESCRIPTION</span></span>
<span data-ttu-id="95f9d-106">Erstellen eines ManagedRule-Objekts für die WAF-Richtlinienerstellung</span><span class="sxs-lookup"><span data-stu-id="95f9d-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="95f9d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="95f9d-107">EXAMPLES</span></span>

### <span data-ttu-id="95f9d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="95f9d-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoor
ManagedRuleObject -Priority 1 -Version 0 -RuleGroupOverride $override1

RuleGroupOverrides                                                   Priority Version
------------------                                                   -------- -------
{Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride}        1 0
```

<span data-ttu-id="95f9d-109">Erstellen eines ManagedRule-Objekts</span><span class="sxs-lookup"><span data-stu-id="95f9d-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="95f9d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="95f9d-110">PARAMETERS</span></span>

### <span data-ttu-id="95f9d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95f9d-111">-DefaultProfile</span></span>
<span data-ttu-id="95f9d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="95f9d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95f9d-113">-Priorität</span><span class="sxs-lookup"><span data-stu-id="95f9d-113">-Priority</span></span>
<span data-ttu-id="95f9d-114">Beschreibt die Priorität der Regel.</span><span class="sxs-lookup"><span data-stu-id="95f9d-114">Describes priority of the rule</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f9d-115">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="95f9d-115">-RuleGroupOverride</span></span>
<span data-ttu-id="95f9d-116">Liste der Überschreibung der Azure Managed Provider-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="95f9d-116">List of azure managed provider override configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f9d-117">-Version</span><span class="sxs-lookup"><span data-stu-id="95f9d-117">-Version</span></span>
<span data-ttu-id="95f9d-118">Version des RuleSet</span><span class="sxs-lookup"><span data-stu-id="95f9d-118">Version of the ruleset</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f9d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95f9d-119">CommonParameters</span></span>
<span data-ttu-id="95f9d-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95f9d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95f9d-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95f9d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95f9d-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="95f9d-122">INPUTS</span></span>

### <span data-ttu-id="95f9d-123">Keine</span><span class="sxs-lookup"><span data-stu-id="95f9d-123">None</span></span>

## <span data-ttu-id="95f9d-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="95f9d-124">OUTPUTS</span></span>

### <span data-ttu-id="95f9d-125">Microsoft. Azure. Commands. Haustür. Models. PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="95f9d-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="95f9d-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="95f9d-126">NOTES</span></span>

## <span data-ttu-id="95f9d-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="95f9d-127">RELATED LINKS</span></span>

<span data-ttu-id="95f9d-128">[Neu – AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Satz-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md) 
 [Neu – AzureRmFrontDoorRuleGroupOverrideObject](./Set-AzureRmFrontDoorRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="95f9d-128">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)
[New-AzureRmFrontDoorRuleGroupOverrideObject](./Set-AzureRmFrontDoorRuleGroupOverrideObject.md)</span></span>
