---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroup.md
ms.openlocfilehash: 9428ea3c297bcdab01ee6464d38b5c20910b69d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662850"
---
# <span data-ttu-id="3a9e2-101">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="3a9e2-101">New-AzureRmActionGroup</span></span>

## <span data-ttu-id="3a9e2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3a9e2-102">SYNOPSIS</span></span>
<span data-ttu-id="3a9e2-103">Erstellt ein Aktions Gruppenverweis-Objekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="3a9e2-103">Creates an ActionGroup reference object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a9e2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a9e2-104">SYNTAX</span></span>

```
New-AzureRmActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a9e2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a9e2-105">DESCRIPTION</span></span>
<span data-ttu-id="3a9e2-106">Mit dem Cmdlet **New-AzureRmActionGroup** wird ein Aktionsgruppen-Referenzobjekt im Arbeitsspeicher erstellt.</span><span class="sxs-lookup"><span data-stu-id="3a9e2-106">The **New-AzureRmActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="3a9e2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3a9e2-107">EXAMPLES</span></span>

### <span data-ttu-id="3a9e2-108">Beispiel 1: Erstellen eines Aktionsgruppen-Referenzobjekts im Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="3a9e2-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
```

## <span data-ttu-id="3a9e2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a9e2-109">PARAMETERS</span></span>

### <span data-ttu-id="3a9e2-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="3a9e2-110">-ActionGroupId</span></span>
<span data-ttu-id="3a9e2-111">Die ID/Name der Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="3a9e2-111">The Id/name of the action group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a9e2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a9e2-112">-DefaultProfile</span></span>
<span data-ttu-id="3a9e2-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3a9e2-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a9e2-114">-Webhookproperty</span><span class="sxs-lookup"><span data-stu-id="3a9e2-114">-WebhookProperty</span></span>
<span data-ttu-id="3a9e2-115">Die webhook-Eigenschaften der Aktionsgruppe</span><span class="sxs-lookup"><span data-stu-id="3a9e2-115">The webhook properties of the action group</span></span>

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

### <span data-ttu-id="3a9e2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a9e2-116">CommonParameters</span></span>
<span data-ttu-id="3a9e2-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a9e2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a9e2-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a9e2-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a9e2-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3a9e2-119">INPUTS</span></span>

### <span data-ttu-id="3a9e2-120">Keine</span><span class="sxs-lookup"><span data-stu-id="3a9e2-120">None</span></span>
<span data-ttu-id="3a9e2-121">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="3a9e2-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3a9e2-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3a9e2-122">OUTPUTS</span></span>

### <span data-ttu-id="3a9e2-123">Microsoft. Azure. Management. Monitor. Management. Models. ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="3a9e2-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="3a9e2-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="3a9e2-124">NOTES</span></span>

## <span data-ttu-id="3a9e2-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3a9e2-125">RELATED LINKS</span></span>

[<span data-ttu-id="3a9e2-126">Satz-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3a9e2-126">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="3a9e2-127">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3a9e2-127">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="3a9e2-128">Deaktivieren-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3a9e2-128">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="3a9e2-129">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3a9e2-129">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="3a9e2-130">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3a9e2-130">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="3a9e2-131">Neu – AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="3a9e2-131">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

