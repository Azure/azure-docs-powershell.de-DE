---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 1bb881d96b0247b4cc6d59171c146d75f6df9de0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371243"
---
# <span data-ttu-id="f1c01-101">New-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1c01-101">New-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="f1c01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1c01-102">SYNOPSIS</span></span>
<span data-ttu-id="f1c01-103">Erstellt einen neuen Alias (Notfallwiederherstellungskonfiguration)</span><span class="sxs-lookup"><span data-stu-id="f1c01-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="f1c01-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1c01-104">SYNTAX</span></span>

### <span data-ttu-id="f1c01-105">GeoDRPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f1c01-105">GeoDRPropertiesSet (Default)</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1c01-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f1c01-106">NamespaceInputObjectSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1c01-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1c01-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1c01-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1c01-108">DESCRIPTION</span></span>
<span data-ttu-id="f1c01-109">Das **Cmdlet "New-AzServiceBusGeoDRConfiguration"** erstellt einen neuen Alias (Notfallwiederherstellungskonfiguration)</span><span class="sxs-lookup"><span data-stu-id="f1c01-109">The **New-AzServiceBusGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="f1c01-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f1c01-110">EXAMPLES</span></span>

### <span data-ttu-id="f1c01-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f1c01-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "/subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : /subscriptions/{SubscriptionId}/resourceGroups/TestignGeoDR/providers/Microsoft.ServiceBus/namespaces/SampleNamespaceSecondary
Role              : Primary
```

<span data-ttu-id="f1c01-112">Erstellt einen Alias "SampleDRConfigName" mit dem primären Namespace "SampleNamespace_Primary" mit dem sekundären Namespace "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="f1c01-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="f1c01-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1c01-113">PARAMETERS</span></span>

### <span data-ttu-id="f1c01-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="f1c01-114">-AlternateName</span></span>
<span data-ttu-id="f1c01-115">AlternateName</span><span class="sxs-lookup"><span data-stu-id="f1c01-115">AlternateName</span></span>

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

### <span data-ttu-id="f1c01-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1c01-116">-AsJob</span></span>
<span data-ttu-id="f1c01-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f1c01-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1c01-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1c01-118">-DefaultProfile</span></span>
<span data-ttu-id="f1c01-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1c01-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1c01-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1c01-120">-InputObject</span></span>
<span data-ttu-id="f1c01-121">Namespaceobjekt</span><span class="sxs-lookup"><span data-stu-id="f1c01-121">Namespace Object</span></span>

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

### <span data-ttu-id="f1c01-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f1c01-122">-Name</span></span>
<span data-ttu-id="f1c01-123">Name der DR-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="f1c01-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="f1c01-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f1c01-124">-Namespace</span></span>
<span data-ttu-id="f1c01-125">Namespacename</span><span class="sxs-lookup"><span data-stu-id="f1c01-125">Namespace Name</span></span>

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

### <span data-ttu-id="f1c01-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="f1c01-126">-PartnerNamespace</span></span>
<span data-ttu-id="f1c01-127">DR Configuration PartnerNamespace (ARM ID of PartnerNamespace [Secondary namespace])</span><span class="sxs-lookup"><span data-stu-id="f1c01-127">DR Configuration PartnerNamespace (ARM Id of PartnerNamespace [Secondary namespace])</span></span>

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

### <span data-ttu-id="f1c01-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1c01-128">-ResourceGroupName</span></span>
<span data-ttu-id="f1c01-129">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="f1c01-129">Resource Group Name</span></span>

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

### <span data-ttu-id="f1c01-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1c01-130">-ResourceId</span></span>
<span data-ttu-id="f1c01-131">Namespaceressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="f1c01-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="f1c01-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1c01-132">-Confirm</span></span>
<span data-ttu-id="f1c01-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1c01-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1c01-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f1c01-134">-WhatIf</span></span>
<span data-ttu-id="f1c01-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1c01-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1c01-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f1c01-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1c01-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1c01-137">CommonParameters</span></span>
<span data-ttu-id="f1c01-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1c01-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1c01-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1c01-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1c01-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f1c01-140">INPUTS</span></span>

### <span data-ttu-id="f1c01-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f1c01-141">System.String</span></span>

### <span data-ttu-id="f1c01-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="f1c01-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="f1c01-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f1c01-143">OUTPUTS</span></span>

### <span data-ttu-id="f1c01-144">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="f1c01-144">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="f1c01-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f1c01-145">NOTES</span></span>

## <span data-ttu-id="f1c01-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f1c01-146">RELATED LINKS</span></span>
