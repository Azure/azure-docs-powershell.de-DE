---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/export-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Export-AzBotServiceApp.md
ms.openlocfilehash: dd922730f03b715924a69219c0b1f1ccb11534de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168089"
---
# <span data-ttu-id="53eac-101">Export-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="53eac-101">Export-AzBotServiceApp</span></span>

## <span data-ttu-id="53eac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53eac-102">SYNOPSIS</span></span>
<span data-ttu-id="53eac-103">Gibt einen BotService zurück, der von den Parametern angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="53eac-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="53eac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53eac-104">SYNTAX</span></span>

```
Export-AzBotServiceApp [-Name <String>] [-ResourceGroupName <String>] [-SavePath <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="53eac-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="53eac-105">DESCRIPTION</span></span>
<span data-ttu-id="53eac-106">Gibt einen BotService zurück, der von den Parametern angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="53eac-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="53eac-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="53eac-107">EXAMPLES</span></span>

### <span data-ttu-id="53eac-108">Beispiel 1: Laden Sie den Ordner "BotService-App" herunter.</span><span class="sxs-lookup"><span data-stu-id="53eac-108">Example 1: DownLoad the BotService App folder</span></span>
```powershell
PS C:\> Export-AzBotServiceApp -ResourceGroupName youriBotTest -name youriechobottest

Parameter $SavePath not provided, defaulting to current working directory.

    Directory: D:\powershell\BotService\azure-powershell\src\BotService

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d----          2020/12/15    13:45                youriechobottest
```

<span data-ttu-id="53eac-109">Laden Sie den Ordner "BotService-App" herunter.</span><span class="sxs-lookup"><span data-stu-id="53eac-109">DownLoad the BotService App folder</span></span>

## <span data-ttu-id="53eac-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53eac-110">PARAMETERS</span></span>

### <span data-ttu-id="53eac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53eac-111">-DefaultProfile</span></span>
<span data-ttu-id="53eac-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="53eac-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53eac-113">-Name</span><span class="sxs-lookup"><span data-stu-id="53eac-113">-Name</span></span>
<span data-ttu-id="53eac-114">Der Name der Bot-Ressource.</span><span class="sxs-lookup"><span data-stu-id="53eac-114">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="53eac-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53eac-115">-ResourceGroupName</span></span>
<span data-ttu-id="53eac-116">Der Name der Ressourcengruppe "Bot" im Benutzerabonnement.</span><span class="sxs-lookup"><span data-stu-id="53eac-116">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="53eac-117">-SavePath</span><span class="sxs-lookup"><span data-stu-id="53eac-117">-SavePath</span></span>


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

### <span data-ttu-id="53eac-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="53eac-118">-SubscriptionId</span></span>
<span data-ttu-id="53eac-119">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="53eac-119">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="53eac-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53eac-120">CommonParameters</span></span>
<span data-ttu-id="53eac-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53eac-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53eac-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53eac-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53eac-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="53eac-123">INPUTS</span></span>

## <span data-ttu-id="53eac-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="53eac-124">OUTPUTS</span></span>

### <span data-ttu-id="53eac-125">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="53eac-125">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="53eac-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="53eac-126">NOTES</span></span>

<span data-ttu-id="53eac-127">ALIASE</span><span class="sxs-lookup"><span data-stu-id="53eac-127">ALIASES</span></span>

## <span data-ttu-id="53eac-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="53eac-128">RELATED LINKS</span></span>

