---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
ms.openlocfilehash: 338486954fe04b6497eb82bc5a11dbede1b25709
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472065"
---
# <span data-ttu-id="6a8a9-101">Get-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="6a8a9-101">Get-AzIotSecuritySolution</span></span>

## <span data-ttu-id="6a8a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a8a9-102">SYNOPSIS</span></span>
<span data-ttu-id="6a8a9-103">Holen Sie sich die Sicherheitslösung für IoT</span><span class="sxs-lookup"><span data-stu-id="6a8a9-103">Get IoT security solution</span></span>

## <span data-ttu-id="6a8a9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6a8a9-104">SYNTAX</span></span>

### <span data-ttu-id="6a8a9-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="6a8a9-105">SubscriptionScope (Default)</span></span>
```
Get-AzIotSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a8a9-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="6a8a9-106">ResourceGroupScope</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6a8a9-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="6a8a9-107">ResourceGroupLevelResource</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6a8a9-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a8a9-108">ResourceId</span></span>
```
Get-AzIotSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a8a9-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6a8a9-109">DESCRIPTION</span></span>
<span data-ttu-id="6a8a9-110">Das Get-AzIotSecuritySolution-Cmdlet gibt eine oder mehrere iot-Sicherheitslösungen zurück.</span><span class="sxs-lookup"><span data-stu-id="6a8a9-110">The Get-AzIotSecuritySolution cmdlet returns one or more iot security solutions.</span></span> <span data-ttu-id="6a8a9-111">Die Sicherheitslösung für das Internet (IoT) sammelt Sicherheitsdaten und Ereignisse von iot-Geräten und dem iot-Hub, um Bedrohungen zu verhindern und zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="6a8a9-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="6a8a9-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6a8a9-112">EXAMPLES</span></span>

### <span data-ttu-id="6a8a9-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6a8a9-113">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/IoTSecuritySolutions/MySample"
Name: "MySample"
Type: "Microsoft.Security/IoTSecuritySolutions"
Location: "centraluseuap"
DisplayName: "MySample"
status: "Enabled"
Export: ["RawEvents"]
DisabledDataSources: ["TwinData"]
Workspace: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.operationalinsights/workspaces/MyLA"
AdditionalWorkspaces: null
IotHubs: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UserDefinedResources: {
    Query: "" 
    QuerySubscriptions: []
}
RecommendationsConfiguration: [
{
    RecommendationType: "IoT_ACRAuthentication"
    Name: "Service prinicpal not used with ACR repository"
    Status: "Enabled"
}
{
    RecommendationType: "IoT_AgentSendsUnutilizedMessages"
    Name: "Agent sending underutilized messages"
    Status: "Enabled"
    }]
AutoDiscoveredResources: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UnmaskedIpLoggingStatus: "Enabled"
Tags: {}
```

<span data-ttu-id="6a8a9-114">Holen Sie sich die Lösung "MySample" in der Ressourcengruppe "MyResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="6a8a9-114">Get the solution "MySample" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="6a8a9-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6a8a9-115">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecuritySolution -ResourceGroupName "MyResourceGroup"

Array of security solution items as shown is example 1
```

<span data-ttu-id="6a8a9-116">Eine Liste aller Sicherheitslösungen in der Ressourcengruppe "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="6a8a9-116">Get list of all security solutions in resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="6a8a9-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a8a9-117">PARAMETERS</span></span>

### <span data-ttu-id="6a8a9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a8a9-118">-DefaultProfile</span></span>
<span data-ttu-id="6a8a9-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6a8a9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a8a9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6a8a9-120">-Name</span></span>
<span data-ttu-id="6a8a9-121">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="6a8a9-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a8a9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a8a9-122">-ResourceGroupName</span></span>
<span data-ttu-id="6a8a9-123">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="6a8a9-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a8a9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a8a9-124">-ResourceId</span></span>
<span data-ttu-id="6a8a9-125">DIE ID der Sicherheitsressource, für die Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="6a8a9-125">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a8a9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a8a9-126">CommonParameters</span></span>
<span data-ttu-id="6a8a9-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a8a9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a8a9-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a8a9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a8a9-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6a8a9-129">INPUTS</span></span>

### <span data-ttu-id="6a8a9-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6a8a9-130">System.String</span></span>

## <span data-ttu-id="6a8a9-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6a8a9-131">OUTPUTS</span></span>

### <span data-ttu-id="6a8a9-132">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="6a8a9-132">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="6a8a9-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6a8a9-133">NOTES</span></span>

## <span data-ttu-id="6a8a9-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6a8a9-134">RELATED LINKS</span></span>
