---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 3b6d07577a6df05a57ed7675f5d14c847e8c33fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479397"
---
# <span data-ttu-id="f31c7-101">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="f31c7-101">Set-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="f31c7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f31c7-102">SYNOPSIS</span></span>
<span data-ttu-id="f31c7-103">Legt vorhandene Abonnementdetails fest.</span><span class="sxs-lookup"><span data-stu-id="f31c7-103">Sets existing subscription details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f31c7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f31c7-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f31c7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f31c7-105">DESCRIPTION</span></span>
<span data-ttu-id="f31c7-106">Das Cmdlet " **Set-AzureRmApiManagementSubscription** " legt vorhandene Abonnementdetails fest.</span><span class="sxs-lookup"><span data-stu-id="f31c7-106">The **Set-AzureRmApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="f31c7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f31c7-107">EXAMPLES</span></span>

### <span data-ttu-id="f31c7-108">Beispiel 1: Festlegen des Zustands und der primären und sekundären Schlüssel für ein Abonnement</span><span class="sxs-lookup"><span data-stu-id="f31c7-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>Set-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SencondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="f31c7-109">Mit diesem Befehl werden die primären und sekundären Schlüssel für ein Abonnement festgelegt und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f31c7-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="f31c7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f31c7-110">PARAMETERS</span></span>

### <span data-ttu-id="f31c7-111">-Context</span><span class="sxs-lookup"><span data-stu-id="f31c7-111">-Context</span></span>
<span data-ttu-id="f31c7-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="f31c7-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f31c7-113">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="f31c7-113">-ExpiresOn</span></span>
<span data-ttu-id="f31c7-114">Gibt das Ablaufdatum eines Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="f31c7-114">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="f31c7-115">Der Standardwert für diesen Parameter ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="f31c7-115">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="f31c7-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f31c7-116">-Name</span></span>
<span data-ttu-id="f31c7-117">Gibt einen Abonnement Namen an.</span><span class="sxs-lookup"><span data-stu-id="f31c7-117">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="f31c7-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f31c7-118">-PassThru</span></span>
<span data-ttu-id="f31c7-119">passthru</span><span class="sxs-lookup"><span data-stu-id="f31c7-119">passthru</span></span>

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

### <span data-ttu-id="f31c7-120">-Primär Primär</span><span class="sxs-lookup"><span data-stu-id="f31c7-120">-PrimaryKey</span></span>
<span data-ttu-id="f31c7-121">Gibt den Primärschlüssel des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="f31c7-121">Specifies the subscription primary key.</span></span>
<span data-ttu-id="f31c7-122">Dieser Parameter wird automatisch generiert, wenn er nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f31c7-122">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="f31c7-123">Dieser Parameter muss 1 bis 300 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="f31c7-123">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="f31c7-124">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="f31c7-124">-SecondaryKey</span></span>
<span data-ttu-id="f31c7-125">Gibt den Sekundärschlüssel des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="f31c7-125">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="f31c7-126">Dieser Parameter wird automatisch generiert, wenn er nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f31c7-126">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="f31c7-127">Dieser Parameter muss 1 bis 300 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="f31c7-127">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="f31c7-128">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="f31c7-128">-State</span></span>
<span data-ttu-id="f31c7-129">Gibt den Status des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="f31c7-129">Specifies the subscription state.</span></span>
<span data-ttu-id="f31c7-130">Der Standardwert für diesen Parameter ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="f31c7-130">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="f31c7-131">-StateComment</span><span class="sxs-lookup"><span data-stu-id="f31c7-131">-StateComment</span></span>
<span data-ttu-id="f31c7-132">Gibt den Status Kommentar des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="f31c7-132">Specifies the subscription state comment.</span></span>
<span data-ttu-id="f31c7-133">Der Standardwert für diesen Parameter ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="f31c7-133">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="f31c7-134">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="f31c7-134">-SubscriptionId</span></span>
<span data-ttu-id="f31c7-135">Gibt die Abonnement-ID an.</span><span class="sxs-lookup"><span data-stu-id="f31c7-135">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="f31c7-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f31c7-136">-DefaultProfile</span></span>
<span data-ttu-id="f31c7-137">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f31c7-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f31c7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f31c7-138">CommonParameters</span></span>
<span data-ttu-id="f31c7-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f31c7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f31c7-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f31c7-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f31c7-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f31c7-141">INPUTS</span></span>

## <span data-ttu-id="f31c7-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f31c7-142">OUTPUTS</span></span>

### <span data-ttu-id="f31c7-143">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSubscripition</span><span class="sxs-lookup"><span data-stu-id="f31c7-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscripition</span></span>

## <span data-ttu-id="f31c7-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="f31c7-144">NOTES</span></span>

## <span data-ttu-id="f31c7-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f31c7-145">RELATED LINKS</span></span>

[<span data-ttu-id="f31c7-146">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="f31c7-146">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="f31c7-147">Neu – AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="f31c7-147">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="f31c7-148">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="f31c7-148">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)


