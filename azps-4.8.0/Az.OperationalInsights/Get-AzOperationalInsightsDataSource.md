---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
ms.openlocfilehash: 4fb6a38ff9c79a16d150402d3a2e2be135e0c004
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009021"
---
# <span data-ttu-id="6c156-101">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="6c156-101">Get-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="6c156-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6c156-102">SYNOPSIS</span></span>
<span data-ttu-id="6c156-103">Abrufen von DataSources unter Azure Log Analytics-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="6c156-103">Get datasources under Azure Log Analytics workspace.</span></span>

## <span data-ttu-id="6c156-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c156-104">SYNTAX</span></span>

### <span data-ttu-id="6c156-105">ByWorkspaceNameByKind (Standard)</span><span class="sxs-lookup"><span data-stu-id="6c156-105">ByWorkspaceNameByKind (Default)</span></span>
```
Get-AzOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c156-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="6c156-106">ByWorkspaceObjectByName</span></span>
```
Get-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c156-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="6c156-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c156-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="6c156-108">ByWorkspaceNameByName</span></span>
```
Get-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c156-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c156-109">DESCRIPTION</span></span>
<span data-ttu-id="6c156-110">Das Cmdlet " **Get-AzOperationalInsightsDataSource** " ruft Datenquellen ab.</span><span class="sxs-lookup"><span data-stu-id="6c156-110">The **Get-AzOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="6c156-111">Sie können eine Datenquelle angeben, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6c156-111">You can specify a data source to get.</span></span>
<span data-ttu-id="6c156-112">Sie können die Ergebnisse basierend auf der Art der Datenquelle filtern.</span><span class="sxs-lookup"><span data-stu-id="6c156-112">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="6c156-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6c156-113">EXAMPLES</span></span>

## <span data-ttu-id="6c156-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c156-114">PARAMETERS</span></span>

### <span data-ttu-id="6c156-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c156-115">-DefaultProfile</span></span>
<span data-ttu-id="6c156-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6c156-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c156-117">-Art</span><span class="sxs-lookup"><span data-stu-id="6c156-117">-Kind</span></span>
<span data-ttu-id="6c156-118">Gibt die Art der abzurufenden Datenquellen an.</span><span class="sxs-lookup"><span data-stu-id="6c156-118">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="6c156-119">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6c156-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6c156-120">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="6c156-120">AzureActivityLog</span></span> 
- <span data-ttu-id="6c156-121">CustomLog</span><span class="sxs-lookup"><span data-stu-id="6c156-121">CustomLog</span></span> 
- <span data-ttu-id="6c156-122">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="6c156-122">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="6c156-123">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="6c156-123">LinuxSyslog</span></span> 
- <span data-ttu-id="6c156-124">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="6c156-124">WindowsEvent</span></span> 
- <span data-ttu-id="6c156-125">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="6c156-125">WindowsPerformanceCounter</span></span>

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

### <span data-ttu-id="6c156-126">-Name</span><span class="sxs-lookup"><span data-stu-id="6c156-126">-Name</span></span>
<span data-ttu-id="6c156-127">Gibt den Namen einer Datenquelle an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6c156-127">Specifies the name of a data source to get.</span></span>

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

### <span data-ttu-id="6c156-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c156-128">-ResourceGroupName</span></span>
<span data-ttu-id="6c156-129">Gibt den Namen einer Ressourcengruppe an, die Datenquellen enthält, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6c156-129">Specifies the name of a resource group that contains data sources to get.</span></span>

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

### <span data-ttu-id="6c156-130">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="6c156-130">-Workspace</span></span>
<span data-ttu-id="6c156-131">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="6c156-131">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="6c156-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6c156-132">-WorkspaceName</span></span>
<span data-ttu-id="6c156-133">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="6c156-133">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="6c156-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c156-134">CommonParameters</span></span>
<span data-ttu-id="6c156-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c156-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c156-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c156-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c156-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6c156-137">INPUTS</span></span>

### <span data-ttu-id="6c156-138">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="6c156-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="6c156-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6c156-139">System.String</span></span>

## <span data-ttu-id="6c156-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6c156-140">OUTPUTS</span></span>

### <span data-ttu-id="6c156-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="6c156-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="6c156-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="6c156-142">NOTES</span></span>
* <span data-ttu-id="6c156-143">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="6c156-143">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="6c156-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6c156-144">RELATED LINKS</span></span>

[<span data-ttu-id="6c156-145">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="6c156-145">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="6c156-146">Satz-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="6c156-146">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


