---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
ms.openlocfilehash: c56637b8470e40e6b46984117a764da248684005
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662653"
---
# <span data-ttu-id="1fdfc-101">Remove-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="1fdfc-101">Remove-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="1fdfc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1fdfc-102">SYNOPSIS</span></span>
<span data-ttu-id="1fdfc-103">Entfernt den Namespace aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1fdfc-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fdfc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1fdfc-104">SYNTAX</span></span>

### <span data-ttu-id="1fdfc-105">NamespacePropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1fdfc-105">NamespacePropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fdfc-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1fdfc-106">NamespaceInputObjectSet</span></span>
```
Remove-AzureRmServiceBusNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fdfc-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fdfc-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzureRmServiceBusNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fdfc-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1fdfc-108">DESCRIPTION</span></span>
<span data-ttu-id="1fdfc-109">Das Cmdlet **Remove-AzureRmServiceBusNamespace** entfernt den Namespace aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1fdfc-109">The **Remove-AzureRmServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="1fdfc-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1fdfc-110">EXAMPLES</span></span>

### <span data-ttu-id="1fdfc-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1fdfc-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="1fdfc-112">Entfernt den ServiceBus-Namespace `SB-Example1` aus der angegebenen Ressourcengruppe `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="1fdfc-112">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

### <span data-ttu-id="1fdfc-113">Beispiel 2,1-Inputobject-using-Variable:</span><span class="sxs-lookup"><span data-stu-id="1fdfc-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusNamespace <params>
PS C:\> Remove-AzureRmServiceBusNamespace -InputObject $inputobject
```

<span data-ttu-id="1fdfc-114">Entfernt den ServiceBus-Namespace, der über die $Inputobject bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="1fdfc-114">Removes the Service Bus namespace provided through the $inputobject.</span></span>

### <span data-ttu-id="1fdfc-115">Beispiel 2,2-Inputobject-using Piping:</span><span class="sxs-lookup"><span data-stu-id="1fdfc-115">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespace <params> | Remove-AzureRmServiceBusNamespace
```

<span data-ttu-id="1fdfc-116">Entfernt den ServiceBus-Namespace mithilfe von Piping.</span><span class="sxs-lookup"><span data-stu-id="1fdfc-116">Removes the Service Bus namespace using Piping.</span></span>

### <span data-ttu-id="1fdfc-117">Beispiel 3-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1fdfc-117">Example 3 - ResourceId</span></span>
```
PS c:\> $ResourceId = (Get-AzureRmResource -ResourceType Microsoft.ServiceBus/namespaces).ResourceId
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceId $resourceid
```

<span data-ttu-id="1fdfc-118">Entfernt den ServiceBus-Namespace, der über die Arm-ID bereitgestellt wird, in $ResourceId für-Resourcen-Parameter oder durch Rohrleitungen.</span><span class="sxs-lookup"><span data-stu-id="1fdfc-118">Removes the Service Bus namespace provided through ARM id in $resourceid for -ResourceId parameter or through piping.</span></span>

## <span data-ttu-id="1fdfc-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="1fdfc-119">PARAMETERS</span></span>

### <span data-ttu-id="1fdfc-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1fdfc-120">-AsJob</span></span>
<span data-ttu-id="1fdfc-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1fdfc-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1fdfc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fdfc-122">-DefaultProfile</span></span>
<span data-ttu-id="1fdfc-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1fdfc-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fdfc-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1fdfc-124">-InputObject</span></span>
<span data-ttu-id="1fdfc-125">ServiceBus-Namespace Objekt</span><span class="sxs-lookup"><span data-stu-id="1fdfc-125">Service Bus Namespace Object</span></span>

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

### <span data-ttu-id="1fdfc-126">-Name</span><span class="sxs-lookup"><span data-stu-id="1fdfc-126">-Name</span></span>
<span data-ttu-id="1fdfc-127">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="1fdfc-127">Namespace Name.</span></span>

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

### <span data-ttu-id="1fdfc-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1fdfc-128">-PassThru</span></span>
<span data-ttu-id="1fdfc-129">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="1fdfc-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="1fdfc-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fdfc-130">-ResourceGroupName</span></span>
<span data-ttu-id="1fdfc-131">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="1fdfc-131">The name of the resource group</span></span>

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

### <span data-ttu-id="1fdfc-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1fdfc-132">-ResourceId</span></span>
<span data-ttu-id="1fdfc-133">Service Bus-Namespace-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="1fdfc-133">Service Bus Namespace Resource Id</span></span>

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

### <span data-ttu-id="1fdfc-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1fdfc-134">-Confirm</span></span>
<span data-ttu-id="1fdfc-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1fdfc-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fdfc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fdfc-136">-WhatIf</span></span>
<span data-ttu-id="1fdfc-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1fdfc-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fdfc-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1fdfc-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fdfc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fdfc-139">CommonParameters</span></span>
<span data-ttu-id="1fdfc-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fdfc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fdfc-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fdfc-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fdfc-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1fdfc-142">INPUTS</span></span>

### <span data-ttu-id="1fdfc-143">System. String</span><span class="sxs-lookup"><span data-stu-id="1fdfc-143">System.String</span></span>

### <span data-ttu-id="1fdfc-144">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="1fdfc-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="1fdfc-145">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1fdfc-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="1fdfc-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1fdfc-146">OUTPUTS</span></span>

### <span data-ttu-id="1fdfc-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1fdfc-147">System.Boolean</span></span>

## <span data-ttu-id="1fdfc-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="1fdfc-148">NOTES</span></span>

## <span data-ttu-id="1fdfc-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1fdfc-149">RELATED LINKS</span></span>
