---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: b90144fb94dcef874ce67168364aa65782084b4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502426"
---
# <span data-ttu-id="f0d50-101">New-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0d50-101">New-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="f0d50-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f0d50-102">SYNOPSIS</span></span>
<span data-ttu-id="f0d50-103">Erstellt einen neuen Alias (Disaster Recovery-Konfiguration)</span><span class="sxs-lookup"><span data-stu-id="f0d50-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0d50-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0d50-104">SYNTAX</span></span>

### <span data-ttu-id="f0d50-105">GeoDRPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f0d50-105">GeoDRPropertiesSet (Default)</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [[-AlternateName] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0d50-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f0d50-106">NamespaceInputObjectSet</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [[-AlternateName] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0d50-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0d50-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [[-AlternateName] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f0d50-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f0d50-108">DESCRIPTION</span></span>
<span data-ttu-id="f0d50-109">Das Cmdlet " **New-AzureRmServiceBusGeoDRConfiguration** " erstellt einen neuen Alias (Disaster Recovery-Konfiguration).</span><span class="sxs-lookup"><span data-stu-id="f0d50-109">The **New-AzureRmServiceBusGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="f0d50-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f0d50-110">EXAMPLES</span></span>

### <span data-ttu-id="f0d50-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f0d50-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName" -PartnerNamespace "/subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Secondary"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : /subscriptions/{SubscriptionId}/resourceGroups/TestignGeoDR/providers/Microsoft.ServiceBus/namespaces/SampleNamespaceSecondary
Role              : Primary
```

<span data-ttu-id="f0d50-112">Erstellt einen Alias "SampleDRCongifName" mit dem primären Namespace "SampleNamespace_Primary" mit sekundärem Namespace "SampleNamespace_Secondary".</span><span class="sxs-lookup"><span data-stu-id="f0d50-112">Creates an alias "SampleDRCongifName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="f0d50-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0d50-113">PARAMETERS</span></span>

### <span data-ttu-id="f0d50-114">-Alternatename</span><span class="sxs-lookup"><span data-stu-id="f0d50-114">-AlternateName</span></span>
<span data-ttu-id="f0d50-115">Alternativname</span><span class="sxs-lookup"><span data-stu-id="f0d50-115">AlternateName</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0d50-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0d50-116">-AsJob</span></span>
<span data-ttu-id="f0d50-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f0d50-117">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0d50-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0d50-118">-DefaultProfile</span></span>
<span data-ttu-id="f0d50-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f0d50-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0d50-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f0d50-120">-InputObject</span></span>
<span data-ttu-id="f0d50-121">Namespace-Objekt</span><span class="sxs-lookup"><span data-stu-id="f0d50-121">Namespace Object</span></span>

```yaml
Type: PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0d50-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f0d50-122">-Name</span></span>
<span data-ttu-id="f0d50-123">Dr-Konfigurations Name</span><span class="sxs-lookup"><span data-stu-id="f0d50-123">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0d50-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f0d50-124">-Namespace</span></span>
<span data-ttu-id="f0d50-125">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="f0d50-125">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0d50-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="f0d50-126">-PartnerNamespace</span></span>
<span data-ttu-id="f0d50-127">Dr-Konfigurations PartnerNamespace (Arm-ID von PartnerNamespace [sekundärer Namespace])</span><span class="sxs-lookup"><span data-stu-id="f0d50-127">DR Configuration PartnerNamespace (ARM Id of PartnerNamespace [Secondary namespace])</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0d50-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0d50-128">-ResourceGroupName</span></span>
<span data-ttu-id="f0d50-129">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="f0d50-129">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0d50-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f0d50-130">-ResourceId</span></span>
<span data-ttu-id="f0d50-131">Namespace-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="f0d50-131">Namespace Resource Id</span></span>

```yaml
Type: String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0d50-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f0d50-132">-Confirm</span></span>
<span data-ttu-id="f0d50-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f0d50-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0d50-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0d50-134">-WhatIf</span></span>
<span data-ttu-id="f0d50-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f0d50-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0d50-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0d50-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0d50-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0d50-137">CommonParameters</span></span>
<span data-ttu-id="f0d50-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0d50-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f0d50-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0d50-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0d50-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f0d50-140">INPUTS</span></span>

### <span data-ttu-id="f0d50-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f0d50-141">System.String</span></span>
<span data-ttu-id="f0d50-142">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="f0d50-142">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="f0d50-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f0d50-143">OUTPUTS</span></span>

### <span data-ttu-id="f0d50-144">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="f0d50-144">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>


## <span data-ttu-id="f0d50-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="f0d50-145">NOTES</span></span>

## <span data-ttu-id="f0d50-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f0d50-146">RELATED LINKS</span></span>
