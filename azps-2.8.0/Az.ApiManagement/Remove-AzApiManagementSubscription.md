---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
ms.openlocfilehash: 5d3ad3481a57f2578678daa88c1f3e87e9893f7c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658171"
---
# <span data-ttu-id="4b54b-101">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4b54b-101">Remove-AzApiManagementSubscription</span></span>

## <span data-ttu-id="4b54b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4b54b-102">SYNOPSIS</span></span>
<span data-ttu-id="4b54b-103">Löscht ein vorhandenes Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4b54b-103">Deletes an existing subscription.</span></span>

## <span data-ttu-id="4b54b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b54b-104">SYNTAX</span></span>

### <span data-ttu-id="4b54b-105">Expanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="4b54b-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b54b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4b54b-106">ByInputObject</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -InputObject <PsApiManagementSubscription> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b54b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4b54b-107">ByResourceId</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4b54b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b54b-108">DESCRIPTION</span></span>
<span data-ttu-id="4b54b-109">Das Cmdlet **Remove-AzApiManagementSubscription** löscht ein vorhandenes Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4b54b-109">The **Remove-AzApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="4b54b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4b54b-110">EXAMPLES</span></span>

### <span data-ttu-id="4b54b-111">Beispiel 1: Löschen eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="4b54b-111">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="4b54b-112">Mit diesem Befehl wird ein vorhandenes Abonnement gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4b54b-112">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="4b54b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b54b-113">PARAMETERS</span></span>

### <span data-ttu-id="4b54b-114">-Context</span><span class="sxs-lookup"><span data-stu-id="4b54b-114">-Context</span></span>
<span data-ttu-id="4b54b-115">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="4b54b-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4b54b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b54b-116">-DefaultProfile</span></span>
<span data-ttu-id="4b54b-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4b54b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b54b-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4b54b-118">-InputObject</span></span>
<span data-ttu-id="4b54b-119">Instanz von PsApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="4b54b-119">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="4b54b-120">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4b54b-120">This parameter is required.</span></span>

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

### <span data-ttu-id="4b54b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b54b-121">-PassThru</span></span>
<span data-ttu-id="4b54b-122">Gibt an, dass dieses Cmdlet einen Wert von $true zurückgibt, wenn dies erfolgreich ist, oder einen Wert von $false, andernfalls.</span><span class="sxs-lookup"><span data-stu-id="4b54b-122">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="4b54b-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4b54b-123">-ResourceId</span></span>
<span data-ttu-id="4b54b-124">Arm-resourcenummer des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="4b54b-124">Arm ResourceId of Subscription.</span></span> <span data-ttu-id="4b54b-125">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4b54b-125">This parameter is required.</span></span>

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

### <span data-ttu-id="4b54b-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="4b54b-126">-SubscriptionId</span></span>
<span data-ttu-id="4b54b-127">Gibt die Abonnement-ID an.</span><span class="sxs-lookup"><span data-stu-id="4b54b-127">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="4b54b-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4b54b-128">-Confirm</span></span>
<span data-ttu-id="4b54b-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4b54b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b54b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b54b-130">-WhatIf</span></span>
<span data-ttu-id="4b54b-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4b54b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b54b-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4b54b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b54b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b54b-133">CommonParameters</span></span>
<span data-ttu-id="4b54b-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b54b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b54b-135">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b54b-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b54b-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4b54b-136">INPUTS</span></span>

### <span data-ttu-id="4b54b-137">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4b54b-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4b54b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4b54b-138">System.String</span></span>

### <span data-ttu-id="4b54b-139">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="4b54b-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4b54b-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4b54b-140">OUTPUTS</span></span>

### <span data-ttu-id="4b54b-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4b54b-141">System.Boolean</span></span>

## <span data-ttu-id="4b54b-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="4b54b-142">NOTES</span></span>

## <span data-ttu-id="4b54b-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4b54b-143">RELATED LINKS</span></span>

[<span data-ttu-id="4b54b-144">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4b54b-144">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="4b54b-145">Neu – AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4b54b-145">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="4b54b-146">Satz-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4b54b-146">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


