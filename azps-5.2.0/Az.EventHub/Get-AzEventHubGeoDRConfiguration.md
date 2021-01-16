---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 2e324524319a2eacd24bc08aa727892ef08928c0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98289973"
---
# <span data-ttu-id="f52b4-101">Get-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="f52b4-101">Get-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="f52b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f52b4-102">SYNOPSIS</span></span>
<span data-ttu-id="f52b4-103">Ruft "Alias(Notfallwiederherstellungskonfiguration)" für den primären oder sekundären Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="f52b4-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="f52b4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f52b4-104">SYNTAX</span></span>

### <span data-ttu-id="f52b4-105">GeoDRParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f52b4-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f52b4-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f52b4-106">NamespaceInputObjectSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f52b4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f52b4-107">ResourceIdParameterSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f52b4-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f52b4-108">DESCRIPTION</span></span>
<span data-ttu-id="f52b4-109">Die **Get-AzEventHubGeoDRConfiguration** ruft "Alias(Notfallwiederherstellungskonfiguration)" für den primären oder sekundären Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="f52b4-109">The **Get-AzEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="f52b4-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f52b4-110">EXAMPLES</span></span>

### <span data-ttu-id="f52b4-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f52b4-111">Example 1</span></span>
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

<span data-ttu-id="f52b4-112">Ruft die Aliaskonfiguration "SampleDRConfigName" für den primären Namespace "SampleNamespace_Primary" ab.</span><span class="sxs-lookup"><span data-stu-id="f52b4-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="f52b4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f52b4-113">PARAMETERS</span></span>

### <span data-ttu-id="f52b4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f52b4-114">-DefaultProfile</span></span>
<span data-ttu-id="f52b4-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f52b4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f52b4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f52b4-116">-InputObject</span></span>
<span data-ttu-id="f52b4-117">Namespaceobjekt</span><span class="sxs-lookup"><span data-stu-id="f52b4-117">Namespace Object</span></span>

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

### <span data-ttu-id="f52b4-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f52b4-118">-Name</span></span>
<span data-ttu-id="f52b4-119">Name der DR-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="f52b4-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="f52b4-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f52b4-120">-Namespace</span></span>
<span data-ttu-id="f52b4-121">Namespacename</span><span class="sxs-lookup"><span data-stu-id="f52b4-121">Namespace Name</span></span>

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

### <span data-ttu-id="f52b4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f52b4-122">-ResourceGroupName</span></span>
<span data-ttu-id="f52b4-123">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="f52b4-123">Resource Group Name</span></span>

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

### <span data-ttu-id="f52b4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f52b4-124">-ResourceId</span></span>
<span data-ttu-id="f52b4-125">Namespaceressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="f52b4-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="f52b4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f52b4-126">CommonParameters</span></span>
<span data-ttu-id="f52b4-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f52b4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f52b4-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f52b4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f52b4-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f52b4-129">INPUTS</span></span>

### <span data-ttu-id="f52b4-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f52b4-130">System.String</span></span>

### <span data-ttu-id="f52b4-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="f52b4-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="f52b4-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f52b4-132">OUTPUTS</span></span>

### <span data-ttu-id="f52b4-133">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="f52b4-133">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="f52b4-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f52b4-134">NOTES</span></span>

## <span data-ttu-id="f52b4-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f52b4-135">RELATED LINKS</span></span>
