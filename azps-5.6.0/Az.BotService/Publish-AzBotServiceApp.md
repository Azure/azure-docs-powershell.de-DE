---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/publish-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
ms.openlocfilehash: 551428a1c5d1737d32aeddf2dd5653586d1dbfbd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925155"
---
# <span data-ttu-id="fafda-101">Publish-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="fafda-101">Publish-AzBotServiceApp</span></span>

## <span data-ttu-id="fafda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fafda-102">SYNOPSIS</span></span>
<span data-ttu-id="fafda-103">Gibt einen botService zurück, der von den Parametern angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fafda-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="fafda-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fafda-104">SYNTAX</span></span>

```
Publish-AzBotServiceApp -CodeDir <String> -Name <String> -ResourceGroupName <String> [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="fafda-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fafda-105">DESCRIPTION</span></span>
<span data-ttu-id="fafda-106">Gibt einen botService zurück, der von den Parametern angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fafda-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="fafda-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fafda-107">EXAMPLES</span></span>

### <span data-ttu-id="fafda-108">Beispiel 1: Veröffentlichen ihres BotService in Azure</span><span class="sxs-lookup"><span data-stu-id="fafda-108">Example 1: Publish your BotService to Azure</span></span>
```powershell
PS C:\> Publish-AzBotServiceApp -ResourceGroupName youriBotTest -CodeDir D:\zips\MyEchoBot -Name youriechobottest

```

<span data-ttu-id="fafda-109">Veröffentlichen Ihres BotService in Azure nach Code</span><span class="sxs-lookup"><span data-stu-id="fafda-109">Publish your BotService to Azure by code</span></span>

## <span data-ttu-id="fafda-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fafda-110">PARAMETERS</span></span>

### <span data-ttu-id="fafda-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="fafda-111">-CodeDir</span></span>
<span data-ttu-id="fafda-112">Dieser Parameter definiert den Pfad der ZIP</span><span class="sxs-lookup"><span data-stu-id="fafda-112">This parameter defines the Path of the ZIP</span></span>

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

### <span data-ttu-id="fafda-113">-Name</span><span class="sxs-lookup"><span data-stu-id="fafda-113">-Name</span></span>
<span data-ttu-id="fafda-114">Dieser Parameter definiert den Namen des Bots.</span><span class="sxs-lookup"><span data-stu-id="fafda-114">This parameter defines the name of the bot.</span></span>

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

### <span data-ttu-id="fafda-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fafda-115">-ResourceGroupName</span></span>
<span data-ttu-id="fafda-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fafda-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fafda-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fafda-117">-Confirm</span></span>
<span data-ttu-id="fafda-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fafda-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fafda-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fafda-119">-WhatIf</span></span>
<span data-ttu-id="fafda-120">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fafda-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fafda-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fafda-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fafda-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fafda-122">CommonParameters</span></span>
<span data-ttu-id="fafda-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fafda-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fafda-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fafda-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fafda-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fafda-125">INPUTS</span></span>

## <span data-ttu-id="fafda-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fafda-126">OUTPUTS</span></span>

## <span data-ttu-id="fafda-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fafda-127">NOTES</span></span>

<span data-ttu-id="fafda-128">ALIASE</span><span class="sxs-lookup"><span data-stu-id="fafda-128">ALIASES</span></span>

## <span data-ttu-id="fafda-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fafda-129">RELATED LINKS</span></span>

