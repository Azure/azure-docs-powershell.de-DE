---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 09a0af4685701de60fc85c1572b492e7582ff71e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663712"
---
# <span data-ttu-id="9b193-101">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9b193-101">Remove-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="9b193-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9b193-102">SYNOPSIS</span></span>
<span data-ttu-id="9b193-103">Löscht ein vorhandenes Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9b193-103">Deletes an existing subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b193-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b193-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b193-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9b193-105">DESCRIPTION</span></span>
<span data-ttu-id="9b193-106">Das Cmdlet **Remove-AzureRmApiManagementSubscription** löscht ein vorhandenes Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9b193-106">The **Remove-AzureRmApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="9b193-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9b193-107">EXAMPLES</span></span>

### <span data-ttu-id="9b193-108">Beispiel 1: Löschen eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="9b193-108">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="9b193-109">Mit diesem Befehl wird ein vorhandenes Abonnement gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9b193-109">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="9b193-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b193-110">PARAMETERS</span></span>

### <span data-ttu-id="9b193-111">-Context</span><span class="sxs-lookup"><span data-stu-id="9b193-111">-Context</span></span>
<span data-ttu-id="9b193-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="9b193-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9b193-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b193-113">-DefaultProfile</span></span>
<span data-ttu-id="9b193-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9b193-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b193-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b193-115">-PassThru</span></span>
<span data-ttu-id="9b193-116">Gibt an, dass dieses Cmdlet einen Wert von $true zurückgibt, wenn dies erfolgreich ist, oder einen Wert von $false, andernfalls.</span><span class="sxs-lookup"><span data-stu-id="9b193-116">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="9b193-117">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="9b193-117">-SubscriptionId</span></span>
<span data-ttu-id="9b193-118">Gibt die Abonnement-ID an.</span><span class="sxs-lookup"><span data-stu-id="9b193-118">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="9b193-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9b193-119">-Confirm</span></span>
<span data-ttu-id="9b193-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9b193-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b193-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b193-121">-WhatIf</span></span>
<span data-ttu-id="9b193-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9b193-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b193-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b193-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b193-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b193-124">CommonParameters</span></span>
<span data-ttu-id="9b193-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b193-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b193-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b193-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b193-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9b193-127">INPUTS</span></span>

### <span data-ttu-id="9b193-128">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9b193-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9b193-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9b193-129">System.String</span></span>

### <span data-ttu-id="9b193-130">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="9b193-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9b193-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9b193-131">OUTPUTS</span></span>

### <span data-ttu-id="9b193-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9b193-132">System.Boolean</span></span>

## <span data-ttu-id="9b193-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="9b193-133">NOTES</span></span>

## <span data-ttu-id="9b193-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9b193-134">RELATED LINKS</span></span>

[<span data-ttu-id="9b193-135">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9b193-135">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="9b193-136">Neu – AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9b193-136">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="9b193-137">Satz-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9b193-137">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


