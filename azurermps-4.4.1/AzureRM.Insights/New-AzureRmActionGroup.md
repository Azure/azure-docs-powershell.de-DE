---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroup.md
ms.openlocfilehash: d4afe709d70872c1d7fb59e99f2f98d3dfe19d6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663581"
---
# <span data-ttu-id="68454-101">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="68454-101">New-AzureRmActionGroup</span></span>

## <span data-ttu-id="68454-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="68454-102">SYNOPSIS</span></span>
<span data-ttu-id="68454-103">Erstellt ein Aktions Gruppenverweis-Objekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="68454-103">Creates an ActionGroup reference object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68454-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="68454-104">SYNTAX</span></span>

```
New-AzureRmActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68454-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="68454-105">DESCRIPTION</span></span>
<span data-ttu-id="68454-106">Mit dem Cmdlet **New-AzureRmActionGroup** wird ein Aktionsgruppen-Referenzobjekt im Arbeitsspeicher erstellt.</span><span class="sxs-lookup"><span data-stu-id="68454-106">The **New-AzureRmActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="68454-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="68454-107">EXAMPLES</span></span>

### <span data-ttu-id="68454-108">Beispiel 1: Erstellen eines Aktionsgruppen-Referenzobjekts im Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="68454-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
```

## <span data-ttu-id="68454-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="68454-109">PARAMETERS</span></span>

### <span data-ttu-id="68454-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="68454-110">-ActionGroupId</span></span>
<span data-ttu-id="68454-111">Die ID/Name der Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="68454-111">The Id/name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68454-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68454-112">-DefaultProfile</span></span>
<span data-ttu-id="68454-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="68454-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68454-114">-Webhookproperty</span><span class="sxs-lookup"><span data-stu-id="68454-114">-WebhookProperty</span></span>
<span data-ttu-id="68454-115">Die webhook-Eigenschaften der Aktionsgruppe</span><span class="sxs-lookup"><span data-stu-id="68454-115">The webhook properties of the action group</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68454-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68454-116">CommonParameters</span></span>
<span data-ttu-id="68454-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68454-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68454-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68454-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68454-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="68454-119">INPUTS</span></span>

## <span data-ttu-id="68454-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="68454-120">OUTPUTS</span></span>

### <span data-ttu-id="68454-121">Microsoft. Azure. Management. Monitor. Management. Models. ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="68454-121">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="68454-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="68454-122">NOTES</span></span>

## <span data-ttu-id="68454-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="68454-123">RELATED LINKS</span></span>

[<span data-ttu-id="68454-124">Satz-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="68454-124">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="68454-125">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="68454-125">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="68454-126">Deaktivieren-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="68454-126">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="68454-127">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="68454-127">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="68454-128">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="68454-128">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="68454-129">Neu – AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="68454-129">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

