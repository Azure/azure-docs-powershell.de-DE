---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAutoscaleWebhook.md
ms.openlocfilehash: a719d841df2d3f211fdb2592ed2a96b507c51e10
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841976"
---
# <span data-ttu-id="68a80-101">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="68a80-101">New-AzAutoscaleWebhook</span></span>

## <span data-ttu-id="68a80-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="68a80-102">SYNOPSIS</span></span>
<span data-ttu-id="68a80-103">Erstellt einen AutoScale-webhook.</span><span class="sxs-lookup"><span data-stu-id="68a80-103">Creates an Autoscale webhook.</span></span>

## <span data-ttu-id="68a80-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="68a80-104">SYNTAX</span></span>

```
New-AzAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68a80-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="68a80-105">DESCRIPTION</span></span>
<span data-ttu-id="68a80-106">Das Cmdlet **New-AzAutoscaleWebhook** erstellt einen AutoScale-webhook.</span><span class="sxs-lookup"><span data-stu-id="68a80-106">The **New-AzAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="68a80-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="68a80-107">EXAMPLES</span></span>

## <span data-ttu-id="68a80-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="68a80-108">PARAMETERS</span></span>

### <span data-ttu-id="68a80-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68a80-109">-DefaultProfile</span></span>
<span data-ttu-id="68a80-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="68a80-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68a80-111">-Property</span><span class="sxs-lookup"><span data-stu-id="68a80-111">-Property</span></span>
<span data-ttu-id="68a80-112">Gibt die Liste der Eigenschaften im Format @ an (Property1 = ' value1 ',....).</span><span class="sxs-lookup"><span data-stu-id="68a80-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="68a80-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="68a80-113">-ServiceUri</span></span>
<span data-ttu-id="68a80-114">Gibt den Dienst-URI an.</span><span class="sxs-lookup"><span data-stu-id="68a80-114">Specifies the service URI.</span></span>

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

### <span data-ttu-id="68a80-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68a80-115">CommonParameters</span></span>
<span data-ttu-id="68a80-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68a80-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68a80-117">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68a80-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68a80-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="68a80-118">INPUTS</span></span>

### <span data-ttu-id="68a80-119">System. String</span><span class="sxs-lookup"><span data-stu-id="68a80-119">System.String</span></span>

### <span data-ttu-id="68a80-120">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="68a80-120">System.Collections.Hashtable</span></span>

## <span data-ttu-id="68a80-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="68a80-121">OUTPUTS</span></span>

### <span data-ttu-id="68a80-122">Microsoft. Azure. Management. Monitor. Management. Models. WebhookNotification</span><span class="sxs-lookup"><span data-stu-id="68a80-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="68a80-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="68a80-123">NOTES</span></span>

## <span data-ttu-id="68a80-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="68a80-124">RELATED LINKS</span></span>

[<span data-ttu-id="68a80-125">Neu – AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="68a80-125">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


