---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 83d1e9edde6e2e792a24e0dc943cf62068938c2d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306576"
---
# <span data-ttu-id="df963-101">New-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="df963-101">New-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="df963-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df963-102">SYNOPSIS</span></span>
<span data-ttu-id="df963-103">Erstellt einen neuen Alias (Notfallwiederherstellungskonfiguration)</span><span class="sxs-lookup"><span data-stu-id="df963-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="df963-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df963-104">SYNTAX</span></span>

### <span data-ttu-id="df963-105">GeoDRParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="df963-105">GeoDRParameterSet (Default)</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df963-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="df963-106">NamespaceInputObjectSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df963-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="df963-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df963-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="df963-108">DESCRIPTION</span></span>
<span data-ttu-id="df963-109">Das **Cmdlet "New-AzEventHubGeoDRConfiguration"** erstellt einen neuen Alias (Notfallwiederherstellungskonfiguration)</span><span class="sxs-lookup"><span data-stu-id="df963-109">The **New-AzEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="df963-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="df963-110">EXAMPLES</span></span>

### <span data-ttu-id="df963-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="df963-111">Example 1</span></span>
```
PS C:\> New-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="df963-112">Erstellt einen Alias "SampleDRConfigName" mit dem primären Namespace "SampleNamespace_Primary" mit dem sekundären Namespace "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="df963-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="df963-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df963-113">PARAMETERS</span></span>

### <span data-ttu-id="df963-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="df963-114">-AlternateName</span></span>
<span data-ttu-id="df963-115">AlternateName erforderlich, wenn der Name der Dr-Konfiguration mit dem primären Namespace identisch ist</span><span class="sxs-lookup"><span data-stu-id="df963-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

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

### <span data-ttu-id="df963-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df963-116">-AsJob</span></span>
<span data-ttu-id="df963-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="df963-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="df963-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df963-118">-DefaultProfile</span></span>
<span data-ttu-id="df963-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="df963-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df963-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df963-120">-InputObject</span></span>
<span data-ttu-id="df963-121">Namespaceobjekt</span><span class="sxs-lookup"><span data-stu-id="df963-121">Namespace Object</span></span>

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

### <span data-ttu-id="df963-122">-Name</span><span class="sxs-lookup"><span data-stu-id="df963-122">-Name</span></span>
<span data-ttu-id="df963-123">Name der DR-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="df963-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="df963-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="df963-124">-Namespace</span></span>
<span data-ttu-id="df963-125">Namespacename</span><span class="sxs-lookup"><span data-stu-id="df963-125">Namespace Name</span></span>

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

### <span data-ttu-id="df963-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="df963-126">-PartnerNamespace</span></span>
<span data-ttu-id="df963-127">DR Configuration PartnerNamespace ARM ID</span><span class="sxs-lookup"><span data-stu-id="df963-127">DR Configuration PartnerNamespace ARM ID</span></span>

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

### <span data-ttu-id="df963-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df963-128">-ResourceGroupName</span></span>
<span data-ttu-id="df963-129">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="df963-129">Resource Group Name</span></span>

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

### <span data-ttu-id="df963-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df963-130">-ResourceId</span></span>
<span data-ttu-id="df963-131">Namespaceressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="df963-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="df963-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df963-132">-Confirm</span></span>
<span data-ttu-id="df963-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="df963-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df963-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="df963-134">-WhatIf</span></span>
<span data-ttu-id="df963-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="df963-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df963-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="df963-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df963-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df963-137">CommonParameters</span></span>
<span data-ttu-id="df963-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df963-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df963-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df963-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df963-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="df963-140">INPUTS</span></span>

### <span data-ttu-id="df963-141">System.String</span><span class="sxs-lookup"><span data-stu-id="df963-141">System.String</span></span>

### <span data-ttu-id="df963-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="df963-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="df963-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="df963-143">OUTPUTS</span></span>

### <span data-ttu-id="df963-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="df963-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="df963-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="df963-145">NOTES</span></span>

## <span data-ttu-id="df963-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="df963-146">RELATED LINKS</span></span>
