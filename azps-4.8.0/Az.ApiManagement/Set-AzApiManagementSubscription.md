---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
ms.openlocfilehash: 82c49524566293adcd8dcbdcb36359e83360158c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167360"
---
# <span data-ttu-id="7da46-101">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7da46-101">Set-AzApiManagementSubscription</span></span>

## <span data-ttu-id="7da46-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7da46-102">SYNOPSIS</span></span>
<span data-ttu-id="7da46-103">Legt vorhandene Abonnementdetails fest.</span><span class="sxs-lookup"><span data-stu-id="7da46-103">Sets existing subscription details.</span></span>

## <span data-ttu-id="7da46-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7da46-104">SYNTAX</span></span>

### <span data-ttu-id="7da46-105">ByInputObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="7da46-105">ByInputObject (Default)</span></span>
```
Set-AzApiManagementSubscription -InputObject <PsApiManagementSubscription> [-Scope <String>] [-UserId <String>]
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7da46-106">Expanded</span><span class="sxs-lookup"><span data-stu-id="7da46-106">ExpandedParameter</span></span>
```
Set-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-Scope <String>]
 [-UserId <String>] [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7da46-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7da46-107">DESCRIPTION</span></span>
<span data-ttu-id="7da46-108">Das Cmdlet " **Set-AzApiManagementSubscription** " legt vorhandene Abonnementdetails fest.</span><span class="sxs-lookup"><span data-stu-id="7da46-108">The **Set-AzApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="7da46-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7da46-109">EXAMPLES</span></span>

### <span data-ttu-id="7da46-110">Beispiel 1: Festlegen des Zustands und der primären und sekundären Schlüssel für ein Abonnement</span><span class="sxs-lookup"><span data-stu-id="7da46-110">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="7da46-111">Mit diesem Befehl werden die primären und sekundären Schlüssel für ein Abonnement festgelegt und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7da46-111">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="7da46-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7da46-112">PARAMETERS</span></span>

### <span data-ttu-id="7da46-113">-Context</span><span class="sxs-lookup"><span data-stu-id="7da46-113">-Context</span></span>
<span data-ttu-id="7da46-114">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="7da46-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7da46-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7da46-115">-DefaultProfile</span></span>
<span data-ttu-id="7da46-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7da46-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7da46-117">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="7da46-117">-ExpiresOn</span></span>
<span data-ttu-id="7da46-118">Gibt das Ablaufdatum eines Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="7da46-118">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="7da46-119">Der Standardwert für diesen Parameter ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="7da46-119">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7da46-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7da46-120">-InputObject</span></span>
<span data-ttu-id="7da46-121">Instanz von PsApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="7da46-121">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="7da46-122">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7da46-122">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7da46-123">-Name</span><span class="sxs-lookup"><span data-stu-id="7da46-123">-Name</span></span>
<span data-ttu-id="7da46-124">Gibt einen Abonnement Namen an.</span><span class="sxs-lookup"><span data-stu-id="7da46-124">Specifies a subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7da46-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7da46-125">-PassThru</span></span>
<span data-ttu-id="7da46-126">passthru</span><span class="sxs-lookup"><span data-stu-id="7da46-126">passthru</span></span>

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

### <span data-ttu-id="7da46-127">-Primär Primär</span><span class="sxs-lookup"><span data-stu-id="7da46-127">-PrimaryKey</span></span>
<span data-ttu-id="7da46-128">Gibt den Primärschlüssel des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="7da46-128">Specifies the subscription primary key.</span></span>
<span data-ttu-id="7da46-129">Dieser Parameter wird automatisch generiert, wenn er nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7da46-129">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="7da46-130">Dieser Parameter muss 1 bis 300 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="7da46-130">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7da46-131">-Scope</span><span class="sxs-lookup"><span data-stu-id="7da46-131">-Scope</span></span>
<span data-ttu-id="7da46-132">Der Umfang des Abonnements, unabhängig davon, ob es sich um einen API-Bereich/APIs/{apiId} oder um einen Produktbereich handelt/Products/{ProductID} oder globaler API-Bereich/APIs oder globaler Bereich/.</span><span class="sxs-lookup"><span data-stu-id="7da46-132">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="7da46-133">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7da46-133">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7da46-134">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="7da46-134">-SecondaryKey</span></span>
<span data-ttu-id="7da46-135">Gibt den Sekundärschlüssel des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="7da46-135">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="7da46-136">Dieser Parameter wird automatisch generiert, wenn er nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7da46-136">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="7da46-137">Dieser Parameter muss 1 bis 300 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="7da46-137">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7da46-138">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="7da46-138">-State</span></span>
<span data-ttu-id="7da46-139">Gibt den Status des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="7da46-139">Specifies the subscription state.</span></span>
<span data-ttu-id="7da46-140">Der Standardwert für diesen Parameter ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="7da46-140">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState]
Parameter Sets: (All)
Aliases:
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7da46-141">-StateComment</span><span class="sxs-lookup"><span data-stu-id="7da46-141">-StateComment</span></span>
<span data-ttu-id="7da46-142">Gibt den Status Kommentar des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="7da46-142">Specifies the subscription state comment.</span></span>
<span data-ttu-id="7da46-143">Der Standardwert für diesen Parameter ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="7da46-143">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7da46-144">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="7da46-144">-SubscriptionId</span></span>
<span data-ttu-id="7da46-145">Gibt die Abonnement-ID an.</span><span class="sxs-lookup"><span data-stu-id="7da46-145">Specifies the subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7da46-146">-UserID</span><span class="sxs-lookup"><span data-stu-id="7da46-146">-UserId</span></span>
<span data-ttu-id="7da46-147">Der Besitzer des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="7da46-147">The owner of the subscription.</span></span> <span data-ttu-id="7da46-148">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="7da46-148">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7da46-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7da46-149">-Confirm</span></span>
<span data-ttu-id="7da46-150">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7da46-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7da46-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7da46-151">-WhatIf</span></span>
<span data-ttu-id="7da46-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7da46-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7da46-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7da46-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7da46-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7da46-154">CommonParameters</span></span>
<span data-ttu-id="7da46-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7da46-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7da46-156">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7da46-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7da46-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7da46-157">INPUTS</span></span>

### <span data-ttu-id="7da46-158">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7da46-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7da46-159">System. String</span><span class="sxs-lookup"><span data-stu-id="7da46-159">System.String</span></span>

### <span data-ttu-id="7da46-160">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSubscriptionState, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement. Servicemanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7da46-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="7da46-161">System. Nullable ' 1 [[System. DateTime, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7da46-161">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7da46-162">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="7da46-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7da46-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7da46-163">OUTPUTS</span></span>

### <span data-ttu-id="7da46-164">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7da46-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="7da46-165">Notizen</span><span class="sxs-lookup"><span data-stu-id="7da46-165">NOTES</span></span>

## <span data-ttu-id="7da46-166">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7da46-166">RELATED LINKS</span></span>

[<span data-ttu-id="7da46-167">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7da46-167">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="7da46-168">Neu – AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7da46-168">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="7da46-169">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7da46-169">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)


