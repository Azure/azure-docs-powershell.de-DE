---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
ms.openlocfilehash: 82c49524566293adcd8dcbdcb36359e83360158c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179927"
---
# <span data-ttu-id="2551d-101">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2551d-101">Set-AzApiManagementSubscription</span></span>

## <span data-ttu-id="2551d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2551d-102">SYNOPSIS</span></span>
<span data-ttu-id="2551d-103">Legt vorhandene Abonnementdetails fest.</span><span class="sxs-lookup"><span data-stu-id="2551d-103">Sets existing subscription details.</span></span>

## <span data-ttu-id="2551d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2551d-104">SYNTAX</span></span>

### <span data-ttu-id="2551d-105">ByInputObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="2551d-105">ByInputObject (Default)</span></span>
```
Set-AzApiManagementSubscription -InputObject <PsApiManagementSubscription> [-Scope <String>] [-UserId <String>]
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2551d-106">Expanded</span><span class="sxs-lookup"><span data-stu-id="2551d-106">ExpandedParameter</span></span>
```
Set-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-Scope <String>]
 [-UserId <String>] [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2551d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2551d-107">DESCRIPTION</span></span>
<span data-ttu-id="2551d-108">Das Cmdlet " **Set-AzApiManagementSubscription** " legt vorhandene Abonnementdetails fest.</span><span class="sxs-lookup"><span data-stu-id="2551d-108">The **Set-AzApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="2551d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2551d-109">EXAMPLES</span></span>

### <span data-ttu-id="2551d-110">Beispiel 1: Festlegen des Zustands und der primären und sekundären Schlüssel für ein Abonnement</span><span class="sxs-lookup"><span data-stu-id="2551d-110">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="2551d-111">Mit diesem Befehl werden die primären und sekundären Schlüssel für ein Abonnement festgelegt und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2551d-111">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="2551d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2551d-112">PARAMETERS</span></span>

### <span data-ttu-id="2551d-113">-Context</span><span class="sxs-lookup"><span data-stu-id="2551d-113">-Context</span></span>
<span data-ttu-id="2551d-114">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="2551d-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2551d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2551d-115">-DefaultProfile</span></span>
<span data-ttu-id="2551d-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2551d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2551d-117">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="2551d-117">-ExpiresOn</span></span>
<span data-ttu-id="2551d-118">Gibt das Ablaufdatum eines Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="2551d-118">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="2551d-119">Der Standardwert für diesen Parameter ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="2551d-119">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="2551d-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2551d-120">-InputObject</span></span>
<span data-ttu-id="2551d-121">Instanz von PsApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="2551d-121">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="2551d-122">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2551d-122">This parameter is required.</span></span>

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

### <span data-ttu-id="2551d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2551d-123">-Name</span></span>
<span data-ttu-id="2551d-124">Gibt einen Abonnement Namen an.</span><span class="sxs-lookup"><span data-stu-id="2551d-124">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="2551d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2551d-125">-PassThru</span></span>
<span data-ttu-id="2551d-126">passthru</span><span class="sxs-lookup"><span data-stu-id="2551d-126">passthru</span></span>

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

### <span data-ttu-id="2551d-127">-Primär Primär</span><span class="sxs-lookup"><span data-stu-id="2551d-127">-PrimaryKey</span></span>
<span data-ttu-id="2551d-128">Gibt den Primärschlüssel des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="2551d-128">Specifies the subscription primary key.</span></span>
<span data-ttu-id="2551d-129">Dieser Parameter wird automatisch generiert, wenn er nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2551d-129">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="2551d-130">Dieser Parameter muss 1 bis 300 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="2551d-130">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="2551d-131">-Scope</span><span class="sxs-lookup"><span data-stu-id="2551d-131">-Scope</span></span>
<span data-ttu-id="2551d-132">Der Umfang des Abonnements, unabhängig davon, ob es sich um einen API-Bereich/APIs/{apiId} oder um einen Produktbereich handelt/Products/{ProductID} oder globaler API-Bereich/APIs oder globaler Bereich/.</span><span class="sxs-lookup"><span data-stu-id="2551d-132">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="2551d-133">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2551d-133">This parameter is required.</span></span>

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

### <span data-ttu-id="2551d-134">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="2551d-134">-SecondaryKey</span></span>
<span data-ttu-id="2551d-135">Gibt den Sekundärschlüssel des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="2551d-135">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="2551d-136">Dieser Parameter wird automatisch generiert, wenn er nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2551d-136">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="2551d-137">Dieser Parameter muss 1 bis 300 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="2551d-137">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="2551d-138">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="2551d-138">-State</span></span>
<span data-ttu-id="2551d-139">Gibt den Status des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="2551d-139">Specifies the subscription state.</span></span>
<span data-ttu-id="2551d-140">Der Standardwert für diesen Parameter ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="2551d-140">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="2551d-141">-StateComment</span><span class="sxs-lookup"><span data-stu-id="2551d-141">-StateComment</span></span>
<span data-ttu-id="2551d-142">Gibt den Status Kommentar des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="2551d-142">Specifies the subscription state comment.</span></span>
<span data-ttu-id="2551d-143">Der Standardwert für diesen Parameter ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="2551d-143">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="2551d-144">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="2551d-144">-SubscriptionId</span></span>
<span data-ttu-id="2551d-145">Gibt die Abonnement-ID an.</span><span class="sxs-lookup"><span data-stu-id="2551d-145">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="2551d-146">-UserID</span><span class="sxs-lookup"><span data-stu-id="2551d-146">-UserId</span></span>
<span data-ttu-id="2551d-147">Der Besitzer des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="2551d-147">The owner of the subscription.</span></span> <span data-ttu-id="2551d-148">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="2551d-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="2551d-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2551d-149">-Confirm</span></span>
<span data-ttu-id="2551d-150">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2551d-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2551d-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2551d-151">-WhatIf</span></span>
<span data-ttu-id="2551d-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2551d-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2551d-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2551d-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2551d-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2551d-154">CommonParameters</span></span>
<span data-ttu-id="2551d-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2551d-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2551d-156">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2551d-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2551d-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2551d-157">INPUTS</span></span>

### <span data-ttu-id="2551d-158">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2551d-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2551d-159">System. String</span><span class="sxs-lookup"><span data-stu-id="2551d-159">System.String</span></span>

### <span data-ttu-id="2551d-160">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSubscriptionState, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement. Servicemanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2551d-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="2551d-161">System. Nullable ' 1 [[System. DateTime, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2551d-161">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2551d-162">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="2551d-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2551d-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2551d-163">OUTPUTS</span></span>

### <span data-ttu-id="2551d-164">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2551d-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="2551d-165">Notizen</span><span class="sxs-lookup"><span data-stu-id="2551d-165">NOTES</span></span>

## <span data-ttu-id="2551d-166">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2551d-166">RELATED LINKS</span></span>

[<span data-ttu-id="2551d-167">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2551d-167">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="2551d-168">Neu – AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2551d-168">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="2551d-169">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2551d-169">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)


