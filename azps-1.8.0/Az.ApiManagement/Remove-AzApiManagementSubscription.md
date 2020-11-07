---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
ms.openlocfilehash: 411fa67d81b772c2e9dcd6b1690e8eac50de3ea0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821048"
---
# <span data-ttu-id="cd128-101">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="cd128-101">Remove-AzApiManagementSubscription</span></span>

## <span data-ttu-id="cd128-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cd128-102">SYNOPSIS</span></span>
<span data-ttu-id="cd128-103">Löscht ein vorhandenes Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cd128-103">Deletes an existing subscription.</span></span>

## <span data-ttu-id="cd128-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd128-104">SYNTAX</span></span>

```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd128-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd128-105">DESCRIPTION</span></span>
<span data-ttu-id="cd128-106">Das Cmdlet **Remove-AzApiManagementSubscription** löscht ein vorhandenes Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cd128-106">The **Remove-AzApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="cd128-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cd128-107">EXAMPLES</span></span>

### <span data-ttu-id="cd128-108">Beispiel 1: Löschen eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="cd128-108">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="cd128-109">Mit diesem Befehl wird ein vorhandenes Abonnement gelöscht.</span><span class="sxs-lookup"><span data-stu-id="cd128-109">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="cd128-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd128-110">PARAMETERS</span></span>

### <span data-ttu-id="cd128-111">-Context</span><span class="sxs-lookup"><span data-stu-id="cd128-111">-Context</span></span>
<span data-ttu-id="cd128-112">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="cd128-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="cd128-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd128-113">-DefaultProfile</span></span>
<span data-ttu-id="cd128-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cd128-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd128-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd128-115">-PassThru</span></span>
<span data-ttu-id="cd128-116">Gibt an, dass dieses Cmdlet einen Wert von $true zurückgibt, wenn dies erfolgreich ist, oder einen Wert von $false, andernfalls.</span><span class="sxs-lookup"><span data-stu-id="cd128-116">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="cd128-117">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="cd128-117">-SubscriptionId</span></span>
<span data-ttu-id="cd128-118">Gibt die Abonnement-ID an.</span><span class="sxs-lookup"><span data-stu-id="cd128-118">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="cd128-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cd128-119">-Confirm</span></span>
<span data-ttu-id="cd128-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cd128-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd128-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd128-121">-WhatIf</span></span>
<span data-ttu-id="cd128-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cd128-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd128-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cd128-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd128-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd128-124">CommonParameters</span></span>
<span data-ttu-id="cd128-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd128-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd128-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd128-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd128-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cd128-127">INPUTS</span></span>

### <span data-ttu-id="cd128-128">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cd128-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cd128-129">System. String</span><span class="sxs-lookup"><span data-stu-id="cd128-129">System.String</span></span>

### <span data-ttu-id="cd128-130">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="cd128-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cd128-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cd128-131">OUTPUTS</span></span>

### <span data-ttu-id="cd128-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cd128-132">System.Boolean</span></span>

## <span data-ttu-id="cd128-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="cd128-133">NOTES</span></span>

## <span data-ttu-id="cd128-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cd128-134">RELATED LINKS</span></span>

[<span data-ttu-id="cd128-135">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="cd128-135">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="cd128-136">Neu – AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="cd128-136">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="cd128-137">Satz-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="cd128-137">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


