---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 62c1bd394dd509b81a8ea748c26c0465718926c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503122"
---
# <span data-ttu-id="d3b23-101">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d3b23-101">Set-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="d3b23-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d3b23-102">SYNOPSIS</span></span>
<span data-ttu-id="d3b23-103">Legt vorhandene Abonnementdetails fest.</span><span class="sxs-lookup"><span data-stu-id="d3b23-103">Sets existing subscription details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3b23-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3b23-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d3b23-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d3b23-105">DESCRIPTION</span></span>
<span data-ttu-id="d3b23-106">Das Cmdlet " **Set-AzureRmApiManagementSubscription** " legt vorhandene Abonnementdetails fest.</span><span class="sxs-lookup"><span data-stu-id="d3b23-106">The **Set-AzureRmApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="d3b23-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d3b23-107">EXAMPLES</span></span>

### <span data-ttu-id="d3b23-108">Beispiel 1: Festlegen des Zustands und der primären und sekundären Schlüssel für ein Abonnement</span><span class="sxs-lookup"><span data-stu-id="d3b23-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="d3b23-109">Mit diesem Befehl werden die primären und sekundären Schlüssel für ein Abonnement festgelegt und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d3b23-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="d3b23-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3b23-110">PARAMETERS</span></span>

### <span data-ttu-id="d3b23-111">-Context</span><span class="sxs-lookup"><span data-stu-id="d3b23-111">-Context</span></span>
<span data-ttu-id="d3b23-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d3b23-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3b23-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3b23-113">-DefaultProfile</span></span>
<span data-ttu-id="d3b23-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d3b23-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3b23-115">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="d3b23-115">-ExpiresOn</span></span>
<span data-ttu-id="d3b23-116">Gibt das Ablaufdatum eines Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="d3b23-116">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="d3b23-117">Der Standardwert für diesen Parameter ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="d3b23-117">The default value of this parameter is $Null.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3b23-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d3b23-118">-Name</span></span>
<span data-ttu-id="d3b23-119">Gibt einen Abonnement Namen an.</span><span class="sxs-lookup"><span data-stu-id="d3b23-119">Specifies a subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3b23-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3b23-120">-PassThru</span></span>
<span data-ttu-id="d3b23-121">passthru</span><span class="sxs-lookup"><span data-stu-id="d3b23-121">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3b23-122">-Primär Primär</span><span class="sxs-lookup"><span data-stu-id="d3b23-122">-PrimaryKey</span></span>
<span data-ttu-id="d3b23-123">Gibt den Primärschlüssel des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="d3b23-123">Specifies the subscription primary key.</span></span>
<span data-ttu-id="d3b23-124">Dieser Parameter wird automatisch generiert, wenn er nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d3b23-124">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="d3b23-125">Dieser Parameter muss 1 bis 300 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="d3b23-125">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3b23-126">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="d3b23-126">-SecondaryKey</span></span>
<span data-ttu-id="d3b23-127">Gibt den Sekundärschlüssel des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="d3b23-127">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="d3b23-128">Dieser Parameter wird automatisch generiert, wenn er nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d3b23-128">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="d3b23-129">Dieser Parameter muss 1 bis 300 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="d3b23-129">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3b23-130">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="d3b23-130">-State</span></span>
<span data-ttu-id="d3b23-131">Gibt den Status des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="d3b23-131">Specifies the subscription state.</span></span>
<span data-ttu-id="d3b23-132">Der Standardwert für diesen Parameter ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="d3b23-132">The default value of this parameter is $Null.</span></span>

```yaml
Type: PsApiManagementSubscriptionState
Parameter Sets: (All)
Aliases: 
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3b23-133">-StateComment</span><span class="sxs-lookup"><span data-stu-id="d3b23-133">-StateComment</span></span>
<span data-ttu-id="d3b23-134">Gibt den Status Kommentar des Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="d3b23-134">Specifies the subscription state comment.</span></span>
<span data-ttu-id="d3b23-135">Der Standardwert für diesen Parameter ist $NULL.</span><span class="sxs-lookup"><span data-stu-id="d3b23-135">The default value of this parameter is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3b23-136">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="d3b23-136">-SubscriptionId</span></span>
<span data-ttu-id="d3b23-137">Gibt die Abonnement-ID an.</span><span class="sxs-lookup"><span data-stu-id="d3b23-137">Specifies the subscription ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3b23-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3b23-138">CommonParameters</span></span>
<span data-ttu-id="d3b23-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3b23-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3b23-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3b23-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3b23-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d3b23-141">INPUTS</span></span>

### <span data-ttu-id="d3b23-142">Keine</span><span class="sxs-lookup"><span data-stu-id="d3b23-142">None</span></span>
<span data-ttu-id="d3b23-143">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="d3b23-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d3b23-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d3b23-144">OUTPUTS</span></span>

### <span data-ttu-id="d3b23-145">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementSubscripition</span><span class="sxs-lookup"><span data-stu-id="d3b23-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscripition</span></span>

## <span data-ttu-id="d3b23-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="d3b23-146">NOTES</span></span>

## <span data-ttu-id="d3b23-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d3b23-147">RELATED LINKS</span></span>

[<span data-ttu-id="d3b23-148">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d3b23-148">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="d3b23-149">Neu – AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d3b23-149">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="d3b23-150">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d3b23-150">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)


