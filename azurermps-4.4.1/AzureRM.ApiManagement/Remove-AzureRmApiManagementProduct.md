---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
ms.openlocfilehash: 505a26c48e53fe05e8724d61d5ddb66981e87ee9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477426"
---
# <span data-ttu-id="19e2b-101">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="19e2b-101">Remove-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="19e2b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="19e2b-102">SYNOPSIS</span></span>
<span data-ttu-id="19e2b-103">Entfernt ein vorhandenes API-Verwaltungsprodukt.</span><span class="sxs-lookup"><span data-stu-id="19e2b-103">Removes an existing API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19e2b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="19e2b-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19e2b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="19e2b-105">DESCRIPTION</span></span>
<span data-ttu-id="19e2b-106">Das Cmdlet **Remove-AzureRmApiManagementProduct** entfernt ein vorhandenes API-Verwaltungsprodukt.</span><span class="sxs-lookup"><span data-stu-id="19e2b-106">The **Remove-AzureRmApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="19e2b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="19e2b-107">EXAMPLES</span></span>

### <span data-ttu-id="19e2b-108">Beispiel 1: Entfernen eines vorhandenen Produkts und aller Abonnements</span><span class="sxs-lookup"><span data-stu-id="19e2b-108">Example 1: Remove an existing product and all subscriptions</span></span>
```
PS C:\>Remove-AzureRmApiManagementProduct -Context $APImContext -Id "0123456789" -DeleteSubscriptions -Force
```

<span data-ttu-id="19e2b-109">Mit diesem Befehl werden ein vorhandenes Produkt und alle Abonnements entfernt.</span><span class="sxs-lookup"><span data-stu-id="19e2b-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="19e2b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="19e2b-110">PARAMETERS</span></span>

### <span data-ttu-id="19e2b-111">-Context</span><span class="sxs-lookup"><span data-stu-id="19e2b-111">-Context</span></span>
<span data-ttu-id="19e2b-112">Gibt eine Instanz des **PsApiManagementContext** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="19e2b-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="19e2b-113">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="19e2b-113">-DeleteSubscriptions</span></span>
<span data-ttu-id="19e2b-114">Gibt an, ob Abonnements für das Produkt gelöscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="19e2b-114">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="19e2b-115">Wenn Sie diesen Parameter nicht setzen und Abonnements vorhanden sind, wird eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="19e2b-115">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="19e2b-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19e2b-116">-PassThru</span></span>
<span data-ttu-id="19e2b-117">Gibt an, dass dieses Cmdlet einen Wert von $true zurückgibt, wenn es erfolgreich ist, oder einen Wert von $false, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="19e2b-117">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="19e2b-118">-ProductID</span><span class="sxs-lookup"><span data-stu-id="19e2b-118">-ProductId</span></span>
<span data-ttu-id="19e2b-119">Gibt den Bezeichner des vorhandenen Produkts an.</span><span class="sxs-lookup"><span data-stu-id="19e2b-119">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="19e2b-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="19e2b-120">-Confirm</span></span>
<span data-ttu-id="19e2b-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="19e2b-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e2b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19e2b-122">-WhatIf</span></span>
<span data-ttu-id="19e2b-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="19e2b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19e2b-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="19e2b-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e2b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19e2b-125">-DefaultProfile</span></span>
<span data-ttu-id="19e2b-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="19e2b-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19e2b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19e2b-127">CommonParameters</span></span>
<span data-ttu-id="19e2b-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19e2b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19e2b-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19e2b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19e2b-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="19e2b-130">INPUTS</span></span>

## <span data-ttu-id="19e2b-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="19e2b-131">OUTPUTS</span></span>

### <span data-ttu-id="19e2b-132">bool</span><span class="sxs-lookup"><span data-stu-id="19e2b-132">bool</span></span>

## <span data-ttu-id="19e2b-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="19e2b-133">NOTES</span></span>

## <span data-ttu-id="19e2b-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="19e2b-134">RELATED LINKS</span></span>

[<span data-ttu-id="19e2b-135">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="19e2b-135">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="19e2b-136">Neu – AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="19e2b-136">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="19e2b-137">Satz-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="19e2b-137">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


