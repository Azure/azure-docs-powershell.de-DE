---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalenotification
schema: 2.0.0
ms.openlocfilehash: 51a5c01c28471cf85617b8ab629c2f79b366d555
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850824"
---
# <span data-ttu-id="eca74-101">New-AzureRmAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="eca74-101">New-AzureRmAutoscaleNotification</span></span>

## <span data-ttu-id="eca74-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eca74-102">SYNOPSIS</span></span>
<span data-ttu-id="eca74-103">Erstellt eine AutoScale-e-Mail-Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="eca74-103">Creates an Autoscale email notification.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eca74-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eca74-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eca74-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eca74-105">DESCRIPTION</span></span>
<span data-ttu-id="eca74-106">Das Cmdlet **New-AzureRmAutoscaleNotification** erstellt eine e-Mail-Benachrichtigung für die autoskala.</span><span class="sxs-lookup"><span data-stu-id="eca74-106">The **New-AzureRmAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="eca74-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eca74-107">EXAMPLES</span></span>

### <span data-ttu-id="eca74-108">Beispiel 1: Erstellen einer AutoScale-e-Mail-Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="eca74-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="eca74-109">Mit diesem Befehl wird eine Autosacale-e-Mail-Benachrichtigung für zwei angegebene Adressen erstellt.</span><span class="sxs-lookup"><span data-stu-id="eca74-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="eca74-110">Beispiel 2: Erstellen einer AutoScale-e-Mail-Benachrichtigung für den Abonnement Administrator</span><span class="sxs-lookup"><span data-stu-id="eca74-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="eca74-111">Mit diesem Befehl wird eine Autosacale-e-Mail-Benachrichtigung für den Abonnement Administrator erstellt.</span><span class="sxs-lookup"><span data-stu-id="eca74-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="eca74-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="eca74-112">PARAMETERS</span></span>

### <span data-ttu-id="eca74-113">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="eca74-113">-CustomEmail</span></span>
<span data-ttu-id="eca74-114">Gibt eine durch trennzeichengetrennte Liste von e-Mail-Adressen an.</span><span class="sxs-lookup"><span data-stu-id="eca74-114">Specifies a comma-separated list of email addresses.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eca74-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eca74-115">-DefaultProfile</span></span>
<span data-ttu-id="eca74-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="eca74-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eca74-117">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="eca74-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="eca74-118">Gibt an, dass dieser Vorgang eine e-Mail-Benachrichtigung an den Abonnement Administrator sendet.</span><span class="sxs-lookup"><span data-stu-id="eca74-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eca74-119">-SendEmailToSubscriptionCoAdministrator</span><span class="sxs-lookup"><span data-stu-id="eca74-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="eca74-120">Gibt an, dass dieser Vorgang eine e-Mail-Benachrichtigung an die Co-Administratoren des Abonnements sendet.</span><span class="sxs-lookup"><span data-stu-id="eca74-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eca74-121">-Webhook</span><span class="sxs-lookup"><span data-stu-id="eca74-121">-Webhook</span></span>
<span data-ttu-id="eca74-122">Gibt eine durch trennzeichengetrennte Liste der AutoScale-webhooks an.</span><span class="sxs-lookup"><span data-stu-id="eca74-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eca74-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eca74-123">CommonParameters</span></span>
<span data-ttu-id="eca74-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eca74-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eca74-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eca74-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eca74-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eca74-126">INPUTS</span></span>

### <span data-ttu-id="eca74-127">Microsoft. Azure. Management. Monitor. Management. Models. WebhookNotification []</span><span class="sxs-lookup"><span data-stu-id="eca74-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span></span>

### <span data-ttu-id="eca74-128">System. String []</span><span class="sxs-lookup"><span data-stu-id="eca74-128">System.String[]</span></span>

### <span data-ttu-id="eca74-129">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="eca74-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="eca74-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eca74-130">OUTPUTS</span></span>

### <span data-ttu-id="eca74-131">Microsoft. Azure. Management. Monitor. Management. Models. AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="eca74-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="eca74-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="eca74-132">NOTES</span></span>

## <span data-ttu-id="eca74-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eca74-133">RELATED LINKS</span></span>

[<span data-ttu-id="eca74-134">Neu – AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="eca74-134">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


