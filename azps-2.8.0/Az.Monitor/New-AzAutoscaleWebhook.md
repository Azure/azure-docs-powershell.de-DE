---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleWebhook.md
ms.openlocfilehash: 4f2e7ea3293c9ca40271b9092673f33108a9f1be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822048"
---
# <span data-ttu-id="984ec-101">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="984ec-101">New-AzAutoscaleWebhook</span></span>

## <span data-ttu-id="984ec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="984ec-102">SYNOPSIS</span></span>
<span data-ttu-id="984ec-103">Erstellt einen AutoScale-webhook.</span><span class="sxs-lookup"><span data-stu-id="984ec-103">Creates an Autoscale webhook.</span></span>

## <span data-ttu-id="984ec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="984ec-104">SYNTAX</span></span>

```
New-AzAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="984ec-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="984ec-105">DESCRIPTION</span></span>
<span data-ttu-id="984ec-106">Das Cmdlet **New-AzAutoscaleWebhook** erstellt einen AutoScale-webhook.</span><span class="sxs-lookup"><span data-stu-id="984ec-106">The **New-AzAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="984ec-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="984ec-107">EXAMPLES</span></span>

## <span data-ttu-id="984ec-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="984ec-108">PARAMETERS</span></span>

### <span data-ttu-id="984ec-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="984ec-109">-DefaultProfile</span></span>
<span data-ttu-id="984ec-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="984ec-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="984ec-111">-Property</span><span class="sxs-lookup"><span data-stu-id="984ec-111">-Property</span></span>
<span data-ttu-id="984ec-112">Gibt die Liste der Eigenschaften im Format @ an (Property1 = ' value1 ',....).</span><span class="sxs-lookup"><span data-stu-id="984ec-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="984ec-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="984ec-113">-ServiceUri</span></span>
<span data-ttu-id="984ec-114">Gibt den Dienst-URI an.</span><span class="sxs-lookup"><span data-stu-id="984ec-114">Specifies the service URI.</span></span>

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

### <span data-ttu-id="984ec-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="984ec-115">CommonParameters</span></span>
<span data-ttu-id="984ec-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="984ec-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="984ec-117">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="984ec-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="984ec-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="984ec-118">INPUTS</span></span>

### <span data-ttu-id="984ec-119">System. String</span><span class="sxs-lookup"><span data-stu-id="984ec-119">System.String</span></span>

### <span data-ttu-id="984ec-120">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="984ec-120">System.Collections.Hashtable</span></span>

## <span data-ttu-id="984ec-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="984ec-121">OUTPUTS</span></span>

### <span data-ttu-id="984ec-122">Microsoft. Azure. Management. Monitor. Management. Models. WebhookNotification</span><span class="sxs-lookup"><span data-stu-id="984ec-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="984ec-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="984ec-123">NOTES</span></span>

## <span data-ttu-id="984ec-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="984ec-124">RELATED LINKS</span></span>

[<span data-ttu-id="984ec-125">Neu – AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="984ec-125">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


