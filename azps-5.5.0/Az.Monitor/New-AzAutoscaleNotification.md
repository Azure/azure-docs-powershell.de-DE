---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
ms.openlocfilehash: 010698183dec206002c0966fb8f37d629d24794a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159417"
---
# <span data-ttu-id="37970-101">New-AzAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="37970-101">New-AzAutoscaleNotification</span></span>

## <span data-ttu-id="37970-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37970-102">SYNOPSIS</span></span>
<span data-ttu-id="37970-103">Erstellt eine E-Mail-Benachrichtigung für die automatische Skalierung.</span><span class="sxs-lookup"><span data-stu-id="37970-103">Creates an Autoscale email notification.</span></span>

## <span data-ttu-id="37970-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="37970-104">SYNTAX</span></span>

```
New-AzAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37970-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="37970-105">DESCRIPTION</span></span>
<span data-ttu-id="37970-106">Das **Cmdlet "New-AzAutoscaleNotification"** erstellt eine E-Mail-Benachrichtigung für AutoScale.</span><span class="sxs-lookup"><span data-stu-id="37970-106">The **New-AzAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="37970-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="37970-107">EXAMPLES</span></span>

### <span data-ttu-id="37970-108">Beispiel 1: Erstellen einer E-Mail-Benachrichtigung für die automatische Skalierung</span><span class="sxs-lookup"><span data-stu-id="37970-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzAutoscaleNotification -CustomEmail "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="37970-109">Mit diesem Befehl wird eine Autoacale-E-Mail-Benachrichtigung für zwei angegebene Adressen erstellt.</span><span class="sxs-lookup"><span data-stu-id="37970-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="37970-110">Beispiel 2: Erstellen einer E-Mail-Benachrichtigung zur automatischen Skalierung für den Abonnementadministrator</span><span class="sxs-lookup"><span data-stu-id="37970-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="37970-111">Mit diesem Befehl wird eine Autoacale-E-Mail-Benachrichtigung für den Abonnementadministrator erstellt.</span><span class="sxs-lookup"><span data-stu-id="37970-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="37970-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37970-112">PARAMETERS</span></span>

### <span data-ttu-id="37970-113">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="37970-113">-CustomEmail</span></span>
<span data-ttu-id="37970-114">Gibt eine durch Kommas getrennte Liste von E-Mail-Adressen an.</span><span class="sxs-lookup"><span data-stu-id="37970-114">Specifies a comma-separated list of email addresses.</span></span>

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

### <span data-ttu-id="37970-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37970-115">-DefaultProfile</span></span>
<span data-ttu-id="37970-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="37970-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37970-117">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="37970-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="37970-118">Gibt an, dass durch diesen Vorgang eine E-Mail-Benachrichtigung an den Abonnementadministrator gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="37970-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

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

### <span data-ttu-id="37970-119">-SendEmailToSubscriptionCoAdministrator</span><span class="sxs-lookup"><span data-stu-id="37970-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="37970-120">Gibt an, dass durch diesen Vorgang eine E-Mail-Benachrichtigung an die Mitadministratoren des Abonnements gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="37970-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

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

### <span data-ttu-id="37970-121">-Webhook</span><span class="sxs-lookup"><span data-stu-id="37970-121">-Webhook</span></span>
<span data-ttu-id="37970-122">Gibt eine durch Kommas getrennte Liste der Autoskalen-Webhooks an.</span><span class="sxs-lookup"><span data-stu-id="37970-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

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

### <span data-ttu-id="37970-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37970-123">CommonParameters</span></span>
<span data-ttu-id="37970-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37970-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37970-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37970-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37970-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="37970-126">INPUTS</span></span>

### <span data-ttu-id="37970-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span><span class="sxs-lookup"><span data-stu-id="37970-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span></span>

### <span data-ttu-id="37970-128">System.String[]</span><span class="sxs-lookup"><span data-stu-id="37970-128">System.String[]</span></span>

### <span data-ttu-id="37970-129">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="37970-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="37970-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="37970-130">OUTPUTS</span></span>

### <span data-ttu-id="37970-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="37970-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="37970-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="37970-132">NOTES</span></span>

## <span data-ttu-id="37970-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="37970-133">RELATED LINKS</span></span>

[<span data-ttu-id="37970-134">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="37970-134">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


