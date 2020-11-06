---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
ms.openlocfilehash: 5c5bd7d0b7df385645bdb51d684616f2c0d7eaa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477049"
---
# <span data-ttu-id="e44f3-101">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e44f3-101">Remove-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="e44f3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e44f3-102">SYNOPSIS</span></span>
<span data-ttu-id="e44f3-103">Entfernt ein vorhandenes API-Verwaltungsprodukt.</span><span class="sxs-lookup"><span data-stu-id="e44f3-103">Removes an existing API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e44f3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e44f3-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e44f3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e44f3-105">DESCRIPTION</span></span>
<span data-ttu-id="e44f3-106">Das Cmdlet **Remove-AzureRmApiManagementProduct** entfernt ein vorhandenes API-Verwaltungsprodukt.</span><span class="sxs-lookup"><span data-stu-id="e44f3-106">The **Remove-AzureRmApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="e44f3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e44f3-107">EXAMPLES</span></span>

### <span data-ttu-id="e44f3-108">Beispiel 1: Entfernen eines vorhandenen Produkts und aller Abonnements</span><span class="sxs-lookup"><span data-stu-id="e44f3-108">Example 1: Remove an existing product and all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProduct -Context $apimContext -Id "0123456789" -DeleteSubscriptions -Force
```

<span data-ttu-id="e44f3-109">Mit diesem Befehl werden ein vorhandenes Produkt und alle Abonnements entfernt.</span><span class="sxs-lookup"><span data-stu-id="e44f3-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="e44f3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e44f3-110">PARAMETERS</span></span>

### <span data-ttu-id="e44f3-111">-Context</span><span class="sxs-lookup"><span data-stu-id="e44f3-111">-Context</span></span>
<span data-ttu-id="e44f3-112">Gibt eine Instanz des **PsApiManagementContext** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="e44f3-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e44f3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e44f3-113">-DefaultProfile</span></span>
<span data-ttu-id="e44f3-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e44f3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="e44f3-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="e44f3-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="e44f3-116">Gibt an, ob Abonnements für das Produkt gelöscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e44f3-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="e44f3-117">Wenn Sie diesen Parameter nicht setzen und Abonnements vorhanden sind, wird eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="e44f3-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="e44f3-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e44f3-118">-PassThru</span></span>
<span data-ttu-id="e44f3-119">Gibt an, dass dieses Cmdlet einen Wert von $true zurückgibt, wenn es erfolgreich ist, oder einen Wert von $false, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="e44f3-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="e44f3-120">-ProductID</span><span class="sxs-lookup"><span data-stu-id="e44f3-120">-ProductId</span></span>
<span data-ttu-id="e44f3-121">Gibt den Bezeichner des vorhandenen Produkts an.</span><span class="sxs-lookup"><span data-stu-id="e44f3-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="e44f3-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e44f3-122">-Confirm</span></span>
<span data-ttu-id="e44f3-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e44f3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e44f3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e44f3-124">-WhatIf</span></span>
<span data-ttu-id="e44f3-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e44f3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e44f3-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e44f3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e44f3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e44f3-127">CommonParameters</span></span>
<span data-ttu-id="e44f3-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e44f3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e44f3-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e44f3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e44f3-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e44f3-130">INPUTS</span></span>

### <span data-ttu-id="e44f3-131">Keine</span><span class="sxs-lookup"><span data-stu-id="e44f3-131">None</span></span>
<span data-ttu-id="e44f3-132">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="e44f3-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e44f3-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e44f3-133">OUTPUTS</span></span>

### <span data-ttu-id="e44f3-134">bool</span><span class="sxs-lookup"><span data-stu-id="e44f3-134">bool</span></span>

## <span data-ttu-id="e44f3-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="e44f3-135">NOTES</span></span>

## <span data-ttu-id="e44f3-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e44f3-136">RELATED LINKS</span></span>

[<span data-ttu-id="e44f3-137">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e44f3-137">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="e44f3-138">Neu – AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e44f3-138">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="e44f3-139">Satz-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e44f3-139">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


