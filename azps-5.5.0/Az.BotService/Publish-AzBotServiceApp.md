---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/publish-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
ms.openlocfilehash: 4ef38ab40f90024124f7d5f09f1a55c16520dd6b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168076"
---
# <span data-ttu-id="b4ef9-101">Publish-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="b4ef9-101">Publish-AzBotServiceApp</span></span>

## <span data-ttu-id="b4ef9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4ef9-102">SYNOPSIS</span></span>
<span data-ttu-id="b4ef9-103">Gibt einen BotService zurück, der von den Parametern angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b4ef9-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="b4ef9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4ef9-104">SYNTAX</span></span>

```
Publish-AzBotServiceApp -CodeDir <String> -Name <String> -ResourceGroupName <String> [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="b4ef9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b4ef9-105">DESCRIPTION</span></span>
<span data-ttu-id="b4ef9-106">Gibt einen BotService zurück, der von den Parametern angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b4ef9-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="b4ef9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b4ef9-107">EXAMPLES</span></span>

### <span data-ttu-id="b4ef9-108">Beispiel 1: Veröffentlichen von BotService in Azure</span><span class="sxs-lookup"><span data-stu-id="b4ef9-108">Example 1: Publish your BotService to Azure</span></span>
```powershell
PS C:\> Publish-AzBotServiceApp -ResourceGroupName youriBotTest -CodeDir D:\zips\MyEchoBot -Name youriechobottest

```

<span data-ttu-id="b4ef9-109">Veröffentlichen von BotService in Azure nach Code</span><span class="sxs-lookup"><span data-stu-id="b4ef9-109">Publish your BotService to Azure by code</span></span>

## <span data-ttu-id="b4ef9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4ef9-110">PARAMETERS</span></span>

### <span data-ttu-id="b4ef9-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="b4ef9-111">-CodeDir</span></span>
<span data-ttu-id="b4ef9-112">Dieser Parameter definiert den Pfad der</span><span class="sxs-lookup"><span data-stu-id="b4ef9-112">This parameter defines the Path of the ZIP</span></span>

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

### <span data-ttu-id="b4ef9-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b4ef9-113">-Name</span></span>
<span data-ttu-id="b4ef9-114">Dieser Parameter definiert den Namen des Bots.</span><span class="sxs-lookup"><span data-stu-id="b4ef9-114">This parameter defines the name of the bot.</span></span>

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

### <span data-ttu-id="b4ef9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4ef9-115">-ResourceGroupName</span></span>
<span data-ttu-id="b4ef9-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4ef9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4ef9-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4ef9-117">-Confirm</span></span>
<span data-ttu-id="b4ef9-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b4ef9-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4ef9-119">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b4ef9-119">-WhatIf</span></span>
<span data-ttu-id="b4ef9-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b4ef9-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4ef9-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b4ef9-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4ef9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4ef9-122">CommonParameters</span></span>
<span data-ttu-id="b4ef9-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4ef9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4ef9-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4ef9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4ef9-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b4ef9-125">INPUTS</span></span>

## <span data-ttu-id="b4ef9-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b4ef9-126">OUTPUTS</span></span>

## <span data-ttu-id="b4ef9-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b4ef9-127">NOTES</span></span>

<span data-ttu-id="b4ef9-128">ALIASE</span><span class="sxs-lookup"><span data-stu-id="b4ef9-128">ALIASES</span></span>

## <span data-ttu-id="b4ef9-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b4ef9-129">RELATED LINKS</span></span>

