---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
ms.openlocfilehash: 010698183dec206002c0966fb8f37d629d24794a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166506"
---
# <span data-ttu-id="7f7c0-101">New-AzAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="7f7c0-101">New-AzAutoscaleNotification</span></span>

## <span data-ttu-id="7f7c0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7f7c0-102">SYNOPSIS</span></span>
<span data-ttu-id="7f7c0-103">Erstellt eine AutoScale-e-Mail-Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="7f7c0-103">Creates an Autoscale email notification.</span></span>

## <span data-ttu-id="7f7c0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f7c0-104">SYNTAX</span></span>

```
New-AzAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f7c0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f7c0-105">DESCRIPTION</span></span>
<span data-ttu-id="7f7c0-106">Das Cmdlet **New-AzAutoscaleNotification** erstellt eine e-Mail-Benachrichtigung für die autoskala.</span><span class="sxs-lookup"><span data-stu-id="7f7c0-106">The **New-AzAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="7f7c0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f7c0-107">EXAMPLES</span></span>

### <span data-ttu-id="7f7c0-108">Beispiel 1: Erstellen einer AutoScale-e-Mail-Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="7f7c0-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzAutoscaleNotification -CustomEmail "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="7f7c0-109">Mit diesem Befehl wird eine Autosacale-e-Mail-Benachrichtigung für zwei angegebene Adressen erstellt.</span><span class="sxs-lookup"><span data-stu-id="7f7c0-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="7f7c0-110">Beispiel 2: Erstellen einer AutoScale-e-Mail-Benachrichtigung für den Abonnement Administrator</span><span class="sxs-lookup"><span data-stu-id="7f7c0-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="7f7c0-111">Mit diesem Befehl wird eine Autosacale-e-Mail-Benachrichtigung für den Abonnement Administrator erstellt.</span><span class="sxs-lookup"><span data-stu-id="7f7c0-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="7f7c0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f7c0-112">PARAMETERS</span></span>

### <span data-ttu-id="7f7c0-113">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="7f7c0-113">-CustomEmail</span></span>
<span data-ttu-id="7f7c0-114">Gibt eine durch trennzeichengetrennte Liste von e-Mail-Adressen an.</span><span class="sxs-lookup"><span data-stu-id="7f7c0-114">Specifies a comma-separated list of email addresses.</span></span>

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

### <span data-ttu-id="7f7c0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f7c0-115">-DefaultProfile</span></span>
<span data-ttu-id="7f7c0-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7f7c0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f7c0-117">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="7f7c0-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="7f7c0-118">Gibt an, dass dieser Vorgang eine e-Mail-Benachrichtigung an den Abonnement Administrator sendet.</span><span class="sxs-lookup"><span data-stu-id="7f7c0-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

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

### <span data-ttu-id="7f7c0-119">-SendEmailToSubscriptionCoAdministrator</span><span class="sxs-lookup"><span data-stu-id="7f7c0-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="7f7c0-120">Gibt an, dass dieser Vorgang eine e-Mail-Benachrichtigung an die Co-Administratoren des Abonnements sendet.</span><span class="sxs-lookup"><span data-stu-id="7f7c0-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

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

### <span data-ttu-id="7f7c0-121">-Webhook</span><span class="sxs-lookup"><span data-stu-id="7f7c0-121">-Webhook</span></span>
<span data-ttu-id="7f7c0-122">Gibt eine durch trennzeichengetrennte Liste der AutoScale-webhooks an.</span><span class="sxs-lookup"><span data-stu-id="7f7c0-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

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

### <span data-ttu-id="7f7c0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f7c0-123">CommonParameters</span></span>
<span data-ttu-id="7f7c0-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f7c0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f7c0-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f7c0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f7c0-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7f7c0-126">INPUTS</span></span>

### <span data-ttu-id="7f7c0-127">Microsoft. Azure. Management. Monitor. Management. Models. WebhookNotification []</span><span class="sxs-lookup"><span data-stu-id="7f7c0-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span></span>

### <span data-ttu-id="7f7c0-128">System. String []</span><span class="sxs-lookup"><span data-stu-id="7f7c0-128">System.String[]</span></span>

### <span data-ttu-id="7f7c0-129">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="7f7c0-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7f7c0-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7f7c0-130">OUTPUTS</span></span>

### <span data-ttu-id="7f7c0-131">Microsoft. Azure. Management. Monitor. Management. Models. AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="7f7c0-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="7f7c0-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="7f7c0-132">NOTES</span></span>

## <span data-ttu-id="7f7c0-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7f7c0-133">RELATED LINKS</span></span>

[<span data-ttu-id="7f7c0-134">Neu – AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="7f7c0-134">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


