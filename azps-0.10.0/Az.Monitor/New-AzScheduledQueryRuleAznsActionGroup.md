---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleaznsactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
ms.openlocfilehash: 485f244caa78bffda71d6129990c76daa8b173c4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841960"
---
# <span data-ttu-id="b83af-101">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="b83af-101">New-AzScheduledQueryRuleAznsActionGroup</span></span>

## <span data-ttu-id="b83af-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b83af-102">SYNOPSIS</span></span>
<span data-ttu-id="b83af-103">Erstellt ein Objekt vom Typ Azns-Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="b83af-103">Creates an object of type Azns Action Group</span></span>

## <span data-ttu-id="b83af-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b83af-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAznsActionGroup [-ActionGroup <String[]>] [-EmailSubject <String>]
 [-CustomWebhookPayload <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b83af-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b83af-105">DESCRIPTION</span></span>
<span data-ttu-id="b83af-106">Erstellt ein Objekt vom Typ Azns-Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="b83af-106">Creates an object of type Azns Action Group.</span></span>
<span data-ttu-id="b83af-107">Dieses Objekt soll an den Befehl übergeben werden, der die Warnungsregel für Protokolle erstellt.</span><span class="sxs-lookup"><span data-stu-id="b83af-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="b83af-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b83af-108">EXAMPLES</span></span>

### <span data-ttu-id="b83af-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b83af-109">Example 1</span></span>
```powershell
PS C:\> $aznsActionGroup = New-AzScheduledQueryRuleAznsActionGroup -ActionGroup @("/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourcegroups/MyResourceGroup/providers/microsoft.insights/actiongroups/MyActionGroup") -EmailSubject "Email subject" -CustomWebhookPayload "{}"
```

## <span data-ttu-id="b83af-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b83af-110">PARAMETERS</span></span>

### <span data-ttu-id="b83af-111">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="b83af-111">-ActionGroup</span></span>
<span data-ttu-id="b83af-112">Die Liste der Aktionsgruppen, an die eine Benachrichtigung gesendet werden soll</span><span class="sxs-lookup"><span data-stu-id="b83af-112">The list of action groups to send notification to</span></span>

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

### <span data-ttu-id="b83af-113">-CustomWebhookPayload</span><span class="sxs-lookup"><span data-stu-id="b83af-113">-CustomWebhookPayload</span></span>
<span data-ttu-id="b83af-114">Die angepasste webhook-Nutzlast</span><span class="sxs-lookup"><span data-stu-id="b83af-114">The customized webhook payload</span></span>

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

### <span data-ttu-id="b83af-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b83af-115">-DefaultProfile</span></span>
<span data-ttu-id="b83af-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b83af-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b83af-117">-EmailSubject</span><span class="sxs-lookup"><span data-stu-id="b83af-117">-EmailSubject</span></span>
<span data-ttu-id="b83af-118">E-Mail-Betreff der Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="b83af-118">The email subject of alert notification</span></span>

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

### <span data-ttu-id="b83af-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b83af-119">CommonParameters</span></span>
<span data-ttu-id="b83af-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b83af-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b83af-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b83af-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b83af-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b83af-122">INPUTS</span></span>

### <span data-ttu-id="b83af-123">Keine</span><span class="sxs-lookup"><span data-stu-id="b83af-123">None</span></span>

## <span data-ttu-id="b83af-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b83af-124">OUTPUTS</span></span>

### <span data-ttu-id="b83af-125">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleAznsAction</span><span class="sxs-lookup"><span data-stu-id="b83af-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span></span>

## <span data-ttu-id="b83af-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="b83af-126">NOTES</span></span>

## <span data-ttu-id="b83af-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b83af-127">RELATED LINKS</span></span>
