---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 21ccb8a16ff3622e6661bd5548721d6d1227e7e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942208"
---
# <span data-ttu-id="bd321-101">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd321-101">Get-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="bd321-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd321-102">SYNOPSIS</span></span>
<span data-ttu-id="bd321-103">Ruft Alias(Notfallwiederherstellungskonfiguration) für primären oder sekundären Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="bd321-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="bd321-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bd321-104">SYNTAX</span></span>

### <span data-ttu-id="bd321-105">GeoDRPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bd321-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd321-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bd321-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd321-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd321-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd321-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bd321-108">DESCRIPTION</span></span>
<span data-ttu-id="bd321-109">Die **Get-AzServiceBusGeoDRConfiguration** ruft Alias(Disaster Recovery-Konfiguration) für primären oder sekundären Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="bd321-109">The **Get-AzServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="bd321-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bd321-110">EXAMPLES</span></span>

### <span data-ttu-id="bd321-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bd321-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="bd321-112">Ruft die Aliaskonfiguration "SampleDRConfigName" für den primären Namespace "SampleNamespace_Primary" ab.</span><span class="sxs-lookup"><span data-stu-id="bd321-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="bd321-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bd321-113">PARAMETERS</span></span>

### <span data-ttu-id="bd321-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd321-114">-DefaultProfile</span></span>
<span data-ttu-id="bd321-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bd321-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd321-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd321-116">-InputObject</span></span>
<span data-ttu-id="bd321-117">Namespaceobjekt</span><span class="sxs-lookup"><span data-stu-id="bd321-117">Namespace Object</span></span>

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

### <span data-ttu-id="bd321-118">-Name</span><span class="sxs-lookup"><span data-stu-id="bd321-118">-Name</span></span>
<span data-ttu-id="bd321-119">NAME der DR-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="bd321-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="bd321-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bd321-120">-Namespace</span></span>
<span data-ttu-id="bd321-121">Namespacename</span><span class="sxs-lookup"><span data-stu-id="bd321-121">Namespace Name</span></span>

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

### <span data-ttu-id="bd321-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd321-122">-ResourceGroupName</span></span>
<span data-ttu-id="bd321-123">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="bd321-123">Resource Group Name</span></span>

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

### <span data-ttu-id="bd321-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd321-124">-ResourceId</span></span>
<span data-ttu-id="bd321-125">Namespaceressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="bd321-125">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd321-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd321-126">CommonParameters</span></span>
<span data-ttu-id="bd321-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd321-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd321-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd321-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd321-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bd321-129">INPUTS</span></span>

### <span data-ttu-id="bd321-130">System.String</span><span class="sxs-lookup"><span data-stu-id="bd321-130">System.String</span></span>

### <span data-ttu-id="bd321-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="bd321-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="bd321-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bd321-132">OUTPUTS</span></span>

### <span data-ttu-id="bd321-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="bd321-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="bd321-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bd321-134">NOTES</span></span>

## <span data-ttu-id="bd321-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bd321-135">RELATED LINKS</span></span>
