---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
ms.openlocfilehash: 8b94ad5728e7852bb3cd834e7479a29cc11c1698
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500593"
---
# <span data-ttu-id="d7703-101">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="d7703-101">New-AzureRmAutoscaleWebhook</span></span>

## <span data-ttu-id="d7703-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d7703-102">SYNOPSIS</span></span>
<span data-ttu-id="d7703-103">Erstellt einen AutoScale-webhook.</span><span class="sxs-lookup"><span data-stu-id="d7703-103">Creates an Autoscale webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7703-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7703-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7703-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7703-105">DESCRIPTION</span></span>
<span data-ttu-id="d7703-106">Das Cmdlet **New-AzureRmAutoscaleWebhook** erstellt einen AutoScale-webhook.</span><span class="sxs-lookup"><span data-stu-id="d7703-106">The **New-AzureRmAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="d7703-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7703-107">EXAMPLES</span></span>

## <span data-ttu-id="d7703-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7703-108">PARAMETERS</span></span>

### <span data-ttu-id="d7703-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7703-109">-DefaultProfile</span></span>
<span data-ttu-id="d7703-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d7703-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7703-111">-Property</span><span class="sxs-lookup"><span data-stu-id="d7703-111">-Property</span></span>
<span data-ttu-id="d7703-112">Gibt die Liste der Eigenschaften im Format @ an (Property1 = ' value1 ',....).</span><span class="sxs-lookup"><span data-stu-id="d7703-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Properties

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7703-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="d7703-113">-ServiceUri</span></span>
<span data-ttu-id="d7703-114">Gibt den Dienst-URI an.</span><span class="sxs-lookup"><span data-stu-id="d7703-114">Specifies the service URI.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7703-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7703-115">CommonParameters</span></span>
<span data-ttu-id="d7703-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7703-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7703-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7703-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7703-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d7703-118">INPUTS</span></span>

### <span data-ttu-id="d7703-119">Keine</span><span class="sxs-lookup"><span data-stu-id="d7703-119">None</span></span>
<span data-ttu-id="d7703-120">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="d7703-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d7703-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d7703-121">OUTPUTS</span></span>

### <span data-ttu-id="d7703-122">Microsoft. Azure. Management. Monitor. Management. Models. WebhookNotification</span><span class="sxs-lookup"><span data-stu-id="d7703-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="d7703-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="d7703-123">NOTES</span></span>

## <span data-ttu-id="d7703-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d7703-124">RELATED LINKS</span></span>

[<span data-ttu-id="d7703-125">Neu – AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="d7703-125">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


