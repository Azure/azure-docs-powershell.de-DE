---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
ms.openlocfilehash: 8c6bc7a9e29d6f187285cacdc9df3621fcba8d0f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145268"
---
# <span data-ttu-id="5a22e-101">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="5a22e-101">Remove-AzApiManagementSubscription</span></span>

## <span data-ttu-id="5a22e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a22e-102">SYNOPSIS</span></span>
<span data-ttu-id="5a22e-103">Löscht ein vorhandenes Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5a22e-103">Deletes an existing subscription.</span></span>

## <span data-ttu-id="5a22e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5a22e-104">SYNTAX</span></span>

### <span data-ttu-id="5a22e-105">ExpandedParameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="5a22e-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a22e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5a22e-106">ByInputObject</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -InputObject <PsApiManagementSubscription> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a22e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5a22e-107">ByResourceId</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5a22e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5a22e-108">DESCRIPTION</span></span>
<span data-ttu-id="5a22e-109">Das **Cmdlet "Remove-AzApiManagementSubscription"** löscht ein vorhandenes Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5a22e-109">The **Remove-AzApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="5a22e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5a22e-110">EXAMPLES</span></span>

### <span data-ttu-id="5a22e-111">Beispiel 1: Löschen eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="5a22e-111">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="5a22e-112">Mit diesem Befehl wird ein vorhandenes Abonnement gelöscht.</span><span class="sxs-lookup"><span data-stu-id="5a22e-112">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="5a22e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a22e-113">PARAMETERS</span></span>

### <span data-ttu-id="5a22e-114">-Context</span><span class="sxs-lookup"><span data-stu-id="5a22e-114">-Context</span></span>
<span data-ttu-id="5a22e-115">Gibt ein **"PsApiManagementContext"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="5a22e-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5a22e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a22e-116">-DefaultProfile</span></span>
<span data-ttu-id="5a22e-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5a22e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a22e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a22e-118">-InputObject</span></span>
<span data-ttu-id="5a22e-119">Instanz von PsApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="5a22e-119">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="5a22e-120">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5a22e-120">This parameter is required.</span></span>

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

### <span data-ttu-id="5a22e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a22e-121">-PassThru</span></span>
<span data-ttu-id="5a22e-122">Gibt an, dass dieses Cmdlet den Wert "$True" (falls erfolgreich) oder andernfalls den Wert $false zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="5a22e-122">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="5a22e-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a22e-123">-ResourceId</span></span>
<span data-ttu-id="5a22e-124">Arm ResourceId des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="5a22e-124">Arm ResourceId of Subscription.</span></span> <span data-ttu-id="5a22e-125">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5a22e-125">This parameter is required.</span></span>

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

### <span data-ttu-id="5a22e-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5a22e-126">-SubscriptionId</span></span>
<span data-ttu-id="5a22e-127">Gibt die Abonnement-ID an.</span><span class="sxs-lookup"><span data-stu-id="5a22e-127">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="5a22e-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a22e-128">-Confirm</span></span>
<span data-ttu-id="5a22e-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5a22e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a22e-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5a22e-130">-WhatIf</span></span>
<span data-ttu-id="5a22e-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5a22e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a22e-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5a22e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a22e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a22e-133">CommonParameters</span></span>
<span data-ttu-id="5a22e-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a22e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a22e-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a22e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a22e-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5a22e-136">INPUTS</span></span>

### <span data-ttu-id="5a22e-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5a22e-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5a22e-138">System.String</span><span class="sxs-lookup"><span data-stu-id="5a22e-138">System.String</span></span>

### <span data-ttu-id="5a22e-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5a22e-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5a22e-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5a22e-140">OUTPUTS</span></span>

### <span data-ttu-id="5a22e-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5a22e-141">System.Boolean</span></span>

## <span data-ttu-id="5a22e-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5a22e-142">NOTES</span></span>

## <span data-ttu-id="5a22e-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5a22e-143">RELATED LINKS</span></span>

[<span data-ttu-id="5a22e-144">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="5a22e-144">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="5a22e-145">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="5a22e-145">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="5a22e-146">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="5a22e-146">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


