---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 83d1e9edde6e2e792a24e0dc943cf62068938c2d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469856"
---
# <span data-ttu-id="fe347-101">New-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe347-101">New-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="fe347-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe347-102">SYNOPSIS</span></span>
<span data-ttu-id="fe347-103">Erstellt einen neuen Alias (Notfallwiederherstellungskonfiguration)</span><span class="sxs-lookup"><span data-stu-id="fe347-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="fe347-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe347-104">SYNTAX</span></span>

### <span data-ttu-id="fe347-105">GeoDRParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fe347-105">GeoDRParameterSet (Default)</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe347-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fe347-106">NamespaceInputObjectSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe347-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe347-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe347-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fe347-108">DESCRIPTION</span></span>
<span data-ttu-id="fe347-109">Das **Cmdlet "New-AzEventHubGeoDRConfiguration"** erstellt einen neuen Alias (Notfallwiederherstellungskonfiguration)</span><span class="sxs-lookup"><span data-stu-id="fe347-109">The **New-AzEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="fe347-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fe347-110">EXAMPLES</span></span>

### <span data-ttu-id="fe347-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fe347-111">Example 1</span></span>
```
PS C:\> New-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="fe347-112">Erstellt einen Alias "SampleDRConfigName" mit dem primären Namespace "SampleNamespace_Primary" mit dem sekundären Namespace "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="fe347-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="fe347-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe347-113">PARAMETERS</span></span>

### <span data-ttu-id="fe347-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="fe347-114">-AlternateName</span></span>
<span data-ttu-id="fe347-115">AlternateName erforderlich, wenn der Name der Dr-Konfiguration mit dem primären Namespace identisch ist</span><span class="sxs-lookup"><span data-stu-id="fe347-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

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

### <span data-ttu-id="fe347-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe347-116">-AsJob</span></span>
<span data-ttu-id="fe347-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fe347-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe347-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe347-118">-DefaultProfile</span></span>
<span data-ttu-id="fe347-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fe347-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe347-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe347-120">-InputObject</span></span>
<span data-ttu-id="fe347-121">Namespaceobjekt</span><span class="sxs-lookup"><span data-stu-id="fe347-121">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe347-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fe347-122">-Name</span></span>
<span data-ttu-id="fe347-123">Name der DR-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="fe347-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="fe347-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fe347-124">-Namespace</span></span>
<span data-ttu-id="fe347-125">Namespacename</span><span class="sxs-lookup"><span data-stu-id="fe347-125">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe347-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="fe347-126">-PartnerNamespace</span></span>
<span data-ttu-id="fe347-127">DR Configuration PartnerNamespace ARM ID</span><span class="sxs-lookup"><span data-stu-id="fe347-127">DR Configuration PartnerNamespace ARM ID</span></span>

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

### <span data-ttu-id="fe347-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe347-128">-ResourceGroupName</span></span>
<span data-ttu-id="fe347-129">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="fe347-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe347-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe347-130">-ResourceId</span></span>
<span data-ttu-id="fe347-131">Namespaceressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="fe347-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="fe347-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe347-132">-Confirm</span></span>
<span data-ttu-id="fe347-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fe347-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe347-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fe347-134">-WhatIf</span></span>
<span data-ttu-id="fe347-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fe347-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe347-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fe347-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe347-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe347-137">CommonParameters</span></span>
<span data-ttu-id="fe347-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe347-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe347-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe347-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe347-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fe347-140">INPUTS</span></span>

### <span data-ttu-id="fe347-141">System.String</span><span class="sxs-lookup"><span data-stu-id="fe347-141">System.String</span></span>

### <span data-ttu-id="fe347-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="fe347-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="fe347-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fe347-143">OUTPUTS</span></span>

### <span data-ttu-id="fe347-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="fe347-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="fe347-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fe347-145">NOTES</span></span>

## <span data-ttu-id="fe347-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fe347-146">RELATED LINKS</span></span>
