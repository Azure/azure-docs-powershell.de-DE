---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azscheduledqueryruleaznsactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
ms.openlocfilehash: b5bfac31babfd4bc848f9619dc8eb8cecd1c3eaa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949064"
---
# <span data-ttu-id="05135-101">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="05135-101">New-AzScheduledQueryRuleAznsActionGroup</span></span>

## <span data-ttu-id="05135-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05135-102">SYNOPSIS</span></span>
<span data-ttu-id="05135-103">Erstellt ein Objekt vom Typ Azns Action Group</span><span class="sxs-lookup"><span data-stu-id="05135-103">Creates an object of type Azns Action Group</span></span>

## <span data-ttu-id="05135-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="05135-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAznsActionGroup [-ActionGroup <String[]>] [-EmailSubject <String>]
 [-CustomWebhookPayload <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05135-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="05135-105">DESCRIPTION</span></span>
<span data-ttu-id="05135-106">Erstellt ein Objekt vom Typ Azns Action Group.</span><span class="sxs-lookup"><span data-stu-id="05135-106">Creates an object of type Azns Action Group.</span></span>
<span data-ttu-id="05135-107">Dieses Objekt muss an den Befehl übergeben werden, mit dem die Protokollbenachrichtigungsregel erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="05135-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="05135-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="05135-108">EXAMPLES</span></span>

### <span data-ttu-id="05135-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="05135-109">Example 1</span></span>
```powershell
PS C:\> $aznsActionGroup = New-AzScheduledQueryRuleAznsActionGroup -ActionGroup @("/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourcegroups/MyResourceGroup/providers/microsoft.insights/actiongroups/MyActionGroup") -EmailSubject "Email subject" -CustomWebhookPayload "{}"
```

## <span data-ttu-id="05135-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="05135-110">PARAMETERS</span></span>

### <span data-ttu-id="05135-111">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="05135-111">-ActionGroup</span></span>
<span data-ttu-id="05135-112">Die Liste der Aktionsgruppen, an die eine Benachrichtigung gesendet werden soll</span><span class="sxs-lookup"><span data-stu-id="05135-112">The list of action groups to send notification to</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05135-113">-CustomWebhookPayload</span><span class="sxs-lookup"><span data-stu-id="05135-113">-CustomWebhookPayload</span></span>
<span data-ttu-id="05135-114">Die angepasste Webhooknutzlast</span><span class="sxs-lookup"><span data-stu-id="05135-114">The customized webhook payload</span></span>

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

### <span data-ttu-id="05135-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05135-115">-DefaultProfile</span></span>
<span data-ttu-id="05135-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="05135-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05135-117">-EmailSubject</span><span class="sxs-lookup"><span data-stu-id="05135-117">-EmailSubject</span></span>
<span data-ttu-id="05135-118">Der Betreff einer Benachrichtigung per E-Mail</span><span class="sxs-lookup"><span data-stu-id="05135-118">The email subject of alert notification</span></span>

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

### <span data-ttu-id="05135-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05135-119">CommonParameters</span></span>
<span data-ttu-id="05135-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05135-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05135-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05135-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05135-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="05135-122">INPUTS</span></span>

### <span data-ttu-id="05135-123">Keine</span><span class="sxs-lookup"><span data-stu-id="05135-123">None</span></span>

## <span data-ttu-id="05135-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="05135-124">OUTPUTS</span></span>

### <span data-ttu-id="05135-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span><span class="sxs-lookup"><span data-stu-id="05135-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span></span>

## <span data-ttu-id="05135-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="05135-126">NOTES</span></span>

## <span data-ttu-id="05135-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="05135-127">RELATED LINKS</span></span>
