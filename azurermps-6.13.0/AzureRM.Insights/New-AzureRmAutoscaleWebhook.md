---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
ms.openlocfilehash: 607976539e6bf93a0fa947741a4af4d4a7d34b67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662686"
---
# <span data-ttu-id="d434a-101">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="d434a-101">New-AzureRmAutoscaleWebhook</span></span>

## <span data-ttu-id="d434a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d434a-102">SYNOPSIS</span></span>
<span data-ttu-id="d434a-103">Erstellt einen AutoScale-webhook.</span><span class="sxs-lookup"><span data-stu-id="d434a-103">Creates an Autoscale webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d434a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d434a-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d434a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d434a-105">DESCRIPTION</span></span>
<span data-ttu-id="d434a-106">Das Cmdlet **New-AzureRmAutoscaleWebhook** erstellt einen AutoScale-webhook.</span><span class="sxs-lookup"><span data-stu-id="d434a-106">The **New-AzureRmAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="d434a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d434a-107">EXAMPLES</span></span>

## <span data-ttu-id="d434a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d434a-108">PARAMETERS</span></span>

### <span data-ttu-id="d434a-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d434a-109">-DefaultProfile</span></span>
<span data-ttu-id="d434a-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d434a-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d434a-111">-Property</span><span class="sxs-lookup"><span data-stu-id="d434a-111">-Property</span></span>
<span data-ttu-id="d434a-112">Gibt die Liste der Eigenschaften im Format @ an (Property1 = ' value1 ',....).</span><span class="sxs-lookup"><span data-stu-id="d434a-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d434a-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="d434a-113">-ServiceUri</span></span>
<span data-ttu-id="d434a-114">Gibt den Dienst-URI an.</span><span class="sxs-lookup"><span data-stu-id="d434a-114">Specifies the service URI.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d434a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d434a-115">CommonParameters</span></span>
<span data-ttu-id="d434a-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d434a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d434a-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d434a-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d434a-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d434a-118">INPUTS</span></span>

### <span data-ttu-id="d434a-119">System. String</span><span class="sxs-lookup"><span data-stu-id="d434a-119">System.String</span></span>

### <span data-ttu-id="d434a-120">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d434a-120">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d434a-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d434a-121">OUTPUTS</span></span>

### <span data-ttu-id="d434a-122">Microsoft. Azure. Management. Monitor. Management. Models. WebhookNotification</span><span class="sxs-lookup"><span data-stu-id="d434a-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="d434a-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="d434a-123">NOTES</span></span>

## <span data-ttu-id="d434a-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d434a-124">RELATED LINKS</span></span>

[<span data-ttu-id="d434a-125">Neu – AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="d434a-125">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


