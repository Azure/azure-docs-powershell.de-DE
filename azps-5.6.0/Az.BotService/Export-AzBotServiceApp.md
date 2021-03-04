---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/export-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
ms.openlocfilehash: 79ef8a92997790f547847e05eae6ca101016bc42
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923051"
---
# <span data-ttu-id="9afd2-101">Export-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="9afd2-101">Export-AzBotServiceApp</span></span>

## <span data-ttu-id="9afd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9afd2-102">SYNOPSIS</span></span>
<span data-ttu-id="9afd2-103">Gibt einen botService zurück, der von den Parametern angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9afd2-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="9afd2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9afd2-104">SYNTAX</span></span>

```
Export-AzBotServiceApp [-Name <String>] [-ResourceGroupName <String>] [-SavePath <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9afd2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9afd2-105">DESCRIPTION</span></span>
<span data-ttu-id="9afd2-106">Gibt einen botService zurück, der von den Parametern angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9afd2-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="9afd2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9afd2-107">EXAMPLES</span></span>

### <span data-ttu-id="9afd2-108">Beispiel 1: Herunterladen des BotService-App-Ordners</span><span class="sxs-lookup"><span data-stu-id="9afd2-108">Example 1: DownLoad the BotService App folder</span></span>
```powershell
PS C:\> Export-AzBotServiceApp -ResourceGroupName youriBotTest -name youriechobottest

Parameter $SavePath not provided, defaulting to current working directory.

    Directory: D:\powershell\BotService\azure-powershell\src\BotService

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d----          2020/12/15    13:45                youriechobottest
```

<span data-ttu-id="9afd2-109">Herunterladen des Ordners BotService App</span><span class="sxs-lookup"><span data-stu-id="9afd2-109">DownLoad the BotService App folder</span></span>

## <span data-ttu-id="9afd2-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9afd2-110">PARAMETERS</span></span>

### <span data-ttu-id="9afd2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9afd2-111">-DefaultProfile</span></span>
<span data-ttu-id="9afd2-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9afd2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9afd2-113">-Name</span><span class="sxs-lookup"><span data-stu-id="9afd2-113">-Name</span></span>
<span data-ttu-id="9afd2-114">Der Name der Bot-Ressource.</span><span class="sxs-lookup"><span data-stu-id="9afd2-114">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9afd2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9afd2-115">-ResourceGroupName</span></span>
<span data-ttu-id="9afd2-116">Der Name der Bot-Ressourcengruppe im Benutzerabonnement.</span><span class="sxs-lookup"><span data-stu-id="9afd2-116">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="9afd2-117">-SavePath</span><span class="sxs-lookup"><span data-stu-id="9afd2-117">-SavePath</span></span>


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

### <span data-ttu-id="9afd2-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9afd2-118">-SubscriptionId</span></span>
<span data-ttu-id="9afd2-119">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="9afd2-119">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="9afd2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9afd2-120">CommonParameters</span></span>
<span data-ttu-id="9afd2-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9afd2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9afd2-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9afd2-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9afd2-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9afd2-123">INPUTS</span></span>

## <span data-ttu-id="9afd2-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9afd2-124">OUTPUTS</span></span>

### <span data-ttu-id="9afd2-125">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="9afd2-125">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="9afd2-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9afd2-126">NOTES</span></span>

<span data-ttu-id="9afd2-127">ALIASE</span><span class="sxs-lookup"><span data-stu-id="9afd2-127">ALIASES</span></span>

## <span data-ttu-id="9afd2-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9afd2-128">RELATED LINKS</span></span>

