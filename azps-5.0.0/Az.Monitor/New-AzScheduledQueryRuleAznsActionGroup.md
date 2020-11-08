---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleaznsactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
ms.openlocfilehash: 44f9eae56c822e5fe068679331bcdd3a0ad17d81
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177497"
---
# <span data-ttu-id="0f9c6-101">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="0f9c6-101">New-AzScheduledQueryRuleAznsActionGroup</span></span>

## <span data-ttu-id="0f9c6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0f9c6-102">SYNOPSIS</span></span>
<span data-ttu-id="0f9c6-103">Erstellt ein Objekt vom Typ Azns-Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="0f9c6-103">Creates an object of type Azns Action Group</span></span>

## <span data-ttu-id="0f9c6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f9c6-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAznsActionGroup [-ActionGroup <String[]>] [-EmailSubject <String>]
 [-CustomWebhookPayload <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f9c6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f9c6-105">DESCRIPTION</span></span>
<span data-ttu-id="0f9c6-106">Erstellt ein Objekt vom Typ Azns-Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="0f9c6-106">Creates an object of type Azns Action Group.</span></span>
<span data-ttu-id="0f9c6-107">Dieses Objekt soll an den Befehl übergeben werden, der die Warnungsregel für Protokolle erstellt.</span><span class="sxs-lookup"><span data-stu-id="0f9c6-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="0f9c6-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0f9c6-108">EXAMPLES</span></span>

### <span data-ttu-id="0f9c6-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0f9c6-109">Example 1</span></span>
```powershell
PS C:\> $aznsActionGroup = New-AzScheduledQueryRuleAznsActionGroup -ActionGroup @("/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourcegroups/MyResourceGroup/providers/microsoft.insights/actiongroups/MyActionGroup") -EmailSubject "Email subject" -CustomWebhookPayload "{}"
```

## <span data-ttu-id="0f9c6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f9c6-110">PARAMETERS</span></span>

### <span data-ttu-id="0f9c6-111">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="0f9c6-111">-ActionGroup</span></span>
<span data-ttu-id="0f9c6-112">Die Liste der Aktionsgruppen, an die eine Benachrichtigung gesendet werden soll</span><span class="sxs-lookup"><span data-stu-id="0f9c6-112">The list of action groups to send notification to</span></span>

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

### <span data-ttu-id="0f9c6-113">-CustomWebhookPayload</span><span class="sxs-lookup"><span data-stu-id="0f9c6-113">-CustomWebhookPayload</span></span>
<span data-ttu-id="0f9c6-114">Die angepasste webhook-Nutzlast</span><span class="sxs-lookup"><span data-stu-id="0f9c6-114">The customized webhook payload</span></span>

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

### <span data-ttu-id="0f9c6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f9c6-115">-DefaultProfile</span></span>
<span data-ttu-id="0f9c6-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0f9c6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f9c6-117">-EmailSubject</span><span class="sxs-lookup"><span data-stu-id="0f9c6-117">-EmailSubject</span></span>
<span data-ttu-id="0f9c6-118">E-Mail-Betreff der Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="0f9c6-118">The email subject of alert notification</span></span>

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

### <span data-ttu-id="0f9c6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f9c6-119">CommonParameters</span></span>
<span data-ttu-id="0f9c6-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f9c6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f9c6-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f9c6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f9c6-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0f9c6-122">INPUTS</span></span>

### <span data-ttu-id="0f9c6-123">Keine</span><span class="sxs-lookup"><span data-stu-id="0f9c6-123">None</span></span>

## <span data-ttu-id="0f9c6-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0f9c6-124">OUTPUTS</span></span>

### <span data-ttu-id="0f9c6-125">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleAznsAction</span><span class="sxs-lookup"><span data-stu-id="0f9c6-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span></span>

## <span data-ttu-id="0f9c6-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="0f9c6-126">NOTES</span></span>

## <span data-ttu-id="0f9c6-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0f9c6-127">RELATED LINKS</span></span>
