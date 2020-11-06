---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
ms.openlocfilehash: c747d85f87e88c3f72ae86c8bcef771b3e42c91a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478025"
---
# <span data-ttu-id="201dc-101">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="201dc-101">Set-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="201dc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="201dc-102">SYNOPSIS</span></span>
<span data-ttu-id="201dc-103">Legt vorhandene Abonnementdetails fest.</span><span class="sxs-lookup"><span data-stu-id="201dc-103">Sets existing subscription details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="201dc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="201dc-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="201dc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="201dc-105">DESCRIPTION</span></span>
<span data-ttu-id="201dc-106">Das Cmdlet " **Set-AzureRmApiManagementSubscription** " legt vorhandene Abonnementdetails fest.</span><span class="sxs-lookup"><span data-stu-id="201dc-106">The **Set-AzureRmApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="201dc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="201dc-107">EXAMPLES</span></span>

### <span data-ttu-id="201dc-108">Beispiel 1: Festlegen des Zustands und der primären und sekundären Schlüssel für ein Abonnement</span><span class="sxs-lookup"><span data-stu-id="201dc-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="201dc-109">Mit diesem Befehl werden die primären und sekundären Schlüssel für ein Abonnement festgelegt und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="201dc-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="201dc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="201dc-110">PARAMETERS</span></span>

### <span data-ttu-id="201dc-111">-Context</span><span class="sxs-lookup"><span data-stu-id="201dc-111">-Context</span></span>
<span data-ttu-id="201dc-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="201dc-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="201dc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="201dc-113">-DefaultProfile</span></span>
<span data-ttu-id="201dc-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="201dc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="201dc-115">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="201dc-115">-ExpiresOn</span></span>
<span data-ttu-id="201dc-116">Gibt das Ablaufdatum eines Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="201dc-116">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="201dc-117">Der Standardwert für diesen Parameter ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="201dc-117">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="201dc-118">-Name</span><span class="sxs-lookup"><span data-stu-id="201dc-118">-Name</span></span>
<span data-ttu-id="201dc-119">Gibt einen Abonnement Namen an.</span><span class="sxs-lookup"><span data-stu-id="201dc-119">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="201dc-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="201dc-120">-PassThru</span></span>
<span data-ttu-id="201dc-121">passthru</span><span class="sxs-lookup"><span data-stu-id="201dc-121">passthru</span></span>

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

### <span data-ttu-id="201dc-122">-Primär Primär</span><span class="sxs-lookup"><span data-stu-id="201dc-122">-PrimaryKey</span></span>
<span data-ttu-id="201dc-123">Gibt den Primärschlüssel des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="201dc-123">Specifies the subscription primary key.</span></span>
<span data-ttu-id="201dc-124">Dieser Parameter wird automatisch generiert, wenn er nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="201dc-124">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="201dc-125">Dieser Parameter muss 1 bis 300 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="201dc-125">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="201dc-126">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="201dc-126">-SecondaryKey</span></span>
<span data-ttu-id="201dc-127">Gibt den Sekundärschlüssel des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="201dc-127">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="201dc-128">Dieser Parameter wird automatisch generiert, wenn er nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="201dc-128">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="201dc-129">Dieser Parameter muss 1 bis 300 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="201dc-129">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="201dc-130">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="201dc-130">-State</span></span>
<span data-ttu-id="201dc-131">Gibt den Status des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="201dc-131">Specifies the subscription state.</span></span>
<span data-ttu-id="201dc-132">Der Standardwert für diesen Parameter ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="201dc-132">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="201dc-133">-StateComment</span><span class="sxs-lookup"><span data-stu-id="201dc-133">-StateComment</span></span>
<span data-ttu-id="201dc-134">Gibt den Status Kommentar des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="201dc-134">Specifies the subscription state comment.</span></span>
<span data-ttu-id="201dc-135">Der Standardwert für diesen Parameter ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="201dc-135">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="201dc-136">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="201dc-136">-SubscriptionId</span></span>
<span data-ttu-id="201dc-137">Gibt die Abonnement-ID an.</span><span class="sxs-lookup"><span data-stu-id="201dc-137">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="201dc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="201dc-138">CommonParameters</span></span>
<span data-ttu-id="201dc-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="201dc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="201dc-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="201dc-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="201dc-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="201dc-141">INPUTS</span></span>

### <span data-ttu-id="201dc-142">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="201dc-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="201dc-143">System. String</span><span class="sxs-lookup"><span data-stu-id="201dc-143">System.String</span></span>

### <span data-ttu-id="201dc-144">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSubscriptionState, Microsoft. Azure. Commands. ApiManagement. Servicemanagement, Version = 6.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="201dc-144">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="201dc-145">System. Nullable ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="201dc-145">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="201dc-146">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="201dc-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="201dc-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="201dc-147">OUTPUTS</span></span>

### <span data-ttu-id="201dc-148">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="201dc-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="201dc-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="201dc-149">NOTES</span></span>

## <span data-ttu-id="201dc-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="201dc-150">RELATED LINKS</span></span>

[<span data-ttu-id="201dc-151">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="201dc-151">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="201dc-152">Neu – AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="201dc-152">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="201dc-153">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="201dc-153">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)


