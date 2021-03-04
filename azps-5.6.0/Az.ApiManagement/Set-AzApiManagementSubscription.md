---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
ms.openlocfilehash: aea1b80507b753a84afd9228c4845da973273a37
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932107"
---
# <span data-ttu-id="ec2fb-101">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ec2fb-101">Set-AzApiManagementSubscription</span></span>

## <span data-ttu-id="ec2fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec2fb-102">SYNOPSIS</span></span>
<span data-ttu-id="ec2fb-103">Legt vorhandene Abonnementdetails fest.</span><span class="sxs-lookup"><span data-stu-id="ec2fb-103">Sets existing subscription details.</span></span>

## <span data-ttu-id="ec2fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ec2fb-104">SYNTAX</span></span>

### <span data-ttu-id="ec2fb-105">ByInputObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="ec2fb-105">ByInputObject (Default)</span></span>
```
Set-AzApiManagementSubscription -InputObject <PsApiManagementSubscription> [-Scope <String>] [-UserId <String>]
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec2fb-106">ExpandedParameter</span><span class="sxs-lookup"><span data-stu-id="ec2fb-106">ExpandedParameter</span></span>
```
Set-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-Scope <String>]
 [-UserId <String>] [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec2fb-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ec2fb-107">DESCRIPTION</span></span>
<span data-ttu-id="ec2fb-108">Das **Cmdlet Set-AzApiManagementSubscription** legt vorhandene Abonnementdetails fest.</span><span class="sxs-lookup"><span data-stu-id="ec2fb-108">The **Set-AzApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="ec2fb-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ec2fb-109">EXAMPLES</span></span>

### <span data-ttu-id="ec2fb-110">Beispiel 1: Festlegen des Zustands sowie von Primär- und Sekundärschlüsseln für ein Abonnement</span><span class="sxs-lookup"><span data-stu-id="ec2fb-110">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="ec2fb-111">Mit diesem Befehl werden die primären und sekundären Schlüssel für ein Abonnement bestimmt und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ec2fb-111">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="ec2fb-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ec2fb-112">PARAMETERS</span></span>

### <span data-ttu-id="ec2fb-113">-Context</span><span class="sxs-lookup"><span data-stu-id="ec2fb-113">-Context</span></span>
<span data-ttu-id="ec2fb-114">Gibt ein **PsApiManagementContext-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="ec2fb-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ec2fb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec2fb-115">-DefaultProfile</span></span>
<span data-ttu-id="ec2fb-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ec2fb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec2fb-117">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="ec2fb-117">-ExpiresOn</span></span>
<span data-ttu-id="ec2fb-118">Gibt ein Ablaufdatum für ein Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="ec2fb-118">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="ec2fb-119">Der Standardwert dieses Parameters ist $Null.</span><span class="sxs-lookup"><span data-stu-id="ec2fb-119">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="ec2fb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec2fb-120">-InputObject</span></span>
<span data-ttu-id="ec2fb-121">Instanz von PsApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="ec2fb-121">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="ec2fb-122">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ec2fb-122">This parameter is required.</span></span>

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

### <span data-ttu-id="ec2fb-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ec2fb-123">-Name</span></span>
<span data-ttu-id="ec2fb-124">Gibt einen Abonnementnamen an.</span><span class="sxs-lookup"><span data-stu-id="ec2fb-124">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="ec2fb-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec2fb-125">-PassThru</span></span>
<span data-ttu-id="ec2fb-126">passthru</span><span class="sxs-lookup"><span data-stu-id="ec2fb-126">passthru</span></span>

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

### <span data-ttu-id="ec2fb-127">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="ec2fb-127">-PrimaryKey</span></span>
<span data-ttu-id="ec2fb-128">Gibt den Primärschlüssel des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="ec2fb-128">Specifies the subscription primary key.</span></span>
<span data-ttu-id="ec2fb-129">Dieser Parameter wird automatisch generiert, wenn er nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ec2fb-129">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="ec2fb-130">Dieser Parameter muss 1 bis 300 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="ec2fb-130">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="ec2fb-131">-Scope</span><span class="sxs-lookup"><span data-stu-id="ec2fb-131">-Scope</span></span>
<span data-ttu-id="ec2fb-132">Der Umfang des Abonnements, unabhängig davon, ob es sich um api scope /apis/{apiId} oder Product Scope /products/{productId} oder Global API Scope /apis oder Global scope /handelt.</span><span class="sxs-lookup"><span data-stu-id="ec2fb-132">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="ec2fb-133">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ec2fb-133">This parameter is required.</span></span>

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

### <span data-ttu-id="ec2fb-134">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="ec2fb-134">-SecondaryKey</span></span>
<span data-ttu-id="ec2fb-135">Gibt den sekundären Abonnementschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="ec2fb-135">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="ec2fb-136">Dieser Parameter wird automatisch generiert, wenn er nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ec2fb-136">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="ec2fb-137">Dieser Parameter muss 1 bis 300 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="ec2fb-137">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="ec2fb-138">-State</span><span class="sxs-lookup"><span data-stu-id="ec2fb-138">-State</span></span>
<span data-ttu-id="ec2fb-139">Gibt den Abonnementstatus an.</span><span class="sxs-lookup"><span data-stu-id="ec2fb-139">Specifies the subscription state.</span></span>
<span data-ttu-id="ec2fb-140">Der Standardwert dieses Parameters ist $Null.</span><span class="sxs-lookup"><span data-stu-id="ec2fb-140">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="ec2fb-141">-StateComment</span><span class="sxs-lookup"><span data-stu-id="ec2fb-141">-StateComment</span></span>
<span data-ttu-id="ec2fb-142">Gibt den Kommentar zum Abonnementstatus an.</span><span class="sxs-lookup"><span data-stu-id="ec2fb-142">Specifies the subscription state comment.</span></span>
<span data-ttu-id="ec2fb-143">Der Standardwert dieses Parameters ist $Null.</span><span class="sxs-lookup"><span data-stu-id="ec2fb-143">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="ec2fb-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ec2fb-144">-SubscriptionId</span></span>
<span data-ttu-id="ec2fb-145">Gibt die Abonnement-ID an.</span><span class="sxs-lookup"><span data-stu-id="ec2fb-145">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="ec2fb-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="ec2fb-146">-UserId</span></span>
<span data-ttu-id="ec2fb-147">Der Besitzer des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="ec2fb-147">The owner of the subscription.</span></span> <span data-ttu-id="ec2fb-148">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="ec2fb-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="ec2fb-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ec2fb-149">-Confirm</span></span>
<span data-ttu-id="ec2fb-150">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ec2fb-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec2fb-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec2fb-151">-WhatIf</span></span>
<span data-ttu-id="ec2fb-152">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ec2fb-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ec2fb-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ec2fb-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec2fb-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec2fb-154">CommonParameters</span></span>
<span data-ttu-id="ec2fb-155">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec2fb-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec2fb-156">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec2fb-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec2fb-157">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ec2fb-157">INPUTS</span></span>

### <span data-ttu-id="ec2fb-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ec2fb-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ec2fb-159">System.String</span><span class="sxs-lookup"><span data-stu-id="ec2fb-159">System.String</span></span>

### <span data-ttu-id="ec2fb-160">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="ec2fb-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="ec2fb-161">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ec2fb-161">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ec2fb-162">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ec2fb-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ec2fb-163">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ec2fb-163">OUTPUTS</span></span>

### <span data-ttu-id="ec2fb-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ec2fb-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="ec2fb-165">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ec2fb-165">NOTES</span></span>

## <span data-ttu-id="ec2fb-166">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ec2fb-166">RELATED LINKS</span></span>

[<span data-ttu-id="ec2fb-167">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ec2fb-167">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="ec2fb-168">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ec2fb-168">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="ec2fb-169">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ec2fb-169">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)


