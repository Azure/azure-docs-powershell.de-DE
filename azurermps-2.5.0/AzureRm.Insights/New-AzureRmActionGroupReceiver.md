---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactiongroupreceiver
schema: 2.0.0
ms.openlocfilehash: 0f452818db1af3f3a69db58f82b89e6cfa8ee461
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848287"
---
# <span data-ttu-id="37a30-101">New-AzureRmActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="37a30-101">New-AzureRmActionGroupReceiver</span></span>

## <span data-ttu-id="37a30-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="37a30-102">SYNOPSIS</span></span>
<span data-ttu-id="37a30-103">Erstellt einen neuen Aktionsgruppen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="37a30-103">Creates an new action group receiver.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37a30-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="37a30-104">SYNTAX</span></span>

### <span data-ttu-id="37a30-105">NewEmailReceiver (Standard)</span><span class="sxs-lookup"><span data-stu-id="37a30-105">NewEmailReceiver (Default)</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37a30-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="37a30-106">NewSmsReceiver</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-SmsReceiver] [-CountryCode <String>] -PhoneNumber <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37a30-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="37a30-107">NewWebhookReceiver</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-WebhookReceiver] -ServiceUri <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37a30-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37a30-108">DESCRIPTION</span></span>
<span data-ttu-id="37a30-109">Das Cmdlet **New-AzureRmActionGroupReceiver** erstellt einen neuen Aktionsgruppen Empfänger im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="37a30-109">The **New-AzureRmActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="37a30-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37a30-110">EXAMPLES</span></span>

### <span data-ttu-id="37a30-111">Beispiel 1: Erstellen eines neuen e-Mail-Empfängers im Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="37a30-111">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzureRmActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="37a30-112">Dieser Befehl erstellt einen neuen e-Mail-Empfänger im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="37a30-112">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="37a30-113">Beispiel 2: Erstellen eines neuen SMS-Empfängers im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="37a30-113">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzureRmActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="37a30-114">Dieser Befehl erstellt einen neuen SMS-Empfänger im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="37a30-114">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="37a30-115">Beispiel 3: Erstellen eines neuen webhook-Receivers im Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="37a30-115">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzureRmActionGroupReceiver -Name 'webhookReceiver1' -SMSReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="37a30-116">Dieser Befehl erstellt einen neuen webhook-Empfänger im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="37a30-116">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="37a30-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="37a30-117">PARAMETERS</span></span>

### <span data-ttu-id="37a30-118">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="37a30-118">-CountryCode</span></span>
<span data-ttu-id="37a30-119">Gibt die Landesvorwahl für den SMS-Empfänger an.</span><span class="sxs-lookup"><span data-stu-id="37a30-119">Specifies the country code for the SMS receiver.</span></span>

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

### <span data-ttu-id="37a30-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37a30-120">-DefaultProfile</span></span>
<span data-ttu-id="37a30-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="37a30-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37a30-122">-Email-Email</span><span class="sxs-lookup"><span data-stu-id="37a30-122">-EmailAddress</span></span>
<span data-ttu-id="37a30-123">Gibt die Adresse des e-Mail-Empfängers an.</span><span class="sxs-lookup"><span data-stu-id="37a30-123">Specifies the address for the Email receiver.</span></span>

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

### <span data-ttu-id="37a30-124">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="37a30-124">-EmailReceiver</span></span>
<span data-ttu-id="37a30-125">Gibt an, dass ein e-Mail-Empfänger erstellt werden soll</span><span class="sxs-lookup"><span data-stu-id="37a30-125">Specifies to create an Email receiver</span></span>

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

### <span data-ttu-id="37a30-126">-Name</span><span class="sxs-lookup"><span data-stu-id="37a30-126">-Name</span></span>
<span data-ttu-id="37a30-127">Gibt den Namen des Empfängers an.</span><span class="sxs-lookup"><span data-stu-id="37a30-127">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="37a30-128">-Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="37a30-128">-PhoneNumber</span></span>
<span data-ttu-id="37a30-129">Gibt die Telefonnummer für den SMS-Empfänger an.</span><span class="sxs-lookup"><span data-stu-id="37a30-129">Specifies the phone number for the SMS receiver.</span></span>

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

### <span data-ttu-id="37a30-130">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="37a30-130">-ServiceUri</span></span>
<span data-ttu-id="37a30-131">Gibt den URI für den webhook-Empfänger an.</span><span class="sxs-lookup"><span data-stu-id="37a30-131">Specifies the URI for the webhook receiver.</span></span>

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

### <span data-ttu-id="37a30-132">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="37a30-132">-SmsReceiver</span></span>
<span data-ttu-id="37a30-133">Gibt an, dass ein SMS-Empfänger erstellt werden soll</span><span class="sxs-lookup"><span data-stu-id="37a30-133">Specifies to create a SMS receiver</span></span>

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

### <span data-ttu-id="37a30-134">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="37a30-134">-WebhookReceiver</span></span>
<span data-ttu-id="37a30-135">Gibt an, dass ein webhook-Empfänger erstellt werden soll</span><span class="sxs-lookup"><span data-stu-id="37a30-135">Specifies to create a webhook receiver</span></span>

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

### <span data-ttu-id="37a30-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37a30-136">CommonParameters</span></span>
<span data-ttu-id="37a30-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37a30-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37a30-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37a30-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37a30-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="37a30-139">INPUTS</span></span>

### <span data-ttu-id="37a30-140">System. String</span><span class="sxs-lookup"><span data-stu-id="37a30-140">System.String</span></span>

### <span data-ttu-id="37a30-141">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="37a30-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="37a30-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="37a30-142">OUTPUTS</span></span>

### <span data-ttu-id="37a30-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="37a30-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="37a30-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="37a30-144">NOTES</span></span>

## <span data-ttu-id="37a30-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="37a30-145">RELATED LINKS</span></span>

<span data-ttu-id="37a30-146">[Satz-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="37a30-146">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)</span></span>
