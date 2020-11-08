---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: fe0d8f29650498e895e19e18bcb080107b2dbf35
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996129"
---
# <span data-ttu-id="55952-101">New-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="55952-101">New-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="55952-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="55952-102">SYNOPSIS</span></span>
<span data-ttu-id="55952-103">Erstellt einen neuen Alias (Disaster Recovery-Konfiguration)</span><span class="sxs-lookup"><span data-stu-id="55952-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="55952-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="55952-104">SYNTAX</span></span>

### <span data-ttu-id="55952-105">GeoDRParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="55952-105">GeoDRParameterSet (Default)</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55952-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="55952-106">NamespaceInputObjectSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55952-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="55952-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="55952-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="55952-108">DESCRIPTION</span></span>
<span data-ttu-id="55952-109">Das Cmdlet " **New-AzEventHubGeoDRConfiguration** " erstellt einen neuen Alias (Disaster Recovery-Konfiguration).</span><span class="sxs-lookup"><span data-stu-id="55952-109">The **New-AzEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="55952-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="55952-110">EXAMPLES</span></span>

### <span data-ttu-id="55952-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="55952-111">Example 1</span></span>
```
PS C:\> New-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="55952-112">Erstellt einen Alias "SampleDRConfigName" mit dem primären Namespace "SampleNamespace_Primary" mit sekundärem Namespace "SampleNamespace_Secondary".</span><span class="sxs-lookup"><span data-stu-id="55952-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="55952-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="55952-113">PARAMETERS</span></span>

### <span data-ttu-id="55952-114">-Alternatename</span><span class="sxs-lookup"><span data-stu-id="55952-114">-AlternateName</span></span>
<span data-ttu-id="55952-115">Alternatename ist erforderlich, wenn der Dr-Konfigurationsname mit dem primären Namespace identisch ist.</span><span class="sxs-lookup"><span data-stu-id="55952-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

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

### <span data-ttu-id="55952-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55952-116">-AsJob</span></span>
<span data-ttu-id="55952-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="55952-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55952-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55952-118">-DefaultProfile</span></span>
<span data-ttu-id="55952-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="55952-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55952-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="55952-120">-InputObject</span></span>
<span data-ttu-id="55952-121">Namespace-Objekt</span><span class="sxs-lookup"><span data-stu-id="55952-121">Namespace Object</span></span>

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

### <span data-ttu-id="55952-122">-Name</span><span class="sxs-lookup"><span data-stu-id="55952-122">-Name</span></span>
<span data-ttu-id="55952-123">Dr-Konfigurations Name</span><span class="sxs-lookup"><span data-stu-id="55952-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="55952-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="55952-124">-Namespace</span></span>
<span data-ttu-id="55952-125">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="55952-125">Namespace Name</span></span>

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

### <span data-ttu-id="55952-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="55952-126">-PartnerNamespace</span></span>
<span data-ttu-id="55952-127">Dr-Konfigurations PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="55952-127">DR Configuration PartnerNamespace</span></span>

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

### <span data-ttu-id="55952-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55952-128">-ResourceGroupName</span></span>
<span data-ttu-id="55952-129">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="55952-129">Resource Group Name</span></span>

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

### <span data-ttu-id="55952-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="55952-130">-ResourceId</span></span>
<span data-ttu-id="55952-131">Namespace-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="55952-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="55952-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="55952-132">-Confirm</span></span>
<span data-ttu-id="55952-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="55952-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55952-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55952-134">-WhatIf</span></span>
<span data-ttu-id="55952-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="55952-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55952-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="55952-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55952-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55952-137">CommonParameters</span></span>
<span data-ttu-id="55952-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55952-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55952-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55952-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55952-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="55952-140">INPUTS</span></span>

### <span data-ttu-id="55952-141">System. String</span><span class="sxs-lookup"><span data-stu-id="55952-141">System.String</span></span>

### <span data-ttu-id="55952-142">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="55952-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="55952-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="55952-143">OUTPUTS</span></span>

### <span data-ttu-id="55952-144">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="55952-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="55952-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="55952-145">NOTES</span></span>

## <span data-ttu-id="55952-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="55952-146">RELATED LINKS</span></span>
