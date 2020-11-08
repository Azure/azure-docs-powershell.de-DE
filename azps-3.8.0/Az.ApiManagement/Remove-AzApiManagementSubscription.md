---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
ms.openlocfilehash: 8c6bc7a9e29d6f187285cacdc9df3621fcba8d0f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996840"
---
# <span data-ttu-id="c9c3f-101">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c9c3f-101">Remove-AzApiManagementSubscription</span></span>

## <span data-ttu-id="c9c3f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c9c3f-102">SYNOPSIS</span></span>
<span data-ttu-id="c9c3f-103">Löscht ein vorhandenes Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c9c3f-103">Deletes an existing subscription.</span></span>

## <span data-ttu-id="c9c3f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9c3f-104">SYNTAX</span></span>

### <span data-ttu-id="c9c3f-105">Expanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="c9c3f-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9c3f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c9c3f-106">ByInputObject</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -InputObject <PsApiManagementSubscription> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9c3f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c9c3f-107">ByResourceId</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9c3f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9c3f-108">DESCRIPTION</span></span>
<span data-ttu-id="c9c3f-109">Das Cmdlet **Remove-AzApiManagementSubscription** löscht ein vorhandenes Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c9c3f-109">The **Remove-AzApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="c9c3f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c9c3f-110">EXAMPLES</span></span>

### <span data-ttu-id="c9c3f-111">Beispiel 1: Löschen eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="c9c3f-111">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="c9c3f-112">Mit diesem Befehl wird ein vorhandenes Abonnement gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c9c3f-112">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="c9c3f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9c3f-113">PARAMETERS</span></span>

### <span data-ttu-id="c9c3f-114">-Context</span><span class="sxs-lookup"><span data-stu-id="c9c3f-114">-Context</span></span>
<span data-ttu-id="c9c3f-115">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="c9c3f-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c9c3f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9c3f-116">-DefaultProfile</span></span>
<span data-ttu-id="c9c3f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c9c3f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9c3f-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c9c3f-118">-InputObject</span></span>
<span data-ttu-id="c9c3f-119">Instanz von PsApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="c9c3f-119">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="c9c3f-120">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c9c3f-120">This parameter is required.</span></span>

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

### <span data-ttu-id="c9c3f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9c3f-121">-PassThru</span></span>
<span data-ttu-id="c9c3f-122">Gibt an, dass dieses Cmdlet einen Wert von $true zurückgibt, wenn dies erfolgreich ist, oder einen Wert von $false, andernfalls.</span><span class="sxs-lookup"><span data-stu-id="c9c3f-122">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="c9c3f-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c9c3f-123">-ResourceId</span></span>
<span data-ttu-id="c9c3f-124">Arm-resourcenummer des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="c9c3f-124">Arm ResourceId of Subscription.</span></span> <span data-ttu-id="c9c3f-125">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c9c3f-125">This parameter is required.</span></span>

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

### <span data-ttu-id="c9c3f-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="c9c3f-126">-SubscriptionId</span></span>
<span data-ttu-id="c9c3f-127">Gibt die Abonnement-ID an.</span><span class="sxs-lookup"><span data-stu-id="c9c3f-127">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="c9c3f-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c9c3f-128">-Confirm</span></span>
<span data-ttu-id="c9c3f-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c9c3f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9c3f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9c3f-130">-WhatIf</span></span>
<span data-ttu-id="c9c3f-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c9c3f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9c3f-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c9c3f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9c3f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9c3f-133">CommonParameters</span></span>
<span data-ttu-id="c9c3f-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9c3f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9c3f-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9c3f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9c3f-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c9c3f-136">INPUTS</span></span>

### <span data-ttu-id="c9c3f-137">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c9c3f-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c9c3f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c9c3f-138">System.String</span></span>

### <span data-ttu-id="c9c3f-139">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="c9c3f-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c9c3f-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c9c3f-140">OUTPUTS</span></span>

### <span data-ttu-id="c9c3f-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c9c3f-141">System.Boolean</span></span>

## <span data-ttu-id="c9c3f-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="c9c3f-142">NOTES</span></span>

## <span data-ttu-id="c9c3f-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c9c3f-143">RELATED LINKS</span></span>

[<span data-ttu-id="c9c3f-144">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c9c3f-144">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="c9c3f-145">Neu – AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c9c3f-145">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="c9c3f-146">Satz-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c9c3f-146">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


