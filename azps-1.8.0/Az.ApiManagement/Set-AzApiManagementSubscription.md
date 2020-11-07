---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
ms.openlocfilehash: cbdc876368f55ace6f77c04172dc2f0a53b0a7f6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661872"
---
# <span data-ttu-id="5dbba-101">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="5dbba-101">Set-AzApiManagementSubscription</span></span>

## <span data-ttu-id="5dbba-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5dbba-102">SYNOPSIS</span></span>
<span data-ttu-id="5dbba-103">Legt vorhandene Abonnementdetails fest.</span><span class="sxs-lookup"><span data-stu-id="5dbba-103">Sets existing subscription details.</span></span>

## <span data-ttu-id="5dbba-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5dbba-104">SYNTAX</span></span>

```
Set-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-Name <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5dbba-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5dbba-105">DESCRIPTION</span></span>
<span data-ttu-id="5dbba-106">Das Cmdlet " **Set-AzApiManagementSubscription** " legt vorhandene Abonnementdetails fest.</span><span class="sxs-lookup"><span data-stu-id="5dbba-106">The **Set-AzApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="5dbba-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5dbba-107">EXAMPLES</span></span>

### <span data-ttu-id="5dbba-108">Beispiel 1: Festlegen des Zustands und der primären und sekundären Schlüssel für ein Abonnement</span><span class="sxs-lookup"><span data-stu-id="5dbba-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="5dbba-109">Mit diesem Befehl werden die primären und sekundären Schlüssel für ein Abonnement festgelegt und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5dbba-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="5dbba-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5dbba-110">PARAMETERS</span></span>

### <span data-ttu-id="5dbba-111">-Context</span><span class="sxs-lookup"><span data-stu-id="5dbba-111">-Context</span></span>
<span data-ttu-id="5dbba-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="5dbba-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dbba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dbba-113">-DefaultProfile</span></span>
<span data-ttu-id="5dbba-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5dbba-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5dbba-115">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="5dbba-115">-ExpiresOn</span></span>
<span data-ttu-id="5dbba-116">Gibt das Ablaufdatum eines Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="5dbba-116">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="5dbba-117">Der Standardwert für diesen Parameter ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="5dbba-117">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="5dbba-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5dbba-118">-Name</span></span>
<span data-ttu-id="5dbba-119">Gibt einen Abonnement Namen an.</span><span class="sxs-lookup"><span data-stu-id="5dbba-119">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="5dbba-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5dbba-120">-PassThru</span></span>
<span data-ttu-id="5dbba-121">passthru</span><span class="sxs-lookup"><span data-stu-id="5dbba-121">passthru</span></span>

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

### <span data-ttu-id="5dbba-122">-Primär Primär</span><span class="sxs-lookup"><span data-stu-id="5dbba-122">-PrimaryKey</span></span>
<span data-ttu-id="5dbba-123">Gibt den Primärschlüssel des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="5dbba-123">Specifies the subscription primary key.</span></span>
<span data-ttu-id="5dbba-124">Dieser Parameter wird automatisch generiert, wenn er nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5dbba-124">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="5dbba-125">Dieser Parameter muss 1 bis 300 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="5dbba-125">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="5dbba-126">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="5dbba-126">-SecondaryKey</span></span>
<span data-ttu-id="5dbba-127">Gibt den Sekundärschlüssel des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="5dbba-127">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="5dbba-128">Dieser Parameter wird automatisch generiert, wenn er nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5dbba-128">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="5dbba-129">Dieser Parameter muss 1 bis 300 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="5dbba-129">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="5dbba-130">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="5dbba-130">-State</span></span>
<span data-ttu-id="5dbba-131">Gibt den Status des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="5dbba-131">Specifies the subscription state.</span></span>
<span data-ttu-id="5dbba-132">Der Standardwert für diesen Parameter ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="5dbba-132">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="5dbba-133">-StateComment</span><span class="sxs-lookup"><span data-stu-id="5dbba-133">-StateComment</span></span>
<span data-ttu-id="5dbba-134">Gibt den Status Kommentar des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="5dbba-134">Specifies the subscription state comment.</span></span>
<span data-ttu-id="5dbba-135">Der Standardwert für diesen Parameter ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="5dbba-135">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="5dbba-136">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="5dbba-136">-SubscriptionId</span></span>
<span data-ttu-id="5dbba-137">Gibt die Abonnement-ID an.</span><span class="sxs-lookup"><span data-stu-id="5dbba-137">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="5dbba-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dbba-138">CommonParameters</span></span>
<span data-ttu-id="5dbba-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dbba-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dbba-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dbba-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dbba-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5dbba-141">INPUTS</span></span>

### <span data-ttu-id="5dbba-142">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5dbba-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5dbba-143">System. String</span><span class="sxs-lookup"><span data-stu-id="5dbba-143">System.String</span></span>

### <span data-ttu-id="5dbba-144">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSubscriptionState, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement. Servicemanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5dbba-144">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="5dbba-145">System. Nullable ' 1 [[System. DateTime, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5dbba-145">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5dbba-146">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="5dbba-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5dbba-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5dbba-147">OUTPUTS</span></span>

### <span data-ttu-id="5dbba-148">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="5dbba-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="5dbba-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="5dbba-149">NOTES</span></span>

## <span data-ttu-id="5dbba-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5dbba-150">RELATED LINKS</span></span>

[<span data-ttu-id="5dbba-151">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="5dbba-151">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="5dbba-152">Neu – AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="5dbba-152">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="5dbba-153">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="5dbba-153">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)


