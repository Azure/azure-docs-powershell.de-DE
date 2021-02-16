---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
ms.openlocfilehash: 4fb6a38ff9c79a16d150402d3a2e2be135e0c004
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146476"
---
# <span data-ttu-id="375dc-101">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="375dc-101">Get-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="375dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="375dc-102">SYNOPSIS</span></span>
<span data-ttu-id="375dc-103">Holen Sie sich Datenquellen im Azure Log Analytics-Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="375dc-103">Get datasources under Azure Log Analytics workspace.</span></span>

## <span data-ttu-id="375dc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="375dc-104">SYNTAX</span></span>

### <span data-ttu-id="375dc-105">ByWorkspaceNameByKind (Standard)</span><span class="sxs-lookup"><span data-stu-id="375dc-105">ByWorkspaceNameByKind (Default)</span></span>
```
Get-AzOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="375dc-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="375dc-106">ByWorkspaceObjectByName</span></span>
```
Get-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="375dc-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="375dc-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="375dc-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="375dc-108">ByWorkspaceNameByName</span></span>
```
Get-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="375dc-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="375dc-109">DESCRIPTION</span></span>
<span data-ttu-id="375dc-110">Das **Cmdlet "Get-AzOperationalInsightsDataSource"** ruft Datenquellen ab.</span><span class="sxs-lookup"><span data-stu-id="375dc-110">The **Get-AzOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="375dc-111">Sie können eine Datenquelle angeben, die Sie erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="375dc-111">You can specify a data source to get.</span></span>
<span data-ttu-id="375dc-112">Sie können die Ergebnisse nach der Art der Datenquelle filtern.</span><span class="sxs-lookup"><span data-stu-id="375dc-112">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="375dc-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="375dc-113">EXAMPLES</span></span>

## <span data-ttu-id="375dc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="375dc-114">PARAMETERS</span></span>

### <span data-ttu-id="375dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="375dc-115">-DefaultProfile</span></span>
<span data-ttu-id="375dc-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="375dc-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="375dc-117">-Kind</span><span class="sxs-lookup"><span data-stu-id="375dc-117">-Kind</span></span>
<span data-ttu-id="375dc-118">Gibt die Art der zu erhaltenden Datenquellen an.</span><span class="sxs-lookup"><span data-stu-id="375dc-118">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="375dc-119">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="375dc-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="375dc-120">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="375dc-120">AzureActivityLog</span></span> 
- <span data-ttu-id="375dc-121">CustomLog</span><span class="sxs-lookup"><span data-stu-id="375dc-121">CustomLog</span></span> 
- <span data-ttu-id="375dc-122">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="375dc-122">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="375dc-123">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="375dc-123">LinuxSyslog</span></span> 
- <span data-ttu-id="375dc-124">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="375dc-124">WindowsEvent</span></span> 
- <span data-ttu-id="375dc-125">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="375dc-125">WindowsPerformanceCounter</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, ApplicationInsights

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, ApplicationInsights

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="375dc-126">-Name</span><span class="sxs-lookup"><span data-stu-id="375dc-126">-Name</span></span>
<span data-ttu-id="375dc-127">Gibt den Namen einer datenquelle an, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="375dc-127">Specifies the name of a data source to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByName
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="375dc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="375dc-128">-ResourceGroupName</span></span>
<span data-ttu-id="375dc-129">Gibt den Namen einer Ressourcengruppe an, die zu erhaltende Datenquellen enthält.</span><span class="sxs-lookup"><span data-stu-id="375dc-129">Specifies the name of a resource group that contains data sources to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="375dc-130">-Workspace</span><span class="sxs-lookup"><span data-stu-id="375dc-130">-Workspace</span></span>
<span data-ttu-id="375dc-131">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="375dc-131">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByKind
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="375dc-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="375dc-132">-WorkspaceName</span></span>
<span data-ttu-id="375dc-133">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="375dc-133">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="375dc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="375dc-134">CommonParameters</span></span>
<span data-ttu-id="375dc-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="375dc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="375dc-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="375dc-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="375dc-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="375dc-137">INPUTS</span></span>

### <span data-ttu-id="375dc-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="375dc-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="375dc-139">System.String</span><span class="sxs-lookup"><span data-stu-id="375dc-139">System.String</span></span>

## <span data-ttu-id="375dc-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="375dc-140">OUTPUTS</span></span>

### <span data-ttu-id="375dc-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="375dc-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="375dc-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="375dc-142">NOTES</span></span>
* <span data-ttu-id="375dc-143">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, operational, insights</span><span class="sxs-lookup"><span data-stu-id="375dc-143">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="375dc-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="375dc-144">RELATED LINKS</span></span>

[<span data-ttu-id="375dc-145">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="375dc-145">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="375dc-146">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="375dc-146">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


