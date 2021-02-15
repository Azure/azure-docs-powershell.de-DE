---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 5a2f3a3310675324fde3ff262cf88325224193c6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174113"
---
# <span data-ttu-id="ddb5b-101">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="ddb5b-101">Get-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="ddb5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddb5b-102">SYNOPSIS</span></span>
<span data-ttu-id="ddb5b-103">Ruft "Alias(Notfallwiederherstellungskonfiguration)" für den primären oder sekundären Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="ddb5b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ddb5b-104">SYNTAX</span></span>

### <span data-ttu-id="ddb5b-105">GeoDRPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ddb5b-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ddb5b-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ddb5b-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ddb5b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddb5b-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddb5b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ddb5b-108">DESCRIPTION</span></span>
<span data-ttu-id="ddb5b-109">Die **Get-AzServiceBusGeoDRConfiguration** ruft "Alias(Notfallwiederherstellungskonfiguration)" für den primären oder sekundären Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-109">The **Get-AzServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="ddb5b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ddb5b-110">EXAMPLES</span></span>

### <span data-ttu-id="ddb5b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ddb5b-111">Example 1</span></span>
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

<span data-ttu-id="ddb5b-112">Ruft die Aliaskonfiguration "SampleDRConfigName" für den primären Namespace "SampleNamespace_Primary" ab.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="ddb5b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddb5b-113">PARAMETERS</span></span>

### <span data-ttu-id="ddb5b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddb5b-114">-DefaultProfile</span></span>
<span data-ttu-id="ddb5b-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddb5b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddb5b-116">-InputObject</span></span>
<span data-ttu-id="ddb5b-117">Namespaceobjekt</span><span class="sxs-lookup"><span data-stu-id="ddb5b-117">Namespace Object</span></span>

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

### <span data-ttu-id="ddb5b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ddb5b-118">-Name</span></span>
<span data-ttu-id="ddb5b-119">Name der DR-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="ddb5b-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="ddb5b-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ddb5b-120">-Namespace</span></span>
<span data-ttu-id="ddb5b-121">Namespacename</span><span class="sxs-lookup"><span data-stu-id="ddb5b-121">Namespace Name</span></span>

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

### <span data-ttu-id="ddb5b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddb5b-122">-ResourceGroupName</span></span>
<span data-ttu-id="ddb5b-123">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="ddb5b-123">Resource Group Name</span></span>

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

### <span data-ttu-id="ddb5b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ddb5b-124">-ResourceId</span></span>
<span data-ttu-id="ddb5b-125">Namespaceressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="ddb5b-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="ddb5b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddb5b-126">CommonParameters</span></span>
<span data-ttu-id="ddb5b-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddb5b-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddb5b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddb5b-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ddb5b-129">INPUTS</span></span>

### <span data-ttu-id="ddb5b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ddb5b-130">System.String</span></span>

### <span data-ttu-id="ddb5b-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="ddb5b-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="ddb5b-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ddb5b-132">OUTPUTS</span></span>

### <span data-ttu-id="ddb5b-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="ddb5b-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="ddb5b-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ddb5b-134">NOTES</span></span>

## <span data-ttu-id="ddb5b-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ddb5b-135">RELATED LINKS</span></span>
