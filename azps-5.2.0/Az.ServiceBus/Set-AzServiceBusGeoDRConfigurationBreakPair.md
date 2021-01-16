---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationBreakPair.md
ms.openlocfilehash: f45899b1c2d397245461a10a6e2648f92dc9da40
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305363"
---
# <span data-ttu-id="edb84-101">Set-AzServiceBusGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="edb84-101">Set-AzServiceBusGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="edb84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edb84-102">SYNOPSIS</span></span>
<span data-ttu-id="edb84-103">Dieser Vorgang deaktiviert die Notfallwiederherstellung und beendet das Replizieren von Änderungen vom primären in den sekundären Namespace.</span><span class="sxs-lookup"><span data-stu-id="edb84-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="edb84-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="edb84-104">SYNTAX</span></span>

### <span data-ttu-id="edb84-105">GeoDRPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="edb84-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="edb84-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="edb84-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edb84-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="edb84-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edb84-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="edb84-108">DESCRIPTION</span></span>
<span data-ttu-id="edb84-109">Das **Cmdlet "Set-AzServiceBusGeoDRConfigurationBreakPair"** deaktiviert die Notfallwiederherstellung und beendet das Replizieren von Änderungen vom primären in den sekundären Namespace.</span><span class="sxs-lookup"><span data-stu-id="edb84-109">The **Set-AzServiceBusGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="edb84-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="edb84-110">EXAMPLES</span></span>

### <span data-ttu-id="edb84-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="edb84-111">Example 1</span></span>
```
PS C:\> Set-AzServiceBusGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"
```

<span data-ttu-id="edb84-112">Dieser Vorgang deaktiviert die Notfallwiederherstellung und beendet das Replizieren von Änderungen vom primären in den sekundären Namespace.</span><span class="sxs-lookup"><span data-stu-id="edb84-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="edb84-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="edb84-113">PARAMETERS</span></span>

### <span data-ttu-id="edb84-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edb84-114">-DefaultProfile</span></span>
<span data-ttu-id="edb84-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="edb84-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edb84-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="edb84-116">-InputObject</span></span>
<span data-ttu-id="edb84-117">Service Bus GeoDR Configuration Object</span><span class="sxs-lookup"><span data-stu-id="edb84-117">Service Bus GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="edb84-118">-Name</span><span class="sxs-lookup"><span data-stu-id="edb84-118">-Name</span></span>
<span data-ttu-id="edb84-119">Name der DR-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="edb84-119">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edb84-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="edb84-120">-Namespace</span></span>
<span data-ttu-id="edb84-121">Namespacename – Primärer Namespace</span><span class="sxs-lookup"><span data-stu-id="edb84-121">Namespace Name - Primary Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edb84-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="edb84-122">-PassThru</span></span>
<span data-ttu-id="edb84-123">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="edb84-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="edb84-124">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="edb84-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="edb84-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edb84-125">-ResourceGroupName</span></span>
<span data-ttu-id="edb84-126">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="edb84-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edb84-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="edb84-127">-ResourceId</span></span>
<span data-ttu-id="edb84-128">GeoDRConfiguration Resource Id</span><span class="sxs-lookup"><span data-stu-id="edb84-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edb84-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="edb84-129">-Confirm</span></span>
<span data-ttu-id="edb84-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="edb84-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edb84-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="edb84-131">-WhatIf</span></span>
<span data-ttu-id="edb84-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="edb84-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edb84-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="edb84-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edb84-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edb84-134">CommonParameters</span></span>
<span data-ttu-id="edb84-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edb84-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edb84-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edb84-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edb84-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="edb84-137">INPUTS</span></span>

### <span data-ttu-id="edb84-138">System.String</span><span class="sxs-lookup"><span data-stu-id="edb84-138">System.String</span></span>

### <span data-ttu-id="edb84-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="edb84-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="edb84-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="edb84-140">OUTPUTS</span></span>

### <span data-ttu-id="edb84-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="edb84-141">System.Boolean</span></span>

## <span data-ttu-id="edb84-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="edb84-142">NOTES</span></span>

## <span data-ttu-id="edb84-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="edb84-143">RELATED LINKS</span></span>
