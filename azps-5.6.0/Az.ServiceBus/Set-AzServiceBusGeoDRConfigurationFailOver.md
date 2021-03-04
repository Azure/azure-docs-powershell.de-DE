---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/set-azservicebusgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
ms.openlocfilehash: 97bc209408190605059e2308091fd60f6366940c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933451"
---
# <span data-ttu-id="e3304-101">Set-AzServiceBusGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="e3304-101">Set-AzServiceBusGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="e3304-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3304-102">SYNOPSIS</span></span>
<span data-ttu-id="e3304-103">Ruft das GEO DR-Failover auf, und konfigurieren Sie den Alias neu, um auf den sekundären Namespace zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="e3304-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="e3304-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e3304-104">SYNTAX</span></span>

### <span data-ttu-id="e3304-105">GeoDRPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e3304-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3304-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e3304-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3304-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3304-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3304-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e3304-108">DESCRIPTION</span></span>
<span data-ttu-id="e3304-109">Das **Cmdlet Set-AzServiceBusGeoDRConfigurationFailOver ruft** das GEO DR-Failover auf und konfiguriert den Alias so, dass er auf den sekundären Namespace zeigt.</span><span class="sxs-lookup"><span data-stu-id="e3304-109">The **Set-AzServiceBusGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="e3304-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e3304-110">EXAMPLES</span></span>

### <span data-ttu-id="e3304-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e3304-111">Example 1</span></span>
```
PS C:\> Set-AzServiceBusGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="e3304-112">Ruft den Failover über alias "SampleDRConfigName" auf, konfiguriert und zeigt auf sekundären Namespace "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="e3304-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="e3304-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e3304-113">PARAMETERS</span></span>

### <span data-ttu-id="e3304-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3304-114">-DefaultProfile</span></span>
<span data-ttu-id="e3304-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e3304-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3304-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3304-116">-InputObject</span></span>
<span data-ttu-id="e3304-117">Service Bus GeoDR Configuration Object</span><span class="sxs-lookup"><span data-stu-id="e3304-117">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="e3304-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e3304-118">-Name</span></span>
<span data-ttu-id="e3304-119">DR-Konfigurationsname – Alias</span><span class="sxs-lookup"><span data-stu-id="e3304-119">DR Configuration Name - Alias</span></span>

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

### <span data-ttu-id="e3304-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e3304-120">-Namespace</span></span>
<span data-ttu-id="e3304-121">Namespacename – Sekundärer Namespace</span><span class="sxs-lookup"><span data-stu-id="e3304-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="e3304-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3304-122">-PassThru</span></span>
<span data-ttu-id="e3304-123">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="e3304-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e3304-124">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="e3304-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e3304-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3304-125">-ResourceGroupName</span></span>
<span data-ttu-id="e3304-126">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="e3304-126">Resource Group Name</span></span>

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

### <span data-ttu-id="e3304-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3304-127">-ResourceId</span></span>
<span data-ttu-id="e3304-128">GeoDRConfiguration Resource Id</span><span class="sxs-lookup"><span data-stu-id="e3304-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="e3304-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e3304-129">-Confirm</span></span>
<span data-ttu-id="e3304-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e3304-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3304-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3304-131">-WhatIf</span></span>
<span data-ttu-id="e3304-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e3304-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3304-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e3304-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3304-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3304-134">CommonParameters</span></span>
<span data-ttu-id="e3304-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3304-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3304-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3304-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3304-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e3304-137">INPUTS</span></span>

### <span data-ttu-id="e3304-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e3304-138">System.String</span></span>

### <span data-ttu-id="e3304-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="e3304-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="e3304-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e3304-140">OUTPUTS</span></span>

### <span data-ttu-id="e3304-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e3304-141">System.Boolean</span></span>

## <span data-ttu-id="e3304-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e3304-142">NOTES</span></span>

## <span data-ttu-id="e3304-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e3304-143">RELATED LINKS</span></span>
