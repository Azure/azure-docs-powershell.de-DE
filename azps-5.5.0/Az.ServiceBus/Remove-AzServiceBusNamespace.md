---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
ms.openlocfilehash: 49b6a29410bd6c670e74b072a48b6f2a79e8fd0f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156340"
---
# <span data-ttu-id="64ab6-101">Remove-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="64ab6-101">Remove-AzServiceBusNamespace</span></span>

## <span data-ttu-id="64ab6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64ab6-102">SYNOPSIS</span></span>
<span data-ttu-id="64ab6-103">Entfernt den Namespace aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="64ab6-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="64ab6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64ab6-104">SYNTAX</span></span>

### <span data-ttu-id="64ab6-105">NamespacePropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="64ab6-105">NamespacePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64ab6-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="64ab6-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64ab6-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="64ab6-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64ab6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64ab6-108">DESCRIPTION</span></span>
<span data-ttu-id="64ab6-109">Das **Cmdlet "Remove-AzServiceBusNamespace"** entfernt den Namespace aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="64ab6-109">The **Remove-AzServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="64ab6-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="64ab6-110">EXAMPLES</span></span>

### <span data-ttu-id="64ab6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="64ab6-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="64ab6-112">Entfernt den Service Bus-Namespace `SB-Example1` aus der angegebenen Ressourcengruppe. `Default-ServiceBus-WestUS`</span><span class="sxs-lookup"><span data-stu-id="64ab6-112">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

### <span data-ttu-id="64ab6-113">Beispiel 2.1 – InputObject – Using variable:</span><span class="sxs-lookup"><span data-stu-id="64ab6-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusNamespace <params>
PS C:\> Remove-AzServiceBusNamespace -InputObject $inputobject
```

<span data-ttu-id="64ab6-114">Entfernt den service bus-Namespace, der über das $inputobject.</span><span class="sxs-lookup"><span data-stu-id="64ab6-114">Removes the Service Bus namespace provided through the $inputobject.</span></span>

### <span data-ttu-id="64ab6-115">Beispiel 2.2 – InputObject – Mithilfe der Piping:</span><span class="sxs-lookup"><span data-stu-id="64ab6-115">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusNamespace <params> | Remove-AzServiceBusNamespace
```

<span data-ttu-id="64ab6-116">Entfernt den Namespace "Service Bus" mithilfe der Piping.</span><span class="sxs-lookup"><span data-stu-id="64ab6-116">Removes the Service Bus namespace using Piping.</span></span>

### <span data-ttu-id="64ab6-117">Beispiel 3 – ResourceId</span><span class="sxs-lookup"><span data-stu-id="64ab6-117">Example 3 - ResourceId</span></span>
```
PS c:\> $ResourceId = (Get-AzResource -ResourceType Microsoft.ServiceBus/namespaces).ResourceId
PS C:\> Remove-AzServiceBusNamespace -ResourceId $resourceid
```

<span data-ttu-id="64ab6-118">Entfernt den Service Bus-Namespace, der über die ARM-ID in $resourceid "-ResourceId"-Parameter oder durch Piping bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="64ab6-118">Removes the Service Bus namespace provided through ARM id in $resourceid for -ResourceId parameter or through piping.</span></span>

## <span data-ttu-id="64ab6-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64ab6-119">PARAMETERS</span></span>

### <span data-ttu-id="64ab6-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64ab6-120">-AsJob</span></span>
<span data-ttu-id="64ab6-121">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="64ab6-121">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64ab6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64ab6-122">-DefaultProfile</span></span>
<span data-ttu-id="64ab6-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64ab6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64ab6-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64ab6-124">-InputObject</span></span>
<span data-ttu-id="64ab6-125">Service Bus Namespace Object</span><span class="sxs-lookup"><span data-stu-id="64ab6-125">Service Bus Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64ab6-126">-Name</span><span class="sxs-lookup"><span data-stu-id="64ab6-126">-Name</span></span>
<span data-ttu-id="64ab6-127">Namespacename.</span><span class="sxs-lookup"><span data-stu-id="64ab6-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64ab6-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64ab6-128">-PassThru</span></span>
<span data-ttu-id="64ab6-129">Wenn Sie diese Angabe angeben, wird "true" zurückgeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="64ab6-129">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64ab6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64ab6-130">-ResourceGroupName</span></span>
<span data-ttu-id="64ab6-131">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="64ab6-131">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: NamespacePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64ab6-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64ab6-132">-ResourceId</span></span>
<span data-ttu-id="64ab6-133">Ressourcen-ID des Dienstbusnamespaces</span><span class="sxs-lookup"><span data-stu-id="64ab6-133">Service Bus Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64ab6-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64ab6-134">-Confirm</span></span>
<span data-ttu-id="64ab6-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="64ab6-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64ab6-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="64ab6-136">-WhatIf</span></span>
<span data-ttu-id="64ab6-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="64ab6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64ab6-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="64ab6-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64ab6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64ab6-139">CommonParameters</span></span>
<span data-ttu-id="64ab6-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64ab6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64ab6-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64ab6-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64ab6-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="64ab6-142">INPUTS</span></span>

### <span data-ttu-id="64ab6-143">System.String</span><span class="sxs-lookup"><span data-stu-id="64ab6-143">System.String</span></span>

### <span data-ttu-id="64ab6-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="64ab6-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="64ab6-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="64ab6-145">OUTPUTS</span></span>

### <span data-ttu-id="64ab6-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="64ab6-146">System.Boolean</span></span>

## <span data-ttu-id="64ab6-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="64ab6-147">NOTES</span></span>

## <span data-ttu-id="64ab6-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="64ab6-148">RELATED LINKS</span></span>
