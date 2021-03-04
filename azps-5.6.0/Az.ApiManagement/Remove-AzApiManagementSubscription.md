---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
ms.openlocfilehash: 1a9c44bf88e3e6aba9fdc74e588ca8e8bb7ae792
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939011"
---
# <span data-ttu-id="a7bdf-101">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a7bdf-101">Remove-AzApiManagementSubscription</span></span>

## <span data-ttu-id="a7bdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="a7bdf-103">Löscht ein vorhandenes Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-103">Deletes an existing subscription.</span></span>

## <span data-ttu-id="a7bdf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7bdf-104">SYNTAX</span></span>

### <span data-ttu-id="a7bdf-105">ExpandedParameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="a7bdf-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7bdf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a7bdf-106">ByInputObject</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -InputObject <PsApiManagementSubscription> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7bdf-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a7bdf-107">ByResourceId</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a7bdf-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a7bdf-108">DESCRIPTION</span></span>
<span data-ttu-id="a7bdf-109">Das **Cmdlet Remove-AzApiManagementSubscription** löscht ein vorhandenes Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-109">The **Remove-AzApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="a7bdf-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a7bdf-110">EXAMPLES</span></span>

### <span data-ttu-id="a7bdf-111">Beispiel 1: Löschen eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="a7bdf-111">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="a7bdf-112">Mit diesem Befehl wird ein vorhandenes Abonnement gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-112">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="a7bdf-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a7bdf-113">PARAMETERS</span></span>

### <span data-ttu-id="a7bdf-114">-Context</span><span class="sxs-lookup"><span data-stu-id="a7bdf-114">-Context</span></span>
<span data-ttu-id="a7bdf-115">Gibt ein **PsApiManagementContext-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a7bdf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7bdf-116">-DefaultProfile</span></span>
<span data-ttu-id="a7bdf-117">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7bdf-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7bdf-118">-InputObject</span></span>
<span data-ttu-id="a7bdf-119">Instanz von PsApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-119">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="a7bdf-120">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7bdf-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7bdf-121">-PassThru</span></span>
<span data-ttu-id="a7bdf-122">Gibt an, dass dieses Cmdlet einen Wert von $True, wenn es erfolgreich ist, oder einen Wert von $false zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-122">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="a7bdf-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7bdf-123">-ResourceId</span></span>
<span data-ttu-id="a7bdf-124">Arm ResourceId des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-124">Arm ResourceId of Subscription.</span></span> <span data-ttu-id="a7bdf-125">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-125">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7bdf-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a7bdf-126">-SubscriptionId</span></span>
<span data-ttu-id="a7bdf-127">Gibt die Abonnement-ID an.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-127">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="a7bdf-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a7bdf-128">-Confirm</span></span>
<span data-ttu-id="a7bdf-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7bdf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7bdf-130">-WhatIf</span></span>
<span data-ttu-id="a7bdf-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7bdf-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7bdf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7bdf-133">CommonParameters</span></span>
<span data-ttu-id="a7bdf-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7bdf-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7bdf-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7bdf-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a7bdf-136">INPUTS</span></span>

### <span data-ttu-id="a7bdf-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a7bdf-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a7bdf-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a7bdf-138">System.String</span></span>

### <span data-ttu-id="a7bdf-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a7bdf-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a7bdf-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a7bdf-140">OUTPUTS</span></span>

### <span data-ttu-id="a7bdf-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a7bdf-141">System.Boolean</span></span>

## <span data-ttu-id="a7bdf-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a7bdf-142">NOTES</span></span>

## <span data-ttu-id="a7bdf-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a7bdf-143">RELATED LINKS</span></span>

[<span data-ttu-id="a7bdf-144">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a7bdf-144">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="a7bdf-145">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a7bdf-145">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="a7bdf-146">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a7bdf-146">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


