---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 777d71dec17f75cba84c15c7499e5ec56ffb854a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665331"
---
# <span data-ttu-id="316e7-101">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="316e7-101">Remove-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="316e7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="316e7-102">SYNOPSIS</span></span>
<span data-ttu-id="316e7-103">Löscht ein vorhandenes Abonnement.</span><span class="sxs-lookup"><span data-stu-id="316e7-103">Deletes an existing subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="316e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="316e7-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="316e7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="316e7-105">DESCRIPTION</span></span>
<span data-ttu-id="316e7-106">Das Cmdlet **Remove-AzureRmApiManagementSubscription** löscht ein vorhandenes Abonnement.</span><span class="sxs-lookup"><span data-stu-id="316e7-106">The **Remove-AzureRmApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="316e7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="316e7-107">EXAMPLES</span></span>

### <span data-ttu-id="316e7-108">Beispiel 1: Löschen eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="316e7-108">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="316e7-109">Mit diesem Befehl wird ein vorhandenes Abonnement gelöscht.</span><span class="sxs-lookup"><span data-stu-id="316e7-109">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="316e7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="316e7-110">PARAMETERS</span></span>

### <span data-ttu-id="316e7-111">-Context</span><span class="sxs-lookup"><span data-stu-id="316e7-111">-Context</span></span>
<span data-ttu-id="316e7-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="316e7-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="316e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="316e7-113">-DefaultProfile</span></span>
<span data-ttu-id="316e7-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="316e7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="316e7-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="316e7-115">-PassThru</span></span>
<span data-ttu-id="316e7-116">Gibt an, dass dieses Cmdlet einen Wert von $true zurückgibt, wenn dies erfolgreich ist, oder einen Wert von $false, andernfalls.</span><span class="sxs-lookup"><span data-stu-id="316e7-116">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="316e7-117">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="316e7-117">-SubscriptionId</span></span>
<span data-ttu-id="316e7-118">Gibt die Abonnement-ID an.</span><span class="sxs-lookup"><span data-stu-id="316e7-118">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="316e7-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="316e7-119">-Confirm</span></span>
<span data-ttu-id="316e7-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="316e7-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="316e7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="316e7-121">-WhatIf</span></span>
<span data-ttu-id="316e7-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="316e7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="316e7-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="316e7-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="316e7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="316e7-124">CommonParameters</span></span>
<span data-ttu-id="316e7-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="316e7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="316e7-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="316e7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="316e7-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="316e7-127">INPUTS</span></span>

### <span data-ttu-id="316e7-128">Keine</span><span class="sxs-lookup"><span data-stu-id="316e7-128">None</span></span>
<span data-ttu-id="316e7-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="316e7-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="316e7-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="316e7-130">OUTPUTS</span></span>

### <span data-ttu-id="316e7-131">Boolean</span><span class="sxs-lookup"><span data-stu-id="316e7-131">Boolean</span></span>

## <span data-ttu-id="316e7-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="316e7-132">NOTES</span></span>

## <span data-ttu-id="316e7-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="316e7-133">RELATED LINKS</span></span>

[<span data-ttu-id="316e7-134">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="316e7-134">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="316e7-135">Neu – AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="316e7-135">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="316e7-136">Satz-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="316e7-136">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


