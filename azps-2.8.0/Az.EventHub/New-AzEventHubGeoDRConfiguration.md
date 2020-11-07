---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: cb1f3ba75b05fcd6950a8cb9bcff9fe899aaf471
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651180"
---
# <span data-ttu-id="a82fe-101">New-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="a82fe-101">New-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="a82fe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a82fe-102">SYNOPSIS</span></span>
<span data-ttu-id="a82fe-103">Erstellt einen neuen Alias (Disaster Recovery-Konfiguration)</span><span class="sxs-lookup"><span data-stu-id="a82fe-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="a82fe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a82fe-104">SYNTAX</span></span>

### <span data-ttu-id="a82fe-105">GeoDRParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a82fe-105">GeoDRParameterSet (Default)</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a82fe-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a82fe-106">NamespaceInputObjectSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a82fe-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a82fe-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a82fe-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a82fe-108">DESCRIPTION</span></span>
<span data-ttu-id="a82fe-109">Das Cmdlet " **New-AzEventHubGeoDRConfiguration** " erstellt einen neuen Alias (Disaster Recovery-Konfiguration).</span><span class="sxs-lookup"><span data-stu-id="a82fe-109">The **New-AzEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="a82fe-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a82fe-110">EXAMPLES</span></span>

### <span data-ttu-id="a82fe-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a82fe-111">Example 1</span></span>
```
PS C:\> New-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="a82fe-112">Erstellt einen Alias "SampleDRConfigName" mit dem primären Namespace "SampleNamespace_Primary" mit sekundärem Namespace "SampleNamespace_Secondary".</span><span class="sxs-lookup"><span data-stu-id="a82fe-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="a82fe-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a82fe-113">PARAMETERS</span></span>

### <span data-ttu-id="a82fe-114">-Alternatename</span><span class="sxs-lookup"><span data-stu-id="a82fe-114">-AlternateName</span></span>
<span data-ttu-id="a82fe-115">Alternatename ist erforderlich, wenn der Dr-Konfigurationsname mit dem primären Namespace identisch ist.</span><span class="sxs-lookup"><span data-stu-id="a82fe-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

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

### <span data-ttu-id="a82fe-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a82fe-116">-AsJob</span></span>
<span data-ttu-id="a82fe-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a82fe-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a82fe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a82fe-118">-DefaultProfile</span></span>
<span data-ttu-id="a82fe-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a82fe-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a82fe-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a82fe-120">-InputObject</span></span>
<span data-ttu-id="a82fe-121">Namespace-Objekt</span><span class="sxs-lookup"><span data-stu-id="a82fe-121">Namespace Object</span></span>

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

### <span data-ttu-id="a82fe-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a82fe-122">-Name</span></span>
<span data-ttu-id="a82fe-123">Dr-Konfigurations Name</span><span class="sxs-lookup"><span data-stu-id="a82fe-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="a82fe-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a82fe-124">-Namespace</span></span>
<span data-ttu-id="a82fe-125">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="a82fe-125">Namespace Name</span></span>

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

### <span data-ttu-id="a82fe-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="a82fe-126">-PartnerNamespace</span></span>
<span data-ttu-id="a82fe-127">Dr-Konfigurations PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="a82fe-127">DR Configuration PartnerNamespace</span></span>

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

### <span data-ttu-id="a82fe-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a82fe-128">-ResourceGroupName</span></span>
<span data-ttu-id="a82fe-129">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="a82fe-129">Resource Group Name</span></span>

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

### <span data-ttu-id="a82fe-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a82fe-130">-ResourceId</span></span>
<span data-ttu-id="a82fe-131">Namespace-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="a82fe-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="a82fe-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a82fe-132">-Confirm</span></span>
<span data-ttu-id="a82fe-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a82fe-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a82fe-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a82fe-134">-WhatIf</span></span>
<span data-ttu-id="a82fe-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a82fe-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a82fe-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a82fe-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a82fe-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a82fe-137">CommonParameters</span></span>
<span data-ttu-id="a82fe-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a82fe-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a82fe-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a82fe-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a82fe-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a82fe-140">INPUTS</span></span>

### <span data-ttu-id="a82fe-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a82fe-141">System.String</span></span>

### <span data-ttu-id="a82fe-142">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="a82fe-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="a82fe-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a82fe-143">OUTPUTS</span></span>

### <span data-ttu-id="a82fe-144">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="a82fe-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="a82fe-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="a82fe-145">NOTES</span></span>

## <span data-ttu-id="a82fe-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a82fe-146">RELATED LINKS</span></span>
