---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: c226f11eecc7cf046234378be7f0417da301cf40
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168876"
---
# <span data-ttu-id="5239b-101">Remove-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="5239b-101">Remove-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="5239b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5239b-102">SYNOPSIS</span></span>
<span data-ttu-id="5239b-103">Löscht einen Alias (Notfallwiederherstellungskonfiguration)</span><span class="sxs-lookup"><span data-stu-id="5239b-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="5239b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5239b-104">SYNTAX</span></span>

### <span data-ttu-id="5239b-105">GeoDRPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5239b-105">GeoDRPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5239b-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5239b-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5239b-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5239b-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5239b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5239b-108">DESCRIPTION</span></span>
<span data-ttu-id="5239b-109">Das **Cmdlet "Remove-AzServiceBusGeoDRConfiguration"** löscht einen Alias (Notfallwiederherstellungskonfiguration)</span><span class="sxs-lookup"><span data-stu-id="5239b-109">The **Remove-AzServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="5239b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5239b-110">EXAMPLES</span></span>

### <span data-ttu-id="5239b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5239b-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="5239b-112">Löscht einen Alias (Notfallwiederherstellungskonfiguration)</span><span class="sxs-lookup"><span data-stu-id="5239b-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="5239b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5239b-113">PARAMETERS</span></span>

### <span data-ttu-id="5239b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5239b-114">-AsJob</span></span>
<span data-ttu-id="5239b-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5239b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5239b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5239b-116">-DefaultProfile</span></span>
<span data-ttu-id="5239b-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5239b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5239b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5239b-118">-InputObject</span></span>
<span data-ttu-id="5239b-119">Service Bus GeoDR Configuration Object</span><span class="sxs-lookup"><span data-stu-id="5239b-119">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="5239b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5239b-120">-Name</span></span>
<span data-ttu-id="5239b-121">Aliasname (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="5239b-121">Alias (GeoDR) Name</span></span>

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

### <span data-ttu-id="5239b-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5239b-122">-Namespace</span></span>
<span data-ttu-id="5239b-123">Namespacename</span><span class="sxs-lookup"><span data-stu-id="5239b-123">Namespace Name</span></span>

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

### <span data-ttu-id="5239b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5239b-124">-PassThru</span></span>
<span data-ttu-id="5239b-125">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="5239b-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5239b-126">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="5239b-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5239b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5239b-127">-ResourceGroupName</span></span>
<span data-ttu-id="5239b-128">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="5239b-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5239b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5239b-129">-ResourceId</span></span>
<span data-ttu-id="5239b-130">GeoDRConfiguration Resource Id</span><span class="sxs-lookup"><span data-stu-id="5239b-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="5239b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5239b-131">-Confirm</span></span>
<span data-ttu-id="5239b-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5239b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5239b-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5239b-133">-WhatIf</span></span>
<span data-ttu-id="5239b-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5239b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5239b-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5239b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5239b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5239b-136">CommonParameters</span></span>
<span data-ttu-id="5239b-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5239b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5239b-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5239b-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5239b-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5239b-139">INPUTS</span></span>

### <span data-ttu-id="5239b-140">System.String</span><span class="sxs-lookup"><span data-stu-id="5239b-140">System.String</span></span>

### <span data-ttu-id="5239b-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="5239b-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="5239b-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5239b-142">OUTPUTS</span></span>

### <span data-ttu-id="5239b-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5239b-143">System.Boolean</span></span>

## <span data-ttu-id="5239b-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5239b-144">NOTES</span></span>

## <span data-ttu-id="5239b-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5239b-145">RELATED LINKS</span></span>
