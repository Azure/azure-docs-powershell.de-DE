---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleaznsactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
ms.openlocfilehash: 44f9eae56c822e5fe068679331bcdd3a0ad17d81
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152156"
---
# <span data-ttu-id="65848-101">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="65848-101">New-AzScheduledQueryRuleAznsActionGroup</span></span>

## <span data-ttu-id="65848-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65848-102">SYNOPSIS</span></span>
<span data-ttu-id="65848-103">Erstellt ein Objekt vom Typ "Azns-Aktionsgruppe".</span><span class="sxs-lookup"><span data-stu-id="65848-103">Creates an object of type Azns Action Group</span></span>

## <span data-ttu-id="65848-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65848-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAznsActionGroup [-ActionGroup <String[]>] [-EmailSubject <String>]
 [-CustomWebhookPayload <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65848-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="65848-105">DESCRIPTION</span></span>
<span data-ttu-id="65848-106">Erstellt ein Objekt vom Typ "Azns-Aktionsgruppe".</span><span class="sxs-lookup"><span data-stu-id="65848-106">Creates an object of type Azns Action Group.</span></span>
<span data-ttu-id="65848-107">Dieses Objekt wird an den Befehl übergeben, mit dem eine Protokollwarnungsregel erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="65848-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="65848-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="65848-108">EXAMPLES</span></span>

### <span data-ttu-id="65848-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="65848-109">Example 1</span></span>
```powershell
PS C:\> $aznsActionGroup = New-AzScheduledQueryRuleAznsActionGroup -ActionGroup @("/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourcegroups/MyResourceGroup/providers/microsoft.insights/actiongroups/MyActionGroup") -EmailSubject "Email subject" -CustomWebhookPayload "{}"
```

## <span data-ttu-id="65848-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65848-110">PARAMETERS</span></span>

### <span data-ttu-id="65848-111">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="65848-111">-ActionGroup</span></span>
<span data-ttu-id="65848-112">Die Liste der Aktionsgruppen, an die Benachrichtigungen gesendet werden</span><span class="sxs-lookup"><span data-stu-id="65848-112">The list of action groups to send notification to</span></span>

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

### <span data-ttu-id="65848-113">-CustomWebhookPayload</span><span class="sxs-lookup"><span data-stu-id="65848-113">-CustomWebhookPayload</span></span>
<span data-ttu-id="65848-114">Die angepasste Webhooknutzlast</span><span class="sxs-lookup"><span data-stu-id="65848-114">The customized webhook payload</span></span>

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

### <span data-ttu-id="65848-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65848-115">-DefaultProfile</span></span>
<span data-ttu-id="65848-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="65848-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65848-117">-EmailSubject</span><span class="sxs-lookup"><span data-stu-id="65848-117">-EmailSubject</span></span>
<span data-ttu-id="65848-118">Der E-Mail-Betreff der Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="65848-118">The email subject of alert notification</span></span>

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

### <span data-ttu-id="65848-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65848-119">CommonParameters</span></span>
<span data-ttu-id="65848-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65848-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65848-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65848-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65848-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="65848-122">INPUTS</span></span>

### <span data-ttu-id="65848-123">Keine</span><span class="sxs-lookup"><span data-stu-id="65848-123">None</span></span>

## <span data-ttu-id="65848-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="65848-124">OUTPUTS</span></span>

### <span data-ttu-id="65848-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span><span class="sxs-lookup"><span data-stu-id="65848-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span></span>

## <span data-ttu-id="65848-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="65848-126">NOTES</span></span>

## <span data-ttu-id="65848-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="65848-127">RELATED LINKS</span></span>
