---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: a4cb60c224c440654854cff66434be1d224e8d50
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661054"
---
# <span data-ttu-id="d86d1-101">Get-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="d86d1-101">Get-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="d86d1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d86d1-102">SYNOPSIS</span></span>
<span data-ttu-id="d86d1-103">Ruft Alias (Disaster Recovery-Konfiguration) für primären oder sekundären Namespace ab</span><span class="sxs-lookup"><span data-stu-id="d86d1-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="d86d1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d86d1-104">SYNTAX</span></span>

### <span data-ttu-id="d86d1-105">GeoDRParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d86d1-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d86d1-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d86d1-106">NamespaceInputObjectSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d86d1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d86d1-107">ResourceIdParameterSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d86d1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d86d1-108">DESCRIPTION</span></span>
<span data-ttu-id="d86d1-109">Der **Get-AzEventHubGeoDRConfiguration** ruft Alias (Disaster Recovery-Konfiguration) für primären oder sekundären Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="d86d1-109">The **Get-AzEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="d86d1-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d86d1-110">EXAMPLES</span></span>

### <span data-ttu-id="d86d1-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d86d1-111">Example 1</span></span>
```
PS C:\> Get-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
AlternateName     :
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="d86d1-112">Ruft Alias "SampleDRCongifName"-Konfiguration für den primären Namespace "SampleNamespace_Primary" ab</span><span class="sxs-lookup"><span data-stu-id="d86d1-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="d86d1-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d86d1-113">PARAMETERS</span></span>

### <span data-ttu-id="d86d1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d86d1-114">-DefaultProfile</span></span>
<span data-ttu-id="d86d1-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d86d1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d86d1-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d86d1-116">-InputObject</span></span>
<span data-ttu-id="d86d1-117">Namespace-Objekt</span><span class="sxs-lookup"><span data-stu-id="d86d1-117">Namespace Object</span></span>

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

### <span data-ttu-id="d86d1-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d86d1-118">-Name</span></span>
<span data-ttu-id="d86d1-119">Dr-Konfigurations Name</span><span class="sxs-lookup"><span data-stu-id="d86d1-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="d86d1-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d86d1-120">-Namespace</span></span>
<span data-ttu-id="d86d1-121">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="d86d1-121">Namespace Name</span></span>

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

### <span data-ttu-id="d86d1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d86d1-122">-ResourceGroupName</span></span>
<span data-ttu-id="d86d1-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="d86d1-123">Resource Group Name</span></span>

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

### <span data-ttu-id="d86d1-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d86d1-124">-ResourceId</span></span>
<span data-ttu-id="d86d1-125">Namespace-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="d86d1-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="d86d1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d86d1-126">CommonParameters</span></span>
<span data-ttu-id="d86d1-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d86d1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d86d1-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d86d1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d86d1-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d86d1-129">INPUTS</span></span>

### <span data-ttu-id="d86d1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d86d1-130">System.String</span></span>

### <span data-ttu-id="d86d1-131">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="d86d1-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="d86d1-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d86d1-132">OUTPUTS</span></span>

### <span data-ttu-id="d86d1-133">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="d86d1-133">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="d86d1-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="d86d1-134">NOTES</span></span>

## <span data-ttu-id="d86d1-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d86d1-135">RELATED LINKS</span></span>
