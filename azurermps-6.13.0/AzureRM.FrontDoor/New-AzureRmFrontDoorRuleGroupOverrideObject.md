---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRuleGroupOverrideObject.md
ms.openlocfilehash: 02253a59a7f05bfdecd8147325575605334f13ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476058"
---
# <span data-ttu-id="f95c7-101">New-AzureRmFrontDoorRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="f95c7-101">New-AzureRmFrontDoorRuleGroupOverrideObject</span></span>

## <span data-ttu-id="f95c7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f95c7-102">SYNOPSIS</span></span>
<span data-ttu-id="f95c7-103">Erstellen eines RuleGroupOverride-Objekts für die WAF-Richtlinienerstellung</span><span class="sxs-lookup"><span data-stu-id="f95c7-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f95c7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f95c7-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorRuleGroupOverrideObject -Override <PSRuleGroupOverride> -Action <PSAction>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f95c7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f95c7-105">DESCRIPTION</span></span>
<span data-ttu-id="f95c7-106">Erstellen eines RuleGroupOverride-Objekts für die WAF-Richtlinienerstellung</span><span class="sxs-lookup"><span data-stu-id="f95c7-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="f95c7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f95c7-107">EXAMPLES</span></span>

### <span data-ttu-id="f95c7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f95c7-108">Example 1</span></span>
```powershell
PS C:\>  New-AzureRmFrontDoorRuleGroupOverrideObject -Override SqlInjection -Action Block

Action RuleGroupOverride
------ -----------------
 Block      SqlInjection
```

<span data-ttu-id="f95c7-109">Erstellen eines RuleGroupOverride-Objekts</span><span class="sxs-lookup"><span data-stu-id="f95c7-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="f95c7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f95c7-110">PARAMETERS</span></span>

### <span data-ttu-id="f95c7-111">– Aktion</span><span class="sxs-lookup"><span data-stu-id="f95c7-111">-Action</span></span>
<span data-ttu-id="f95c7-112">Art der Aktionen.</span><span class="sxs-lookup"><span data-stu-id="f95c7-112">Type of Actions.</span></span>
<span data-ttu-id="f95c7-113">Mögliche Werte sind: ' allow ', ' Block ', ' log '</span><span class="sxs-lookup"><span data-stu-id="f95c7-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f95c7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f95c7-114">-DefaultProfile</span></span>
<span data-ttu-id="f95c7-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f95c7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f95c7-116">-Override</span><span class="sxs-lookup"><span data-stu-id="f95c7-116">-Override</span></span>
<span data-ttu-id="f95c7-117">Beschreibt overrideruleGroup.</span><span class="sxs-lookup"><span data-stu-id="f95c7-117">Describes overrideruleGroup.</span></span>
<span data-ttu-id="f95c7-118">Mögliche Werte sind: "sqlinjection", "XSS"</span><span class="sxs-lookup"><span data-stu-id="f95c7-118">Possible values include: 'SqlInjection', 'XSS'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRuleGroupOverride
Parameter Sets: (All)
Aliases:
Accepted values: SqlInjection, XSS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f95c7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f95c7-119">CommonParameters</span></span>
<span data-ttu-id="f95c7-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f95c7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f95c7-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f95c7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f95c7-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f95c7-122">INPUTS</span></span>

### <span data-ttu-id="f95c7-123">Keine</span><span class="sxs-lookup"><span data-stu-id="f95c7-123">None</span></span>

## <span data-ttu-id="f95c7-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f95c7-124">OUTPUTS</span></span>

### <span data-ttu-id="f95c7-125">Microsoft. Azure. Commands. Haustür. Models. PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="f95c7-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="f95c7-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="f95c7-126">NOTES</span></span>

## <span data-ttu-id="f95c7-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f95c7-127">RELATED LINKS</span></span>

[<span data-ttu-id="f95c7-128">Neu – AzureRmFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="f95c7-128">New-AzureRmFrontDoorManagedRuleObject</span></span>](./New-AzureRmFrontDoorManagedRuleObject.md)
