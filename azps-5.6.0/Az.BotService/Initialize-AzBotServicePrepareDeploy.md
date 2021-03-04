---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/initialize-azbotservicepreparedeploy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
ms.openlocfilehash: 118fce3e75ee7ba66fa30e6e07cfce16e5dadcff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947267"
---
# <span data-ttu-id="29f8d-101">Initialize-AzBotServicePrepareDeploy</span><span class="sxs-lookup"><span data-stu-id="29f8d-101">Initialize-AzBotServicePrepareDeploy</span></span>

## <span data-ttu-id="29f8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29f8d-102">SYNOPSIS</span></span>
<span data-ttu-id="29f8d-103">Gibt einen botService zurück, der von den Parametern angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="29f8d-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="29f8d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29f8d-104">SYNTAX</span></span>

```
Initialize-AzBotServicePrepareDeploy [-CodeDir <String>] [-Language <String>] [-ProjFileName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="29f8d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29f8d-105">DESCRIPTION</span></span>
<span data-ttu-id="29f8d-106">Gibt einen botService zurück, der von den Parametern angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="29f8d-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="29f8d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="29f8d-107">EXAMPLES</span></span>

### <span data-ttu-id="29f8d-108">Beispiel 1: Initialisieren des Projektdateiordners</span><span class="sxs-lookup"><span data-stu-id="29f8d-108">Example 1: Initialize the Project FileFolder</span></span>
```powershell
PS C:\> Initialize-AzBotServicePrepareDeploy -CodeDir D:\zips\MyEchoBot -ProjFileName MyEchoBot.csproj

```

<span data-ttu-id="29f8d-109">Initialisieren Bereitet eine Ressource für die Verwendung vor und legt sie auf einen Standardzustand fest.</span><span class="sxs-lookup"><span data-stu-id="29f8d-109">Initialize Prepares a resource for use, and sets it to a default state</span></span>

## <span data-ttu-id="29f8d-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="29f8d-110">PARAMETERS</span></span>

### <span data-ttu-id="29f8d-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="29f8d-111">-CodeDir</span></span>
<span data-ttu-id="29f8d-112">Der Name der Bot-Ressourcengruppe im Benutzerabonnement.</span><span class="sxs-lookup"><span data-stu-id="29f8d-112">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="29f8d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29f8d-113">-DefaultProfile</span></span>
<span data-ttu-id="29f8d-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="29f8d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f8d-115">-Sprache</span><span class="sxs-lookup"><span data-stu-id="29f8d-115">-Language</span></span>


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

### <span data-ttu-id="29f8d-116">-ProjFileName</span><span class="sxs-lookup"><span data-stu-id="29f8d-116">-ProjFileName</span></span>


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

### <span data-ttu-id="29f8d-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="29f8d-117">-SubscriptionId</span></span>
<span data-ttu-id="29f8d-118">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="29f8d-118">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f8d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29f8d-119">CommonParameters</span></span>
<span data-ttu-id="29f8d-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29f8d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29f8d-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29f8d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29f8d-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="29f8d-122">INPUTS</span></span>

## <span data-ttu-id="29f8d-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="29f8d-123">OUTPUTS</span></span>

### <span data-ttu-id="29f8d-124">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="29f8d-124">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="29f8d-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="29f8d-125">NOTES</span></span>

<span data-ttu-id="29f8d-126">ALIASE</span><span class="sxs-lookup"><span data-stu-id="29f8d-126">ALIASES</span></span>

## <span data-ttu-id="29f8d-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="29f8d-127">RELATED LINKS</span></span>

