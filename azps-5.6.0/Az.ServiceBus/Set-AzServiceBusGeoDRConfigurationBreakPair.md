---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/set-azservicebusgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationBreakPair.md
ms.openlocfilehash: 3b308818df135606ac470bcf82d8cd2c0c12b37a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933456"
---
# <span data-ttu-id="39227-101">Set-AzServiceBusGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="39227-101">Set-AzServiceBusGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="39227-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39227-102">SYNOPSIS</span></span>
<span data-ttu-id="39227-103">Dieser Vorgang deaktiviert die Notfallwiederherstellung und beendet das Replizieren von Änderungen von primären in sekundären Namespaces.</span><span class="sxs-lookup"><span data-stu-id="39227-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="39227-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39227-104">SYNTAX</span></span>

### <span data-ttu-id="39227-105">GeoDRPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="39227-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="39227-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="39227-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39227-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="39227-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39227-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="39227-108">DESCRIPTION</span></span>
<span data-ttu-id="39227-109">Das **Cmdlet Set-AzServiceBusGeoDRConfigurationBreakPair** deaktiviert das Disaster Recovery und beendet das Replizieren von Änderungen von primären in sekundären Namespaces.</span><span class="sxs-lookup"><span data-stu-id="39227-109">The **Set-AzServiceBusGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="39227-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="39227-110">EXAMPLES</span></span>

### <span data-ttu-id="39227-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="39227-111">Example 1</span></span>
```
PS C:\> Set-AzServiceBusGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"
```

<span data-ttu-id="39227-112">Dieser Vorgang deaktiviert die Notfallwiederherstellung und beendet das Replizieren von Änderungen von primären in sekundären Namespaces.</span><span class="sxs-lookup"><span data-stu-id="39227-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="39227-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="39227-113">PARAMETERS</span></span>

### <span data-ttu-id="39227-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39227-114">-DefaultProfile</span></span>
<span data-ttu-id="39227-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39227-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39227-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39227-116">-InputObject</span></span>
<span data-ttu-id="39227-117">Service Bus GeoDR Configuration Object</span><span class="sxs-lookup"><span data-stu-id="39227-117">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="39227-118">-Name</span><span class="sxs-lookup"><span data-stu-id="39227-118">-Name</span></span>
<span data-ttu-id="39227-119">NAME der DR-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="39227-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="39227-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="39227-120">-Namespace</span></span>
<span data-ttu-id="39227-121">Namespacename – Primärer Namespace</span><span class="sxs-lookup"><span data-stu-id="39227-121">Namespace Name - Primary Namespace</span></span>

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

### <span data-ttu-id="39227-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39227-122">-PassThru</span></span>
<span data-ttu-id="39227-123">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="39227-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="39227-124">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="39227-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="39227-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39227-125">-ResourceGroupName</span></span>
<span data-ttu-id="39227-126">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="39227-126">Resource Group Name</span></span>

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

### <span data-ttu-id="39227-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39227-127">-ResourceId</span></span>
<span data-ttu-id="39227-128">GeoDRConfiguration Resource Id</span><span class="sxs-lookup"><span data-stu-id="39227-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="39227-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="39227-129">-Confirm</span></span>
<span data-ttu-id="39227-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="39227-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39227-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39227-131">-WhatIf</span></span>
<span data-ttu-id="39227-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39227-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39227-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39227-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39227-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39227-134">CommonParameters</span></span>
<span data-ttu-id="39227-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39227-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39227-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39227-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39227-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="39227-137">INPUTS</span></span>

### <span data-ttu-id="39227-138">System.String</span><span class="sxs-lookup"><span data-stu-id="39227-138">System.String</span></span>

### <span data-ttu-id="39227-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="39227-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="39227-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="39227-140">OUTPUTS</span></span>

### <span data-ttu-id="39227-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="39227-141">System.Boolean</span></span>

## <span data-ttu-id="39227-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="39227-142">NOTES</span></span>

## <span data-ttu-id="39227-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="39227-143">RELATED LINKS</span></span>
