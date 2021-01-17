---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/export-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
ms.openlocfilehash: dd922730f03b715924a69219c0b1f1ccb11534de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473220"
---
# <span data-ttu-id="a3387-101">Export-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="a3387-101">Export-AzBotServiceApp</span></span>

## <span data-ttu-id="a3387-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3387-102">SYNOPSIS</span></span>
<span data-ttu-id="a3387-103">Gibt einen BotService zurück, der von den Parametern angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a3387-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="a3387-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3387-104">SYNTAX</span></span>

```
Export-AzBotServiceApp [-Name <String>] [-ResourceGroupName <String>] [-SavePath <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a3387-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3387-105">DESCRIPTION</span></span>
<span data-ttu-id="a3387-106">Gibt einen BotService zurück, der von den Parametern angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a3387-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="a3387-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a3387-107">EXAMPLES</span></span>

### <span data-ttu-id="a3387-108">Beispiel 1: Laden Sie den Ordner "BotService-App" herunter.</span><span class="sxs-lookup"><span data-stu-id="a3387-108">Example 1: DownLoad the BotService App folder</span></span>
```powershell
PS C:\> Export-AzBotServiceApp -ResourceGroupName youriBotTest -name youriechobottest

Parameter $SavePath not provided, defaulting to current working directory.

    Directory: D:\powershell\BotService\azure-powershell\src\BotService

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d----          2020/12/15    13:45                youriechobottest
```

<span data-ttu-id="a3387-109">Laden Sie den Ordner "BotService-App" herunter.</span><span class="sxs-lookup"><span data-stu-id="a3387-109">DownLoad the BotService App folder</span></span>

## <span data-ttu-id="a3387-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3387-110">PARAMETERS</span></span>

### <span data-ttu-id="a3387-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3387-111">-DefaultProfile</span></span>
<span data-ttu-id="a3387-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3387-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3387-113">-Name</span><span class="sxs-lookup"><span data-stu-id="a3387-113">-Name</span></span>
<span data-ttu-id="a3387-114">Der Name der Bot-Ressource.</span><span class="sxs-lookup"><span data-stu-id="a3387-114">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="a3387-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3387-115">-ResourceGroupName</span></span>
<span data-ttu-id="a3387-116">Der Name der Ressourcengruppe "Bot" im Benutzerabonnement.</span><span class="sxs-lookup"><span data-stu-id="a3387-116">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="a3387-117">-SavePath</span><span class="sxs-lookup"><span data-stu-id="a3387-117">-SavePath</span></span>


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

### <span data-ttu-id="a3387-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a3387-118">-SubscriptionId</span></span>
<span data-ttu-id="a3387-119">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="a3387-119">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="a3387-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3387-120">CommonParameters</span></span>
<span data-ttu-id="a3387-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3387-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3387-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3387-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3387-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a3387-123">INPUTS</span></span>

## <span data-ttu-id="a3387-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a3387-124">OUTPUTS</span></span>

### <span data-ttu-id="a3387-125">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="a3387-125">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="a3387-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a3387-126">NOTES</span></span>

<span data-ttu-id="a3387-127">ALIASE</span><span class="sxs-lookup"><span data-stu-id="a3387-127">ALIASES</span></span>

## <span data-ttu-id="a3387-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a3387-128">RELATED LINKS</span></span>

