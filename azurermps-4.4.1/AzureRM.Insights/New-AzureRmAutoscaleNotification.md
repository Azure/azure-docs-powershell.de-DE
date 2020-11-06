---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
ms.openlocfilehash: f6791d2cc962f0bb0db038ad8c5391425c09bfbe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504154"
---
# <span data-ttu-id="7c215-101">New-AzureRmAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="7c215-101">New-AzureRmAutoscaleNotification</span></span>

## <span data-ttu-id="7c215-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7c215-102">SYNOPSIS</span></span>
<span data-ttu-id="7c215-103">Erstellt eine AutoScale-e-Mail-Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="7c215-103">Creates an Autoscale email notification.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c215-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c215-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleNotification [[-Webhooks] <WebhookNotification[]>] [[-CustomEmails] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c215-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7c215-105">DESCRIPTION</span></span>
<span data-ttu-id="7c215-106">Das Cmdlet **New-AzureRmAutoscaleNotification** erstellt eine e-Mail-Benachrichtigung für die autoskala.</span><span class="sxs-lookup"><span data-stu-id="7c215-106">The **New-AzureRmAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="7c215-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7c215-107">EXAMPLES</span></span>

### <span data-ttu-id="7c215-108">Beispiel 1: Erstellen einer AutoScale-e-Mail-Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="7c215-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="7c215-109">Mit diesem Befehl wird eine Autosacale-e-Mail-Benachrichtigung für zwei angegebene Adressen erstellt.</span><span class="sxs-lookup"><span data-stu-id="7c215-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="7c215-110">Beispiel 2: Erstellen einer AutoScale-e-Mail-Benachrichtigung für den Abonnement Administrator</span><span class="sxs-lookup"><span data-stu-id="7c215-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="7c215-111">Mit diesem Befehl wird eine Autosacale-e-Mail-Benachrichtigung für den Abonnement Administrator erstellt.</span><span class="sxs-lookup"><span data-stu-id="7c215-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="7c215-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c215-112">PARAMETERS</span></span>

### <span data-ttu-id="7c215-113">-CustomEmails</span><span class="sxs-lookup"><span data-stu-id="7c215-113">-CustomEmails</span></span>
<span data-ttu-id="7c215-114">Gibt eine durch trennzeichengetrennte Liste von e-Mail-Adressen an.</span><span class="sxs-lookup"><span data-stu-id="7c215-114">Specifies a comma-separated list of email addresses.</span></span>

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

### <span data-ttu-id="7c215-115">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="7c215-115">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="7c215-116">Gibt an, dass dieser Vorgang eine e-Mail-Benachrichtigung an den Abonnement Administrator sendet.</span><span class="sxs-lookup"><span data-stu-id="7c215-116">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

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

### <span data-ttu-id="7c215-117">-SendEmailToSubscriptionCoAdministrators</span><span class="sxs-lookup"><span data-stu-id="7c215-117">-SendEmailToSubscriptionCoAdministrators</span></span>
<span data-ttu-id="7c215-118">Gibt an, dass dieser Vorgang eine e-Mail-Benachrichtigung an die Co-Administratoren des Abonnements sendet.</span><span class="sxs-lookup"><span data-stu-id="7c215-118">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

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

### <span data-ttu-id="7c215-119">-Webhooks</span><span class="sxs-lookup"><span data-stu-id="7c215-119">-Webhooks</span></span>
<span data-ttu-id="7c215-120">Gibt eine durch trennzeichengetrennte Liste der AutoScale-webhooks an.</span><span class="sxs-lookup"><span data-stu-id="7c215-120">Specifies a comma-separated list of Autoscale webhooks.</span></span>

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

### <span data-ttu-id="7c215-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c215-121">-DefaultProfile</span></span>
<span data-ttu-id="7c215-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7c215-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c215-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c215-123">CommonParameters</span></span>
<span data-ttu-id="7c215-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c215-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c215-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c215-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c215-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7c215-126">INPUTS</span></span>

## <span data-ttu-id="7c215-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7c215-127">OUTPUTS</span></span>

### <span data-ttu-id="7c215-128">Microsoft. Azure. Management. Monitor. Management. Models. AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="7c215-128">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="7c215-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="7c215-129">NOTES</span></span>

## <span data-ttu-id="7c215-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7c215-130">RELATED LINKS</span></span>

[<span data-ttu-id="7c215-131">Neu – AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="7c215-131">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


