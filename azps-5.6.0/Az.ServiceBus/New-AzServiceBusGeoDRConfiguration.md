---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/new-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 02335868ca9984d4da57be905b9600b81333b484
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920928"
---
# <span data-ttu-id="8366e-101">New-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="8366e-101">New-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="8366e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8366e-102">SYNOPSIS</span></span>
<span data-ttu-id="8366e-103">Erstellt einen neuen Alias(Notfallwiederherstellungskonfiguration)</span><span class="sxs-lookup"><span data-stu-id="8366e-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="8366e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8366e-104">SYNTAX</span></span>

### <span data-ttu-id="8366e-105">GeoDRPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8366e-105">GeoDRPropertiesSet (Default)</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8366e-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8366e-106">NamespaceInputObjectSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8366e-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8366e-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8366e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8366e-108">DESCRIPTION</span></span>
<span data-ttu-id="8366e-109">Das **Cmdlet New-AzServiceBusGeoDRConfiguration** Erstellt einen neuen Alias(Notfallwiederherstellungskonfiguration)</span><span class="sxs-lookup"><span data-stu-id="8366e-109">The **New-AzServiceBusGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="8366e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8366e-110">EXAMPLES</span></span>

### <span data-ttu-id="8366e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8366e-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "/subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : /subscriptions/{SubscriptionId}/resourceGroups/TestignGeoDR/providers/Microsoft.ServiceBus/namespaces/SampleNamespaceSecondary
Role              : Primary
```

<span data-ttu-id="8366e-112">Erstellt einen Alias "SampleDRConfigName" mit dem primären Namespace "SampleNamespace_Primary" mit dem sekundären Namespace "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="8366e-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="8366e-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8366e-113">PARAMETERS</span></span>

### <span data-ttu-id="8366e-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="8366e-114">-AlternateName</span></span>
<span data-ttu-id="8366e-115">Alternativname</span><span class="sxs-lookup"><span data-stu-id="8366e-115">AlternateName</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8366e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8366e-116">-AsJob</span></span>
<span data-ttu-id="8366e-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8366e-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8366e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8366e-118">-DefaultProfile</span></span>
<span data-ttu-id="8366e-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8366e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8366e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8366e-120">-InputObject</span></span>
<span data-ttu-id="8366e-121">Namespaceobjekt</span><span class="sxs-lookup"><span data-stu-id="8366e-121">Namespace Object</span></span>

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

### <span data-ttu-id="8366e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8366e-122">-Name</span></span>
<span data-ttu-id="8366e-123">NAME der DR-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="8366e-123">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8366e-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8366e-124">-Namespace</span></span>
<span data-ttu-id="8366e-125">Namespacename</span><span class="sxs-lookup"><span data-stu-id="8366e-125">Namespace Name</span></span>

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

### <span data-ttu-id="8366e-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="8366e-126">-PartnerNamespace</span></span>
<span data-ttu-id="8366e-127">DR Configuration PartnerNamespace (ARM Id of PartnerNamespace [Secondary namespace])</span><span class="sxs-lookup"><span data-stu-id="8366e-127">DR Configuration PartnerNamespace (ARM Id of PartnerNamespace [Secondary namespace])</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8366e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8366e-128">-ResourceGroupName</span></span>
<span data-ttu-id="8366e-129">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="8366e-129">Resource Group Name</span></span>

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

### <span data-ttu-id="8366e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8366e-130">-ResourceId</span></span>
<span data-ttu-id="8366e-131">Namespaceressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="8366e-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="8366e-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8366e-132">-Confirm</span></span>
<span data-ttu-id="8366e-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8366e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8366e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8366e-134">-WhatIf</span></span>
<span data-ttu-id="8366e-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8366e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8366e-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8366e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8366e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8366e-137">CommonParameters</span></span>
<span data-ttu-id="8366e-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8366e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8366e-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8366e-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8366e-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8366e-140">INPUTS</span></span>

### <span data-ttu-id="8366e-141">System.String</span><span class="sxs-lookup"><span data-stu-id="8366e-141">System.String</span></span>

### <span data-ttu-id="8366e-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="8366e-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="8366e-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8366e-143">OUTPUTS</span></span>

### <span data-ttu-id="8366e-144">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="8366e-144">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="8366e-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8366e-145">NOTES</span></span>

## <span data-ttu-id="8366e-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8366e-146">RELATED LINKS</span></span>
