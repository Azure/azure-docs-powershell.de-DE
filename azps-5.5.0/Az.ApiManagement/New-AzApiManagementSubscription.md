---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
ms.openlocfilehash: ea68d17d482a73a528cfe450a84700e48bfdd9f9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171803"
---
# <span data-ttu-id="bcb53-101">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="bcb53-101">New-AzApiManagementSubscription</span></span>

## <span data-ttu-id="bcb53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcb53-102">SYNOPSIS</span></span>
<span data-ttu-id="bcb53-103">Erstellt ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bcb53-103">Creates a subscription.</span></span>

## <span data-ttu-id="bcb53-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bcb53-104">SYNTAX</span></span>

### <span data-ttu-id="bcb53-105">OldSubscriptionModel (Standard)</span><span class="sxs-lookup"><span data-stu-id="bcb53-105">OldSubscriptionModel (Default)</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcb53-106">NewSubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="bcb53-106">NewSubscriptionModel</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 [-UserId <String>] -Scope <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcb53-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bcb53-107">DESCRIPTION</span></span>
<span data-ttu-id="bcb53-108">Das **Cmdlet "New-AzApiManagementSubscription"** erstellt ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bcb53-108">The **New-AzApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="bcb53-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bcb53-109">EXAMPLES</span></span>

### <span data-ttu-id="bcb53-110">Beispiel 1: Abonnieren eines Benutzers für ein Produkt</span><span class="sxs-lookup"><span data-stu-id="bcb53-110">Example 1: Subscribe a user to a product</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="bcb53-111">Dieser Befehl abonniert einen vorhandenen Benutzer für ein Produkt.</span><span class="sxs-lookup"><span data-stu-id="bcb53-111">This command subscribes an existing user to a product.</span></span>

### <span data-ttu-id="bcb53-112">Beispiel 2: Erstellen eines Abonnements für den ganzen Api-Bereich</span><span class="sxs-lookup"><span data-stu-id="bcb53-112">Example 2: Create a subscription for all Api Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/apis" -Name "GlobalApiScope"
```

### <span data-ttu-id="bcb53-113">Beispiel 3: Erstellen eines Abonnements für den Produktbereich</span><span class="sxs-lookup"><span data-stu-id="bcb53-113">Example 3: Create a subscription for Product Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/products/starter" -Name "UnlimitedProductSub"
```

## <span data-ttu-id="bcb53-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcb53-114">PARAMETERS</span></span>

### <span data-ttu-id="bcb53-115">-AllowTracing</span><span class="sxs-lookup"><span data-stu-id="bcb53-115">-AllowTracing</span></span>
<span data-ttu-id="bcb53-116">Das Kennzeichen bestimmt, ob die Ablaufverfolgung auf Abonnementebene aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="bcb53-116">Flag which determines whether Tracing can be enabled at the Subscription Level.</span></span> <span data-ttu-id="bcb53-117">Dies ist ein optionaler Parameter, und der Standardwert ist $null.</span><span class="sxs-lookup"><span data-stu-id="bcb53-117">This is optional parameter and default is $null.</span></span>

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

### <span data-ttu-id="bcb53-118">-Context</span><span class="sxs-lookup"><span data-stu-id="bcb53-118">-Context</span></span>
<span data-ttu-id="bcb53-119">Gibt ein **"PsApiManagementContext"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="bcb53-119">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bcb53-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcb53-120">-DefaultProfile</span></span>
<span data-ttu-id="bcb53-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bcb53-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcb53-122">-Name</span><span class="sxs-lookup"><span data-stu-id="bcb53-122">-Name</span></span>
<span data-ttu-id="bcb53-123">Gibt den Namen des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="bcb53-123">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="bcb53-124">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="bcb53-124">-PrimaryKey</span></span>
<span data-ttu-id="bcb53-125">Gibt den Primärschlüssel des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="bcb53-125">Specifies the subscription primary key.</span></span>
<span data-ttu-id="bcb53-126">Wenn dieser Parameter nicht angegeben wird, wird der Schlüssel automatisch generiert.</span><span class="sxs-lookup"><span data-stu-id="bcb53-126">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="bcb53-127">Dieser Parameter muss 1 bis 300 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="bcb53-127">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="bcb53-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="bcb53-128">-ProductId</span></span>
<span data-ttu-id="bcb53-129">Gibt die ID des Produkts an, das Sie abonnieren möchten.</span><span class="sxs-lookup"><span data-stu-id="bcb53-129">Specifies the ID of the product to which to subscribe.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSubscriptionModel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcb53-130">-Scope</span><span class="sxs-lookup"><span data-stu-id="bcb53-130">-Scope</span></span>
<span data-ttu-id="bcb53-131">Der Umfang des Abonnements, unabhängig davon, ob es sich um den Api-Bereich /apis/{apiId} oder den Produktbereich /products/{productId} oder den globalen API-Bereich /apis oder den globalen Bereich /handelt.</span><span class="sxs-lookup"><span data-stu-id="bcb53-131">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="bcb53-132">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bcb53-132">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSubscriptionModel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcb53-133">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="bcb53-133">-SecondaryKey</span></span>
<span data-ttu-id="bcb53-134">Gibt den sekundären Abonnementschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="bcb53-134">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="bcb53-135">Dieser Parameter wird automatisch generiert, wenn er nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bcb53-135">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="bcb53-136">Dieser Parameter muss 1 bis 300 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="bcb53-136">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="bcb53-137">-State</span><span class="sxs-lookup"><span data-stu-id="bcb53-137">-State</span></span>
<span data-ttu-id="bcb53-138">Gibt den Abonnementstatus an.</span><span class="sxs-lookup"><span data-stu-id="bcb53-138">Specifies the subscription state.</span></span>
<span data-ttu-id="bcb53-139">Der Standardwert ist $Null.</span><span class="sxs-lookup"><span data-stu-id="bcb53-139">The default value is $Null.</span></span>

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

### <span data-ttu-id="bcb53-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bcb53-140">-SubscriptionId</span></span>
<span data-ttu-id="bcb53-141">Gibt die Abonnement-ID an.</span><span class="sxs-lookup"><span data-stu-id="bcb53-141">Specifies the subscription ID.</span></span>
<span data-ttu-id="bcb53-142">Dieser Parameter wird generiert, wenn er nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bcb53-142">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="bcb53-143">-UserId</span><span class="sxs-lookup"><span data-stu-id="bcb53-143">-UserId</span></span>
<span data-ttu-id="bcb53-144">Gibt die Abonnenten-ID an.</span><span class="sxs-lookup"><span data-stu-id="bcb53-144">Specifies the subscriber ID.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSubscriptionModel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NewSubscriptionModel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcb53-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcb53-145">CommonParameters</span></span>
<span data-ttu-id="bcb53-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcb53-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcb53-147">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bcb53-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcb53-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bcb53-148">INPUTS</span></span>

### <span data-ttu-id="bcb53-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bcb53-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bcb53-150">System.String</span><span class="sxs-lookup"><span data-stu-id="bcb53-150">System.String</span></span>

### <span data-ttu-id="bcb53-151">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="bcb53-151">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="bcb53-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bcb53-152">OUTPUTS</span></span>

### <span data-ttu-id="bcb53-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="bcb53-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="bcb53-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bcb53-154">NOTES</span></span>

## <span data-ttu-id="bcb53-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bcb53-155">RELATED LINKS</span></span>

[<span data-ttu-id="bcb53-156">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="bcb53-156">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="bcb53-157">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="bcb53-157">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="bcb53-158">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="bcb53-158">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


