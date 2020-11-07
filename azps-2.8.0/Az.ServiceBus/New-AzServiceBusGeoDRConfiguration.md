---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 92bea9777d29a3cdf13007e743b1e7d929c8df40
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823256"
---
# <span data-ttu-id="11973-101">New-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="11973-101">New-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="11973-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="11973-102">SYNOPSIS</span></span>
<span data-ttu-id="11973-103">Erstellt einen neuen Alias (Disaster Recovery-Konfiguration)</span><span class="sxs-lookup"><span data-stu-id="11973-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="11973-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="11973-104">SYNTAX</span></span>

### <span data-ttu-id="11973-105">GeoDRPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="11973-105">GeoDRPropertiesSet (Default)</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11973-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="11973-106">NamespaceInputObjectSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11973-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11973-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11973-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11973-108">DESCRIPTION</span></span>
<span data-ttu-id="11973-109">Das Cmdlet " **New-AzServiceBusGeoDRConfiguration** " erstellt einen neuen Alias (Disaster Recovery-Konfiguration).</span><span class="sxs-lookup"><span data-stu-id="11973-109">The **New-AzServiceBusGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="11973-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="11973-110">EXAMPLES</span></span>

### <span data-ttu-id="11973-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="11973-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "/subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : /subscriptions/{SubscriptionId}/resourceGroups/TestignGeoDR/providers/Microsoft.ServiceBus/namespaces/SampleNamespaceSecondary
Role              : Primary
```

<span data-ttu-id="11973-112">Erstellt einen Alias "SampleDRConfigName" mit dem primären Namespace "SampleNamespace_Primary" mit sekundärem Namespace "SampleNamespace_Secondary".</span><span class="sxs-lookup"><span data-stu-id="11973-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="11973-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="11973-113">PARAMETERS</span></span>

### <span data-ttu-id="11973-114">-Alternatename</span><span class="sxs-lookup"><span data-stu-id="11973-114">-AlternateName</span></span>
<span data-ttu-id="11973-115">Alternativname</span><span class="sxs-lookup"><span data-stu-id="11973-115">AlternateName</span></span>

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

### <span data-ttu-id="11973-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11973-116">-AsJob</span></span>
<span data-ttu-id="11973-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="11973-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11973-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11973-118">-DefaultProfile</span></span>
<span data-ttu-id="11973-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="11973-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11973-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="11973-120">-InputObject</span></span>
<span data-ttu-id="11973-121">Namespace-Objekt</span><span class="sxs-lookup"><span data-stu-id="11973-121">Namespace Object</span></span>

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

### <span data-ttu-id="11973-122">-Name</span><span class="sxs-lookup"><span data-stu-id="11973-122">-Name</span></span>
<span data-ttu-id="11973-123">Dr-Konfigurations Name</span><span class="sxs-lookup"><span data-stu-id="11973-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="11973-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="11973-124">-Namespace</span></span>
<span data-ttu-id="11973-125">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="11973-125">Namespace Name</span></span>

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

### <span data-ttu-id="11973-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="11973-126">-PartnerNamespace</span></span>
<span data-ttu-id="11973-127">Dr-Konfigurations PartnerNamespace (Arm-ID von PartnerNamespace [sekundärer Namespace])</span><span class="sxs-lookup"><span data-stu-id="11973-127">DR Configuration PartnerNamespace (ARM Id of PartnerNamespace [Secondary namespace])</span></span>

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

### <span data-ttu-id="11973-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11973-128">-ResourceGroupName</span></span>
<span data-ttu-id="11973-129">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="11973-129">Resource Group Name</span></span>

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

### <span data-ttu-id="11973-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="11973-130">-ResourceId</span></span>
<span data-ttu-id="11973-131">Namespace-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="11973-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="11973-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="11973-132">-Confirm</span></span>
<span data-ttu-id="11973-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="11973-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11973-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11973-134">-WhatIf</span></span>
<span data-ttu-id="11973-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="11973-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11973-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="11973-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11973-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11973-137">CommonParameters</span></span>
<span data-ttu-id="11973-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11973-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11973-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11973-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11973-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="11973-140">INPUTS</span></span>

### <span data-ttu-id="11973-141">System. String</span><span class="sxs-lookup"><span data-stu-id="11973-141">System.String</span></span>

### <span data-ttu-id="11973-142">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="11973-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="11973-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="11973-143">OUTPUTS</span></span>

### <span data-ttu-id="11973-144">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="11973-144">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="11973-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="11973-145">NOTES</span></span>

## <span data-ttu-id="11973-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="11973-146">RELATED LINKS</span></span>
