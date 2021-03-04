---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: b2003821178875777240cb43bcdc1e9e53784fc4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921240"
---
# <span data-ttu-id="622f7-101">Get-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="622f7-101">Get-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="622f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="622f7-102">SYNOPSIS</span></span>
<span data-ttu-id="622f7-103">Ruft Alias(Notfallwiederherstellungskonfiguration) für primären oder sekundären Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="622f7-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="622f7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="622f7-104">SYNTAX</span></span>

### <span data-ttu-id="622f7-105">GeoDRParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="622f7-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="622f7-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="622f7-106">NamespaceInputObjectSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="622f7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="622f7-107">ResourceIdParameterSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="622f7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="622f7-108">DESCRIPTION</span></span>
<span data-ttu-id="622f7-109">Die **Get-AzEventHubGeoDRConfiguration** Ruft Alias(Disaster Recovery-Konfiguration) für primären oder sekundären Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="622f7-109">The **Get-AzEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="622f7-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="622f7-110">EXAMPLES</span></span>

### <span data-ttu-id="622f7-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="622f7-111">Example 1</span></span>
```
PS C:\> Get-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
AlternateName     :
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="622f7-112">Ruft die Aliaskonfiguration "SampleDRConfigName" für den primären Namespace "SampleNamespace_Primary" ab.</span><span class="sxs-lookup"><span data-stu-id="622f7-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="622f7-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="622f7-113">PARAMETERS</span></span>

### <span data-ttu-id="622f7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="622f7-114">-DefaultProfile</span></span>
<span data-ttu-id="622f7-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="622f7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="622f7-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="622f7-116">-InputObject</span></span>
<span data-ttu-id="622f7-117">Namespaceobjekt</span><span class="sxs-lookup"><span data-stu-id="622f7-117">Namespace Object</span></span>

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

### <span data-ttu-id="622f7-118">-Name</span><span class="sxs-lookup"><span data-stu-id="622f7-118">-Name</span></span>
<span data-ttu-id="622f7-119">NAME der DR-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="622f7-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="622f7-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="622f7-120">-Namespace</span></span>
<span data-ttu-id="622f7-121">Namespacename</span><span class="sxs-lookup"><span data-stu-id="622f7-121">Namespace Name</span></span>

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

### <span data-ttu-id="622f7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="622f7-122">-ResourceGroupName</span></span>
<span data-ttu-id="622f7-123">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="622f7-123">Resource Group Name</span></span>

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

### <span data-ttu-id="622f7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="622f7-124">-ResourceId</span></span>
<span data-ttu-id="622f7-125">Namespaceressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="622f7-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="622f7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="622f7-126">CommonParameters</span></span>
<span data-ttu-id="622f7-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="622f7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="622f7-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="622f7-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="622f7-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="622f7-129">INPUTS</span></span>

### <span data-ttu-id="622f7-130">System.String</span><span class="sxs-lookup"><span data-stu-id="622f7-130">System.String</span></span>

### <span data-ttu-id="622f7-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="622f7-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="622f7-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="622f7-132">OUTPUTS</span></span>

### <span data-ttu-id="622f7-133">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="622f7-133">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="622f7-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="622f7-134">NOTES</span></span>

## <span data-ttu-id="622f7-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="622f7-135">RELATED LINKS</span></span>
