---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: 917f6287c40d4c26123217cccbf1dfc11866a488
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932568"
---
# <span data-ttu-id="89da1-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="89da1-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="89da1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89da1-102">SYNOPSIS</span></span>
<span data-ttu-id="89da1-103">Erstellt einen neuen Empfänger einer Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="89da1-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="89da1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89da1-104">SYNTAX</span></span>

### <span data-ttu-id="89da1-105">NewEmailReceiver (Standard)</span><span class="sxs-lookup"><span data-stu-id="89da1-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89da1-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="89da1-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-SmsReceiver] [-CountryCode <String>]
 -PhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89da1-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="89da1-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-WebhookReceiver] -ServiceUri <String>
 [-UseAadAuth] [-ObjectId <String>] [-IdentifierUri <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89da1-108">NewItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="89da1-108">NewItsmReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ItsmReceiver] -WorkspaceId <String>
 -ConnectionId <String> -TicketConfiguration <String> -Region <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89da1-109">NewVoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="89da1-109">NewVoiceReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-VoiceReceiver] [-VoiceCountryCode <String>]
 -VoicePhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89da1-110">NewArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="89da1-110">NewArmRoleReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ArmRoleReceiver] -RoleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89da1-111">NewAzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="89da1-111">NewAzureFunctionReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureFunctionReceiver]
 -FunctionAppResourceId <String> -HttpTriggerUrl <String> -FunctionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89da1-112">NewLogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="89da1-112">NewLogicAppReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-LogicAppReceiver] -ResourceId <String>
 -CallbackUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89da1-113">NewAutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="89da1-113">NewAutomationRunbookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AutomationRunbookReceiver]
 -AutomationAccountId <String> -RunbookName <String> [-IsGlobalRunbook] -AutomationRunbookServiceUri <String>
 -WebhookResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89da1-114">NewAzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="89da1-114">NewAzureAppPushReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureAppPushReceiver]
 -AzureAppPushEmailAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89da1-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="89da1-115">DESCRIPTION</span></span>
<span data-ttu-id="89da1-116">Das **Cmdlet New-AzActionGroupReceiver** erstellt einen neuen Aktionsgruppeempfänger im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="89da1-116">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="89da1-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="89da1-117">EXAMPLES</span></span>

### <span data-ttu-id="89da1-118">Beispiel 1: Erstellen eines neuen E-Mail-Empfängers im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="89da1-118">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="89da1-119">Mit diesem Befehl wird ein neuer E-Mail-Empfänger im Arbeitsspeicher erstellt.</span><span class="sxs-lookup"><span data-stu-id="89da1-119">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="89da1-120">Beispiel 2: Erstellen sie einen neuen SMS-Empfänger im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="89da1-120">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="89da1-121">Mit diesem Befehl wird ein neuer SMS-Empfänger im Arbeitsspeicher erstellt.</span><span class="sxs-lookup"><span data-stu-id="89da1-121">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="89da1-122">Beispiel 3: Erstellen eines neuen Webhookempfängers im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="89da1-122">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="89da1-123">Mit diesem Befehl wird ein neuer Webhookempfänger im Arbeitsspeicher erstellt.</span><span class="sxs-lookup"><span data-stu-id="89da1-123">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="89da1-124">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="89da1-124">PARAMETERS</span></span>

### <span data-ttu-id="89da1-125">-ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="89da1-125">-ArmRoleReceiver</span></span>
<span data-ttu-id="89da1-126">Erstellen eines ArmRoleReceivers</span><span class="sxs-lookup"><span data-stu-id="89da1-126">Create a ArmRoleReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewArmRoleReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89da1-127">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="89da1-127">-AutomationAccountId</span></span>
<span data-ttu-id="89da1-128">AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="89da1-128">the AutomationAccountId</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89da1-129">-AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="89da1-129">-AutomationRunbookReceiver</span></span>
<span data-ttu-id="89da1-130">Erstellen eines AutomationRunbookReceivers</span><span class="sxs-lookup"><span data-stu-id="89da1-130">Create a AutomationRunbookReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89da1-131">-AutomationRunbookServiceUri</span><span class="sxs-lookup"><span data-stu-id="89da1-131">-AutomationRunbookServiceUri</span></span>
<span data-ttu-id="89da1-132">der URI, in dem Webhooks gesendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="89da1-132">the URI where webhooks should be sent</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89da1-133">-AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="89da1-133">-AzureAppPushEmailAddress</span></span>
<span data-ttu-id="89da1-134">AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="89da1-134">the AzureAppPushEmailAddress</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureAppPushReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89da1-135">-AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="89da1-135">-AzureAppPushReceiver</span></span>
<span data-ttu-id="89da1-136">Erstellen eines AzureAppPushReceivers</span><span class="sxs-lookup"><span data-stu-id="89da1-136">Create a AzureAppPushReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAzureAppPushReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89da1-137">-AzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="89da1-137">-AzureFunctionReceiver</span></span>
<span data-ttu-id="89da1-138">Erstellen eines ArmRoleReceivers</span><span class="sxs-lookup"><span data-stu-id="89da1-138">Create a ArmRoleReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89da1-139">-CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="89da1-139">-CallbackUrl</span></span>
<span data-ttu-id="89da1-140">callbackUrl</span><span class="sxs-lookup"><span data-stu-id="89da1-140">the CallbackUrl</span></span>

```yaml
Type: System.String
Parameter Sets: NewLogicAppReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89da1-141">-ConnectionId</span><span class="sxs-lookup"><span data-stu-id="89da1-141">-ConnectionId</span></span>
<span data-ttu-id="89da1-142">die itsm-Verbindungs-ID dieses Empfängers</span><span class="sxs-lookup"><span data-stu-id="89da1-142">the itsm connection id of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89da1-143">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="89da1-143">-CountryCode</span></span>
<span data-ttu-id="89da1-144">Gibt die Ländercode für den SMS-Empfänger an.</span><span class="sxs-lookup"><span data-stu-id="89da1-144">Specifies the country code for the SMS receiver.</span></span>

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

### <span data-ttu-id="89da1-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89da1-145">-DefaultProfile</span></span>
<span data-ttu-id="89da1-146">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="89da1-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89da1-147">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="89da1-147">-EmailAddress</span></span>
<span data-ttu-id="89da1-148">Gibt die Adresse für den E-Mail-Empfänger an.</span><span class="sxs-lookup"><span data-stu-id="89da1-148">Specifies the address for the Email receiver.</span></span>

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

### <span data-ttu-id="89da1-149">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="89da1-149">-EmailReceiver</span></span>
<span data-ttu-id="89da1-150">Gibt an, dass ein E-Mail-Empfänger erstellt werden soll</span><span class="sxs-lookup"><span data-stu-id="89da1-150">Specifies to create an Email receiver</span></span>

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

### <span data-ttu-id="89da1-151">-FunctionAppResourceId</span><span class="sxs-lookup"><span data-stu-id="89da1-151">-FunctionAppResourceId</span></span>
<span data-ttu-id="89da1-152">die Funktion App resourceId</span><span class="sxs-lookup"><span data-stu-id="89da1-152">the function app resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89da1-153">-FunctionName</span><span class="sxs-lookup"><span data-stu-id="89da1-153">-FunctionName</span></span>
<span data-ttu-id="89da1-154">die FunktionName</span><span class="sxs-lookup"><span data-stu-id="89da1-154">the functionName</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89da1-155">-HttpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="89da1-155">-HttpTriggerUrl</span></span>
<span data-ttu-id="89da1-156">httpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="89da1-156">the httpTriggerUrl</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89da1-157">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="89da1-157">-IdentifierUri</span></span>
<span data-ttu-id="89da1-158">Der Bezeichner-URI für aad auth</span><span class="sxs-lookup"><span data-stu-id="89da1-158">the Identifier uri for aad auth</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89da1-159">-IsGlobalRunbook</span><span class="sxs-lookup"><span data-stu-id="89da1-159">-IsGlobalRunbook</span></span>
<span data-ttu-id="89da1-160">gibt an, ob es sich bei dieser Instanz um ein globales Runbook handelt</span><span class="sxs-lookup"><span data-stu-id="89da1-160">indicating whether this instance is global runbook</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89da1-161">-ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="89da1-161">-ItsmReceiver</span></span>
<span data-ttu-id="89da1-162">Erstellen eines ItsmReceivers</span><span class="sxs-lookup"><span data-stu-id="89da1-162">Create a ItsmReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewItsmReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89da1-163">-LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="89da1-163">-LogicAppReceiver</span></span>
<span data-ttu-id="89da1-164">Erstellen einer LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="89da1-164">Create a LogicAppReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewLogicAppReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89da1-165">-Name</span><span class="sxs-lookup"><span data-stu-id="89da1-165">-Name</span></span>
<span data-ttu-id="89da1-166">Gibt den Namen für den Empfänger an.</span><span class="sxs-lookup"><span data-stu-id="89da1-166">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="89da1-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="89da1-167">-ObjectId</span></span>
<span data-ttu-id="89da1-168">die Webhook-App-Objekt-ID für aad auth</span><span class="sxs-lookup"><span data-stu-id="89da1-168">the webhook app object Id for aad auth</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89da1-169">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="89da1-169">-PhoneNumber</span></span>
<span data-ttu-id="89da1-170">Gibt die Telefonnummer für den SMS-Empfänger an.</span><span class="sxs-lookup"><span data-stu-id="89da1-170">Specifies the phone number for the SMS receiver.</span></span>

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

### <span data-ttu-id="89da1-171">-Region</span><span class="sxs-lookup"><span data-stu-id="89da1-171">-Region</span></span>
<span data-ttu-id="89da1-172">der Itsm-Bereich dieses Empfängers</span><span class="sxs-lookup"><span data-stu-id="89da1-172">the itsm Region of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89da1-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89da1-173">-ResourceId</span></span>
<span data-ttu-id="89da1-174">ResourceId</span><span class="sxs-lookup"><span data-stu-id="89da1-174">the ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: NewLogicAppReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89da1-175">-RoleId</span><span class="sxs-lookup"><span data-stu-id="89da1-175">-RoleId</span></span>
<span data-ttu-id="89da1-176">Die Armrolle-ID des Empfängers</span><span class="sxs-lookup"><span data-stu-id="89da1-176">The arm role id of the receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewArmRoleReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89da1-177">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="89da1-177">-RunbookName</span></span>
<span data-ttu-id="89da1-178">runbookName</span><span class="sxs-lookup"><span data-stu-id="89da1-178">the RunbookName</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89da1-179">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="89da1-179">-ServiceUri</span></span>
<span data-ttu-id="89da1-180">Gibt den URI für den Webhookempfänger an.</span><span class="sxs-lookup"><span data-stu-id="89da1-180">Specifies the URI for the webhook receiver.</span></span>

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

### <span data-ttu-id="89da1-181">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="89da1-181">-SmsReceiver</span></span>
<span data-ttu-id="89da1-182">Gibt an, dass ein SMS-Empfänger erstellt werden soll</span><span class="sxs-lookup"><span data-stu-id="89da1-182">Specifies to create a SMS receiver</span></span>

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

### <span data-ttu-id="89da1-183">-TenantId</span><span class="sxs-lookup"><span data-stu-id="89da1-183">-TenantId</span></span>
<span data-ttu-id="89da1-184">Die Mandanten-ID für aad auth</span><span class="sxs-lookup"><span data-stu-id="89da1-184">the tenant id for aad auth</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89da1-185">-TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="89da1-185">-TicketConfiguration</span></span>
<span data-ttu-id="89da1-186">die itsm TicketConfiguration dieses Empfängers</span><span class="sxs-lookup"><span data-stu-id="89da1-186">the itsm TicketConfiguration of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89da1-187">-UseAadAuth</span><span class="sxs-lookup"><span data-stu-id="89da1-187">-UseAadAuth</span></span>
<span data-ttu-id="89da1-188">das Flag zum Verwenden von Add Auth</span><span class="sxs-lookup"><span data-stu-id="89da1-188">the flag to use add auth</span></span>

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

### <span data-ttu-id="89da1-189">-UseCommonAlertSchema</span><span class="sxs-lookup"><span data-stu-id="89da1-189">-UseCommonAlertSchema</span></span>
<span data-ttu-id="89da1-190">Gibt an, ob ein allgemeines Warnungsschema verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="89da1-190">The flag whether to use common alert schema .</span></span> <span data-ttu-id="89da1-191">Dieser Wert wird für SMS, Azure App Push, ITSM und Voice Recievers nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="89da1-191">This value will be neglectedfor SMS, Azure App push , ITSM and Voice recievers.</span></span>

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

### <span data-ttu-id="89da1-192">-VoiceCountryCode</span><span class="sxs-lookup"><span data-stu-id="89da1-192">-VoiceCountryCode</span></span>
<span data-ttu-id="89da1-193">Die Ländercode des Sprachempfängers</span><span class="sxs-lookup"><span data-stu-id="89da1-193">The country code of the voice receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewVoiceReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89da1-194">-VoicePhoneNumber</span><span class="sxs-lookup"><span data-stu-id="89da1-194">-VoicePhoneNumber</span></span>
<span data-ttu-id="89da1-195">Die Telefonnummer des Sprachempfängers</span><span class="sxs-lookup"><span data-stu-id="89da1-195">The phone number of the voice receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewVoiceReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89da1-196">-VoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="89da1-196">-VoiceReceiver</span></span>
<span data-ttu-id="89da1-197">Erstellen eines Sprachempfängers</span><span class="sxs-lookup"><span data-stu-id="89da1-197">Create a voice receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewVoiceReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89da1-198">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="89da1-198">-WebhookReceiver</span></span>
<span data-ttu-id="89da1-199">Gibt an, dass ein Webhookempfänger erstellt werden soll</span><span class="sxs-lookup"><span data-stu-id="89da1-199">Specifies to create a webhook receiver</span></span>

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

### <span data-ttu-id="89da1-200">-WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="89da1-200">-WebhookResourceId</span></span>
<span data-ttu-id="89da1-201">webhookResourceId</span><span class="sxs-lookup"><span data-stu-id="89da1-201">the WebhookResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89da1-202">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="89da1-202">-WorkspaceId</span></span>
<span data-ttu-id="89da1-203">die id des itsm-Arbeitsbereichs dieses Empfängers</span><span class="sxs-lookup"><span data-stu-id="89da1-203">the itsm workspace id of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89da1-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89da1-204">CommonParameters</span></span>
<span data-ttu-id="89da1-205">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89da1-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89da1-206">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89da1-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89da1-207">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="89da1-207">INPUTS</span></span>

### <span data-ttu-id="89da1-208">System.String</span><span class="sxs-lookup"><span data-stu-id="89da1-208">System.String</span></span>

### <span data-ttu-id="89da1-209">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="89da1-209">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="89da1-210">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="89da1-210">OUTPUTS</span></span>

### <span data-ttu-id="89da1-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="89da1-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="89da1-212">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="89da1-212">NOTES</span></span>

## <span data-ttu-id="89da1-213">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="89da1-213">RELATED LINKS</span></span>

<span data-ttu-id="89da1-214">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="89da1-214">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>
