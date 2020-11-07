---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleaznsactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
ms.openlocfilehash: aa15b2b74fff056eb4fde3e9a3d176b703a6aaed
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822683"
---
# <span data-ttu-id="10276-101">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="10276-101">New-AzScheduledQueryRuleAznsActionGroup</span></span>

## <span data-ttu-id="10276-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="10276-102">SYNOPSIS</span></span>
<span data-ttu-id="10276-103">Erstellt ein Objekt vom Typ Azns-Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="10276-103">Creates an object of type Azns Action Group</span></span>

## <span data-ttu-id="10276-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="10276-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAznsActionGroup [-ActionGroup <String[]>] [-EmailSubject <String>]
 [-CustomWebhookPayload <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10276-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10276-105">DESCRIPTION</span></span>
<span data-ttu-id="10276-106">Erstellt ein Objekt vom Typ Azns-Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="10276-106">Creates an object of type Azns Action Group.</span></span>
<span data-ttu-id="10276-107">Dieses Objekt soll an den Befehl übergeben werden, der die Warnungsregel für Protokolle erstellt.</span><span class="sxs-lookup"><span data-stu-id="10276-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="10276-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="10276-108">EXAMPLES</span></span>

### <span data-ttu-id="10276-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="10276-109">Example 1</span></span>
```powershell
PS C:\> $aznsActionGroup = New-AzScheduledQueryRuleAznsActionGroup -ActionGroup @("/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourcegroups/MyResourceGroup/providers/microsoft.insights/actiongroups/MyActionGroup") -EmailSubject "Email subject" -CustomWebhookPayload "{}"
```

## <span data-ttu-id="10276-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="10276-110">PARAMETERS</span></span>

### <span data-ttu-id="10276-111">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="10276-111">-ActionGroup</span></span>
<span data-ttu-id="10276-112">Die Liste der Aktionsgruppen, an die eine Benachrichtigung gesendet werden soll</span><span class="sxs-lookup"><span data-stu-id="10276-112">The list of action groups to send notification to</span></span>

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

### <span data-ttu-id="10276-113">-CustomWebhookPayload</span><span class="sxs-lookup"><span data-stu-id="10276-113">-CustomWebhookPayload</span></span>
<span data-ttu-id="10276-114">Die angepasste webhook-Nutzlast</span><span class="sxs-lookup"><span data-stu-id="10276-114">The customized webhook payload</span></span>

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

### <span data-ttu-id="10276-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10276-115">-DefaultProfile</span></span>
<span data-ttu-id="10276-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="10276-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10276-117">-EmailSubject</span><span class="sxs-lookup"><span data-stu-id="10276-117">-EmailSubject</span></span>
<span data-ttu-id="10276-118">E-Mail-Betreff der Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="10276-118">The email subject of alert notification</span></span>

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

### <span data-ttu-id="10276-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10276-119">CommonParameters</span></span>
<span data-ttu-id="10276-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10276-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10276-121">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10276-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10276-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="10276-122">INPUTS</span></span>

### <span data-ttu-id="10276-123">Keine</span><span class="sxs-lookup"><span data-stu-id="10276-123">None</span></span>

## <span data-ttu-id="10276-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="10276-124">OUTPUTS</span></span>

### <span data-ttu-id="10276-125">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleAznsAction</span><span class="sxs-lookup"><span data-stu-id="10276-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span></span>

## <span data-ttu-id="10276-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="10276-126">NOTES</span></span>

## <span data-ttu-id="10276-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="10276-127">RELATED LINKS</span></span>
