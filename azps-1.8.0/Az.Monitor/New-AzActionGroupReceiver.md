---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: 35f540d26464b7cdc4b08916f1397b71ee7cca18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93818948"
---
# <span data-ttu-id="75721-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="75721-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="75721-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="75721-102">SYNOPSIS</span></span>
<span data-ttu-id="75721-103">Erstellt einen neuen Aktionsgruppen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="75721-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="75721-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="75721-104">SYNTAX</span></span>

### <span data-ttu-id="75721-105">NewEmailReceiver (Standard)</span><span class="sxs-lookup"><span data-stu-id="75721-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75721-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="75721-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-SmsReceiver] [-CountryCode <String>] -PhoneNumber <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75721-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="75721-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-WebhookReceiver] -ServiceUri <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75721-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75721-108">DESCRIPTION</span></span>
<span data-ttu-id="75721-109">Das Cmdlet **New-AzActionGroupReceiver** erstellt einen neuen Aktionsgruppen Empfänger im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="75721-109">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="75721-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75721-110">EXAMPLES</span></span>

### <span data-ttu-id="75721-111">Beispiel 1: Erstellen eines neuen e-Mail-Empfängers im Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="75721-111">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="75721-112">Dieser Befehl erstellt einen neuen e-Mail-Empfänger im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="75721-112">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="75721-113">Beispiel 2: Erstellen eines neuen SMS-Empfängers im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="75721-113">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="75721-114">Dieser Befehl erstellt einen neuen SMS-Empfänger im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="75721-114">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="75721-115">Beispiel 3: Erstellen eines neuen webhook-Receivers im Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="75721-115">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="75721-116">Dieser Befehl erstellt einen neuen webhook-Empfänger im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="75721-116">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="75721-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="75721-117">PARAMETERS</span></span>

### <span data-ttu-id="75721-118">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="75721-118">-CountryCode</span></span>
<span data-ttu-id="75721-119">Gibt die Landesvorwahl für den SMS-Empfänger an.</span><span class="sxs-lookup"><span data-stu-id="75721-119">Specifies the country code for the SMS receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSmsReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75721-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75721-120">-DefaultProfile</span></span>
<span data-ttu-id="75721-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="75721-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75721-122">-Email-Email</span><span class="sxs-lookup"><span data-stu-id="75721-122">-EmailAddress</span></span>
<span data-ttu-id="75721-123">Gibt die Adresse des e-Mail-Empfängers an.</span><span class="sxs-lookup"><span data-stu-id="75721-123">Specifies the address for the Email receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewEmailReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75721-124">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="75721-124">-EmailReceiver</span></span>
<span data-ttu-id="75721-125">Gibt an, dass ein e-Mail-Empfänger erstellt werden soll</span><span class="sxs-lookup"><span data-stu-id="75721-125">Specifies to create an Email receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewEmailReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75721-126">-Name</span><span class="sxs-lookup"><span data-stu-id="75721-126">-Name</span></span>
<span data-ttu-id="75721-127">Gibt den Namen des Empfängers an.</span><span class="sxs-lookup"><span data-stu-id="75721-127">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="75721-128">-Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="75721-128">-PhoneNumber</span></span>
<span data-ttu-id="75721-129">Gibt die Telefonnummer für den SMS-Empfänger an.</span><span class="sxs-lookup"><span data-stu-id="75721-129">Specifies the phone number for the SMS receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSmsReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75721-130">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="75721-130">-ServiceUri</span></span>
<span data-ttu-id="75721-131">Gibt den URI für den webhook-Empfänger an.</span><span class="sxs-lookup"><span data-stu-id="75721-131">Specifies the URI for the webhook receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75721-132">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="75721-132">-SmsReceiver</span></span>
<span data-ttu-id="75721-133">Gibt an, dass ein SMS-Empfänger erstellt werden soll</span><span class="sxs-lookup"><span data-stu-id="75721-133">Specifies to create a SMS receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewSmsReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75721-134">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="75721-134">-WebhookReceiver</span></span>
<span data-ttu-id="75721-135">Gibt an, dass ein webhook-Empfänger erstellt werden soll</span><span class="sxs-lookup"><span data-stu-id="75721-135">Specifies to create a webhook receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75721-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75721-136">CommonParameters</span></span>
<span data-ttu-id="75721-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75721-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75721-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75721-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75721-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="75721-139">INPUTS</span></span>

### <span data-ttu-id="75721-140">System. String</span><span class="sxs-lookup"><span data-stu-id="75721-140">System.String</span></span>

### <span data-ttu-id="75721-141">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="75721-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="75721-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="75721-142">OUTPUTS</span></span>

### <span data-ttu-id="75721-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="75721-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="75721-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="75721-144">NOTES</span></span>

## <span data-ttu-id="75721-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="75721-145">RELATED LINKS</span></span>

<span data-ttu-id="75721-146">[Satz-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="75721-146">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>
