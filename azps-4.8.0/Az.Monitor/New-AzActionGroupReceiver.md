---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: f2862c08212f5e41de10cb600edb22c38eac68d4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166512"
---
# <span data-ttu-id="67911-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="67911-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="67911-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="67911-102">SYNOPSIS</span></span>
<span data-ttu-id="67911-103">Erstellt einen neuen Aktionsgruppen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="67911-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="67911-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="67911-104">SYNTAX</span></span>

### <span data-ttu-id="67911-105">NewEmailReceiver (Standard)</span><span class="sxs-lookup"><span data-stu-id="67911-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67911-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="67911-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-SmsReceiver] [-CountryCode <String>]
 -PhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67911-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="67911-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-WebhookReceiver] -ServiceUri <String>
 [-UseAadAuth] [-ObjectId <String>] [-IdentifierUri <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67911-108">NewItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="67911-108">NewItsmReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ItsmReceiver] -WorkspaceId <String>
 -ConnectionId <String> -TicketConfiguration <String> -Region <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67911-109">NewVoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="67911-109">NewVoiceReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-VoiceReceiver] [-VoiceCountryCode <String>]
 -VoicePhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67911-110">NewArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="67911-110">NewArmRoleReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ArmRoleReceiver] -RoleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67911-111">NewAzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="67911-111">NewAzureFunctionReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureFunctionReceiver]
 -FunctionAppResourceId <String> -HttpTriggerUrl <String> -FunctionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67911-112">NewLogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="67911-112">NewLogicAppReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-LogicAppReceiver] -ResourceId <String>
 -CallbackUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67911-113">NewAutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="67911-113">NewAutomationRunbookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AutomationRunbookReceiver]
 -AutomationAccountId <String> -RunbookName <String> [-IsGlobalRunbook] -AutomationRunbookServiceUri <String>
 -WebhookResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67911-114">NewAzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="67911-114">NewAzureAppPushReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureAppPushReceiver]
 -AzureAppPushEmailAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67911-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="67911-115">DESCRIPTION</span></span>
<span data-ttu-id="67911-116">Das Cmdlet **New-AzActionGroupReceiver** erstellt einen neuen Aktionsgruppen Empfänger im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="67911-116">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="67911-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="67911-117">EXAMPLES</span></span>

### <span data-ttu-id="67911-118">Beispiel 1: Erstellen eines neuen e-Mail-Empfängers im Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="67911-118">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="67911-119">Dieser Befehl erstellt einen neuen e-Mail-Empfänger im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="67911-119">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="67911-120">Beispiel 2: Erstellen eines neuen SMS-Empfängers im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="67911-120">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="67911-121">Dieser Befehl erstellt einen neuen SMS-Empfänger im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="67911-121">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="67911-122">Beispiel 3: Erstellen eines neuen webhook-Receivers im Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="67911-122">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="67911-123">Dieser Befehl erstellt einen neuen webhook-Empfänger im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="67911-123">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="67911-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="67911-124">PARAMETERS</span></span>

### <span data-ttu-id="67911-125">-ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="67911-125">-ArmRoleReceiver</span></span>
<span data-ttu-id="67911-126">Erstellen eines ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="67911-126">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="67911-127">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="67911-127">-AutomationAccountId</span></span>
<span data-ttu-id="67911-128">die AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="67911-128">the AutomationAccountId</span></span>

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

### <span data-ttu-id="67911-129">-AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="67911-129">-AutomationRunbookReceiver</span></span>
<span data-ttu-id="67911-130">Erstellen eines AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="67911-130">Create a AutomationRunbookReceiver</span></span>

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

### <span data-ttu-id="67911-131">-AutomationRunbookServiceUri</span><span class="sxs-lookup"><span data-stu-id="67911-131">-AutomationRunbookServiceUri</span></span>
<span data-ttu-id="67911-132">der URI, in dem webhooks gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="67911-132">the URI where webhooks should be sent</span></span>

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

### <span data-ttu-id="67911-133">-AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="67911-133">-AzureAppPushEmailAddress</span></span>
<span data-ttu-id="67911-134">die AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="67911-134">the AzureAppPushEmailAddress</span></span>

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

### <span data-ttu-id="67911-135">-AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="67911-135">-AzureAppPushReceiver</span></span>
<span data-ttu-id="67911-136">Erstellen eines AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="67911-136">Create a AzureAppPushReceiver</span></span>

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

### <span data-ttu-id="67911-137">-AzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="67911-137">-AzureFunctionReceiver</span></span>
<span data-ttu-id="67911-138">Erstellen eines ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="67911-138">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="67911-139">-CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="67911-139">-CallbackUrl</span></span>
<span data-ttu-id="67911-140">die CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="67911-140">the CallbackUrl</span></span>

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

### <span data-ttu-id="67911-141">-Verbindungs-Nr</span><span class="sxs-lookup"><span data-stu-id="67911-141">-ConnectionId</span></span>
<span data-ttu-id="67911-142">die ITSM-Verbindungs-ID dieses Receivers</span><span class="sxs-lookup"><span data-stu-id="67911-142">the itsm connection id of this receiver</span></span>

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

### <span data-ttu-id="67911-143">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="67911-143">-CountryCode</span></span>
<span data-ttu-id="67911-144">Gibt die Landesvorwahl für den SMS-Empfänger an.</span><span class="sxs-lookup"><span data-stu-id="67911-144">Specifies the country code for the SMS receiver.</span></span>

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

### <span data-ttu-id="67911-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67911-145">-DefaultProfile</span></span>
<span data-ttu-id="67911-146">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="67911-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67911-147">-Email-Email</span><span class="sxs-lookup"><span data-stu-id="67911-147">-EmailAddress</span></span>
<span data-ttu-id="67911-148">Gibt die Adresse des e-Mail-Empfängers an.</span><span class="sxs-lookup"><span data-stu-id="67911-148">Specifies the address for the Email receiver.</span></span>

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

### <span data-ttu-id="67911-149">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="67911-149">-EmailReceiver</span></span>
<span data-ttu-id="67911-150">Gibt an, dass ein e-Mail-Empfänger erstellt werden soll</span><span class="sxs-lookup"><span data-stu-id="67911-150">Specifies to create an Email receiver</span></span>

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

### <span data-ttu-id="67911-151">-FunctionAppResourceId</span><span class="sxs-lookup"><span data-stu-id="67911-151">-FunctionAppResourceId</span></span>
<span data-ttu-id="67911-152">die Funktions-APP-Quell Code Funktion</span><span class="sxs-lookup"><span data-stu-id="67911-152">the function app resourceId</span></span>

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

### <span data-ttu-id="67911-153">-FunctionName</span><span class="sxs-lookup"><span data-stu-id="67911-153">-FunctionName</span></span>
<span data-ttu-id="67911-154">der Funktionsname</span><span class="sxs-lookup"><span data-stu-id="67911-154">the functionName</span></span>

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

### <span data-ttu-id="67911-155">-HttpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="67911-155">-HttpTriggerUrl</span></span>
<span data-ttu-id="67911-156">die httpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="67911-156">the httpTriggerUrl</span></span>

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

### <span data-ttu-id="67911-157">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="67911-157">-IdentifierUri</span></span>
<span data-ttu-id="67911-158">der Bezeichner-URI für Aad auth</span><span class="sxs-lookup"><span data-stu-id="67911-158">the Identifier uri for aad auth</span></span>

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

### <span data-ttu-id="67911-159">-IsGlobalRunbook</span><span class="sxs-lookup"><span data-stu-id="67911-159">-IsGlobalRunbook</span></span>
<span data-ttu-id="67911-160">Gibt an, ob es sich bei dieser Instanz um eine globale runbooks</span><span class="sxs-lookup"><span data-stu-id="67911-160">indicating whether this instance is global runbook</span></span>

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

### <span data-ttu-id="67911-161">-ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="67911-161">-ItsmReceiver</span></span>
<span data-ttu-id="67911-162">Erstellen eines ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="67911-162">Create a ItsmReceiver</span></span>

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

### <span data-ttu-id="67911-163">-LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="67911-163">-LogicAppReceiver</span></span>
<span data-ttu-id="67911-164">Erstellen eines LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="67911-164">Create a LogicAppReceiver</span></span>

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

### <span data-ttu-id="67911-165">-Name</span><span class="sxs-lookup"><span data-stu-id="67911-165">-Name</span></span>
<span data-ttu-id="67911-166">Gibt den Namen des Empfängers an.</span><span class="sxs-lookup"><span data-stu-id="67911-166">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="67911-167">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="67911-167">-ObjectId</span></span>
<span data-ttu-id="67911-168">die webhook-App-Objekt-ID für Aad auth</span><span class="sxs-lookup"><span data-stu-id="67911-168">the webhook app object Id for aad auth</span></span>

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

### <span data-ttu-id="67911-169">-Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="67911-169">-PhoneNumber</span></span>
<span data-ttu-id="67911-170">Gibt die Telefonnummer für den SMS-Empfänger an.</span><span class="sxs-lookup"><span data-stu-id="67911-170">Specifies the phone number for the SMS receiver.</span></span>

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

### <span data-ttu-id="67911-171">-Region</span><span class="sxs-lookup"><span data-stu-id="67911-171">-Region</span></span>
<span data-ttu-id="67911-172">der ITSM-Bereich dieses Receivers</span><span class="sxs-lookup"><span data-stu-id="67911-172">the itsm Region of this receiver</span></span>

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

### <span data-ttu-id="67911-173">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="67911-173">-ResourceId</span></span>
<span data-ttu-id="67911-174">die Resourcen--Nr</span><span class="sxs-lookup"><span data-stu-id="67911-174">the ResourceId</span></span>

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

### <span data-ttu-id="67911-175">-Role-Nr</span><span class="sxs-lookup"><span data-stu-id="67911-175">-RoleId</span></span>
<span data-ttu-id="67911-176">Die Arm-Rollen-ID des Empfängers</span><span class="sxs-lookup"><span data-stu-id="67911-176">The arm role id of the receiver</span></span>

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

### <span data-ttu-id="67911-177">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="67911-177">-RunbookName</span></span>
<span data-ttu-id="67911-178">die RunbookName</span><span class="sxs-lookup"><span data-stu-id="67911-178">the RunbookName</span></span>

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

### <span data-ttu-id="67911-179">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="67911-179">-ServiceUri</span></span>
<span data-ttu-id="67911-180">Gibt den URI für den webhook-Empfänger an.</span><span class="sxs-lookup"><span data-stu-id="67911-180">Specifies the URI for the webhook receiver.</span></span>

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

### <span data-ttu-id="67911-181">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="67911-181">-SmsReceiver</span></span>
<span data-ttu-id="67911-182">Gibt an, dass ein SMS-Empfänger erstellt werden soll</span><span class="sxs-lookup"><span data-stu-id="67911-182">Specifies to create a SMS receiver</span></span>

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

### <span data-ttu-id="67911-183">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="67911-183">-TenantId</span></span>
<span data-ttu-id="67911-184">die Mandanten-ID für Aad auth</span><span class="sxs-lookup"><span data-stu-id="67911-184">the tenant id for aad auth</span></span>

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

### <span data-ttu-id="67911-185">-TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="67911-185">-TicketConfiguration</span></span>
<span data-ttu-id="67911-186">der ITSM-TicketConfiguration dieses Receivers</span><span class="sxs-lookup"><span data-stu-id="67911-186">the itsm TicketConfiguration of this receiver</span></span>

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

### <span data-ttu-id="67911-187">-UseAadAuth</span><span class="sxs-lookup"><span data-stu-id="67911-187">-UseAadAuth</span></span>
<span data-ttu-id="67911-188">das zu verwendende Flag zum Hinzufügen von auth</span><span class="sxs-lookup"><span data-stu-id="67911-188">the flag to use add auth</span></span>

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

### <span data-ttu-id="67911-189">-UseCommonAlertSchema</span><span class="sxs-lookup"><span data-stu-id="67911-189">-UseCommonAlertSchema</span></span>
<span data-ttu-id="67911-190">Das Kennzeichen, ob ein allgemeines Warnungs Schema verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="67911-190">The flag whether to use common alert schema .</span></span> <span data-ttu-id="67911-191">Dieser Wert wird neglectedfor SMS, Azure App Push, ITSM und Voice Receivers sein.</span><span class="sxs-lookup"><span data-stu-id="67911-191">This value will be neglectedfor SMS, Azure App push , ITSM and Voice recievers.</span></span>

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

### <span data-ttu-id="67911-192">-VoiceCountryCode</span><span class="sxs-lookup"><span data-stu-id="67911-192">-VoiceCountryCode</span></span>
<span data-ttu-id="67911-193">Die Landesvorwahl des Voice-Receivers</span><span class="sxs-lookup"><span data-stu-id="67911-193">The country code of the voice receiver</span></span>

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

### <span data-ttu-id="67911-194">-VoicePhoneNumber</span><span class="sxs-lookup"><span data-stu-id="67911-194">-VoicePhoneNumber</span></span>
<span data-ttu-id="67911-195">Die Telefonnummer des sprach Empfängers</span><span class="sxs-lookup"><span data-stu-id="67911-195">The phone number of the voice receiver</span></span>

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

### <span data-ttu-id="67911-196">-VoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="67911-196">-VoiceReceiver</span></span>
<span data-ttu-id="67911-197">Erstellen eines sprach Empfängers</span><span class="sxs-lookup"><span data-stu-id="67911-197">Create a voice receiver</span></span>

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

### <span data-ttu-id="67911-198">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="67911-198">-WebhookReceiver</span></span>
<span data-ttu-id="67911-199">Gibt an, dass ein webhook-Empfänger erstellt werden soll</span><span class="sxs-lookup"><span data-stu-id="67911-199">Specifies to create a webhook receiver</span></span>

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

### <span data-ttu-id="67911-200">-WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="67911-200">-WebhookResourceId</span></span>
<span data-ttu-id="67911-201">die WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="67911-201">the WebhookResourceId</span></span>

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

### <span data-ttu-id="67911-202">-Arbeitsbereichs-Nr</span><span class="sxs-lookup"><span data-stu-id="67911-202">-WorkspaceId</span></span>
<span data-ttu-id="67911-203">die ITSM-Arbeitsbereichs-ID dieses Receivers</span><span class="sxs-lookup"><span data-stu-id="67911-203">the itsm workspace id of this receiver</span></span>

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

### <span data-ttu-id="67911-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67911-204">CommonParameters</span></span>
<span data-ttu-id="67911-205">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67911-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67911-206">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67911-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67911-207">Eingaben</span><span class="sxs-lookup"><span data-stu-id="67911-207">INPUTS</span></span>

### <span data-ttu-id="67911-208">System. String</span><span class="sxs-lookup"><span data-stu-id="67911-208">System.String</span></span>

### <span data-ttu-id="67911-209">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="67911-209">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="67911-210">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="67911-210">OUTPUTS</span></span>

### <span data-ttu-id="67911-211">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="67911-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="67911-212">Notizen</span><span class="sxs-lookup"><span data-stu-id="67911-212">NOTES</span></span>

## <span data-ttu-id="67911-213">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="67911-213">RELATED LINKS</span></span>

<span data-ttu-id="67911-214">[Satz-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="67911-214">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>
