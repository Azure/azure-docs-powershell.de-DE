---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
ms.openlocfilehash: 49b6a29410bd6c670e74b072a48b6f2a79e8fd0f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173532"
---
# <span data-ttu-id="a85eb-101">Remove-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="a85eb-101">Remove-AzServiceBusNamespace</span></span>

## <span data-ttu-id="a85eb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a85eb-102">SYNOPSIS</span></span>
<span data-ttu-id="a85eb-103">Entfernt den Namespace aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a85eb-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="a85eb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a85eb-104">SYNTAX</span></span>

### <span data-ttu-id="a85eb-105">NamespacePropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a85eb-105">NamespacePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a85eb-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a85eb-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a85eb-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a85eb-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a85eb-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a85eb-108">DESCRIPTION</span></span>
<span data-ttu-id="a85eb-109">Das Cmdlet **Remove-AzServiceBusNamespace** entfernt den Namespace aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a85eb-109">The **Remove-AzServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="a85eb-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a85eb-110">EXAMPLES</span></span>

### <span data-ttu-id="a85eb-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a85eb-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="a85eb-112">Entfernt den ServiceBus-Namespace `SB-Example1` aus der angegebenen Ressourcengruppe `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="a85eb-112">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

### <span data-ttu-id="a85eb-113">Beispiel 2,1-Inputobject-using-Variable:</span><span class="sxs-lookup"><span data-stu-id="a85eb-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusNamespace <params>
PS C:\> Remove-AzServiceBusNamespace -InputObject $inputobject
```

<span data-ttu-id="a85eb-114">Entfernt den ServiceBus-Namespace, der über die $Inputobject bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a85eb-114">Removes the Service Bus namespace provided through the $inputobject.</span></span>

### <span data-ttu-id="a85eb-115">Beispiel 2,2-Inputobject-using Piping:</span><span class="sxs-lookup"><span data-stu-id="a85eb-115">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusNamespace <params> | Remove-AzServiceBusNamespace
```

<span data-ttu-id="a85eb-116">Entfernt den ServiceBus-Namespace mithilfe von Piping.</span><span class="sxs-lookup"><span data-stu-id="a85eb-116">Removes the Service Bus namespace using Piping.</span></span>

### <span data-ttu-id="a85eb-117">Beispiel 3-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a85eb-117">Example 3 - ResourceId</span></span>
```
PS c:\> $ResourceId = (Get-AzResource -ResourceType Microsoft.ServiceBus/namespaces).ResourceId
PS C:\> Remove-AzServiceBusNamespace -ResourceId $resourceid
```

<span data-ttu-id="a85eb-118">Entfernt den ServiceBus-Namespace, der über die Arm-ID bereitgestellt wird, in $ResourceId für-Resourcen-Parameter oder durch Rohrleitungen.</span><span class="sxs-lookup"><span data-stu-id="a85eb-118">Removes the Service Bus namespace provided through ARM id in $resourceid for -ResourceId parameter or through piping.</span></span>

## <span data-ttu-id="a85eb-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="a85eb-119">PARAMETERS</span></span>

### <span data-ttu-id="a85eb-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a85eb-120">-AsJob</span></span>
<span data-ttu-id="a85eb-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a85eb-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a85eb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a85eb-122">-DefaultProfile</span></span>
<span data-ttu-id="a85eb-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a85eb-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a85eb-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a85eb-124">-InputObject</span></span>
<span data-ttu-id="a85eb-125">ServiceBus-Namespace Objekt</span><span class="sxs-lookup"><span data-stu-id="a85eb-125">Service Bus Namespace Object</span></span>

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

### <span data-ttu-id="a85eb-126">-Name</span><span class="sxs-lookup"><span data-stu-id="a85eb-126">-Name</span></span>
<span data-ttu-id="a85eb-127">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="a85eb-127">Namespace Name.</span></span>

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

### <span data-ttu-id="a85eb-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a85eb-128">-PassThru</span></span>
<span data-ttu-id="a85eb-129">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="a85eb-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="a85eb-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a85eb-130">-ResourceGroupName</span></span>
<span data-ttu-id="a85eb-131">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a85eb-131">The name of the resource group</span></span>

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

### <span data-ttu-id="a85eb-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a85eb-132">-ResourceId</span></span>
<span data-ttu-id="a85eb-133">Service Bus-Namespace-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="a85eb-133">Service Bus Namespace Resource Id</span></span>

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

### <span data-ttu-id="a85eb-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a85eb-134">-Confirm</span></span>
<span data-ttu-id="a85eb-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a85eb-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a85eb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a85eb-136">-WhatIf</span></span>
<span data-ttu-id="a85eb-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a85eb-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a85eb-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a85eb-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a85eb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a85eb-139">CommonParameters</span></span>
<span data-ttu-id="a85eb-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a85eb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a85eb-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a85eb-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a85eb-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a85eb-142">INPUTS</span></span>

### <span data-ttu-id="a85eb-143">System. String</span><span class="sxs-lookup"><span data-stu-id="a85eb-143">System.String</span></span>

### <span data-ttu-id="a85eb-144">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="a85eb-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="a85eb-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a85eb-145">OUTPUTS</span></span>

### <span data-ttu-id="a85eb-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a85eb-146">System.Boolean</span></span>

## <span data-ttu-id="a85eb-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="a85eb-147">NOTES</span></span>

## <span data-ttu-id="a85eb-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a85eb-148">RELATED LINKS</span></span>
