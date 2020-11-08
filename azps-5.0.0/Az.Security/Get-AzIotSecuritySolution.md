---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
ms.openlocfilehash: 338486954fe04b6497eb82bc5a11dbede1b25709
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179674"
---
# <span data-ttu-id="60a6d-101">Get-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="60a6d-101">Get-AzIotSecuritySolution</span></span>

## <span data-ttu-id="60a6d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="60a6d-102">SYNOPSIS</span></span>
<span data-ttu-id="60a6d-103">Sicherheitslösung für Sie</span><span class="sxs-lookup"><span data-stu-id="60a6d-103">Get IoT security solution</span></span>

## <span data-ttu-id="60a6d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="60a6d-104">SYNTAX</span></span>

### <span data-ttu-id="60a6d-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="60a6d-105">SubscriptionScope (Default)</span></span>
```
Get-AzIotSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60a6d-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="60a6d-106">ResourceGroupScope</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="60a6d-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="60a6d-107">ResourceGroupLevelResource</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="60a6d-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="60a6d-108">ResourceId</span></span>
```
Get-AzIotSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60a6d-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60a6d-109">DESCRIPTION</span></span>
<span data-ttu-id="60a6d-110">Das Get-AzIotSecuritySolution-Cmdlet gibt eine oder mehrere Sicherheitslösungen zurück.</span><span class="sxs-lookup"><span data-stu-id="60a6d-110">The Get-AzIotSecuritySolution cmdlet returns one or more iot security solutions.</span></span> <span data-ttu-id="60a6d-111">Die Sicherheitslösung "viel" sammelt Sicherheitsdaten und Ereignisse von viel-Geräten und viel Hub, um Bedrohungen zu verhindern und zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="60a6d-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="60a6d-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="60a6d-112">EXAMPLES</span></span>

### <span data-ttu-id="60a6d-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="60a6d-113">Example 1</span></span>
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

<span data-ttu-id="60a6d-114">Abrufen der Lösung "MySample" in der Ressourcengruppe "myresourcegroup"</span><span class="sxs-lookup"><span data-stu-id="60a6d-114">Get the solution "MySample" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="60a6d-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="60a6d-115">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecuritySolution -ResourceGroupName "MyResourceGroup"

Array of security solution items as shown is example 1
```

<span data-ttu-id="60a6d-116">Abrufen einer Liste aller Sicherheitslösungen in der Ressourcengruppe "myresourcegroup"</span><span class="sxs-lookup"><span data-stu-id="60a6d-116">Get list of all security solutions in resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="60a6d-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="60a6d-117">PARAMETERS</span></span>

### <span data-ttu-id="60a6d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60a6d-118">-DefaultProfile</span></span>
<span data-ttu-id="60a6d-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="60a6d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60a6d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="60a6d-120">-Name</span></span>
<span data-ttu-id="60a6d-121">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="60a6d-121">Resource name.</span></span>

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

### <span data-ttu-id="60a6d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60a6d-122">-ResourceGroupName</span></span>
<span data-ttu-id="60a6d-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="60a6d-123">Resource group name.</span></span>

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

### <span data-ttu-id="60a6d-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="60a6d-124">-ResourceId</span></span>
<span data-ttu-id="60a6d-125">Die ID der Sicherheitsressource, auf der Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="60a6d-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="60a6d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60a6d-126">CommonParameters</span></span>
<span data-ttu-id="60a6d-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60a6d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60a6d-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60a6d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60a6d-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="60a6d-129">INPUTS</span></span>

### <span data-ttu-id="60a6d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="60a6d-130">System.String</span></span>

## <span data-ttu-id="60a6d-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="60a6d-131">OUTPUTS</span></span>

### <span data-ttu-id="60a6d-132">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="60a6d-132">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="60a6d-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="60a6d-133">NOTES</span></span>

## <span data-ttu-id="60a6d-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="60a6d-134">RELATED LINKS</span></span>
