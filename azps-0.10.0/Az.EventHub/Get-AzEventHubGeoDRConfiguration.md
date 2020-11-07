---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 98e5a6c869fba2a49f56e3f69170602ce1d443a3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842351"
---
# <span data-ttu-id="8a39a-101">Get-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="8a39a-101">Get-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="8a39a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8a39a-102">SYNOPSIS</span></span>
<span data-ttu-id="8a39a-103">Ruft Alias (Disaster Recovery-Konfiguration) für primären oder sekundären Namespace ab</span><span class="sxs-lookup"><span data-stu-id="8a39a-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="8a39a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a39a-104">SYNTAX</span></span>

### <span data-ttu-id="8a39a-105">GeoDRParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8a39a-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a39a-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8a39a-106">NamespaceInputObjectSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a39a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a39a-107">ResourceIdParameterSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a39a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a39a-108">DESCRIPTION</span></span>
<span data-ttu-id="8a39a-109">Der **Get-AzEventHubGeoDRConfiguration** ruft Alias (Disaster Recovery-Konfiguration) für primären oder sekundären Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="8a39a-109">The **Get-AzEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="8a39a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8a39a-110">EXAMPLES</span></span>

### <span data-ttu-id="8a39a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8a39a-111">Example 1</span></span>
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

<span data-ttu-id="8a39a-112">Ruft Alias "SampleDRConfigName"-Konfiguration für den primären Namespace "SampleNamespace_Primary" ab</span><span class="sxs-lookup"><span data-stu-id="8a39a-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="8a39a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a39a-113">PARAMETERS</span></span>

### <span data-ttu-id="8a39a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a39a-114">-DefaultProfile</span></span>
<span data-ttu-id="8a39a-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8a39a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a39a-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8a39a-116">-InputObject</span></span>
<span data-ttu-id="8a39a-117">Namespace-Objekt</span><span class="sxs-lookup"><span data-stu-id="8a39a-117">Namespace Object</span></span>

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

### <span data-ttu-id="8a39a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8a39a-118">-Name</span></span>
<span data-ttu-id="8a39a-119">Dr-Konfigurations Name</span><span class="sxs-lookup"><span data-stu-id="8a39a-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="8a39a-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8a39a-120">-Namespace</span></span>
<span data-ttu-id="8a39a-121">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="8a39a-121">Namespace Name</span></span>

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

### <span data-ttu-id="8a39a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a39a-122">-ResourceGroupName</span></span>
<span data-ttu-id="8a39a-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="8a39a-123">Resource Group Name</span></span>

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

### <span data-ttu-id="8a39a-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8a39a-124">-ResourceId</span></span>
<span data-ttu-id="8a39a-125">Namespace-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="8a39a-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="8a39a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a39a-126">CommonParameters</span></span>
<span data-ttu-id="8a39a-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a39a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a39a-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a39a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a39a-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8a39a-129">INPUTS</span></span>

### <span data-ttu-id="8a39a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8a39a-130">System.String</span></span>

### <span data-ttu-id="8a39a-131">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="8a39a-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="8a39a-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8a39a-132">OUTPUTS</span></span>

### <span data-ttu-id="8a39a-133">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="8a39a-133">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="8a39a-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="8a39a-134">NOTES</span></span>

## <span data-ttu-id="8a39a-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8a39a-135">RELATED LINKS</span></span>
