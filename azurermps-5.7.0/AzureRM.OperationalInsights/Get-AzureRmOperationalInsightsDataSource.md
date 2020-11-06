---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 057437e55fd7877154343bdbfc5f25d216412b8e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496345"
---
# <span data-ttu-id="85683-101">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="85683-101">Get-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="85683-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="85683-102">SYNOPSIS</span></span>
<span data-ttu-id="85683-103">Abrufen von DataSources unter Azure Log Analytics-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="85683-103">Get datasources under Azure Log Analytics workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85683-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="85683-104">SYNTAX</span></span>

### <span data-ttu-id="85683-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="85683-105">ByWorkspaceName (Default)</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85683-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="85683-106">ByWorkspaceObjectByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85683-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="85683-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85683-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="85683-108">ByWorkspaceNameByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85683-109">ByWorkspaceNameByKind</span><span class="sxs-lookup"><span data-stu-id="85683-109">ByWorkspaceNameByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85683-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85683-110">DESCRIPTION</span></span>
<span data-ttu-id="85683-111">Das Cmdlet " **Get-AzureRmOperationalInsightsDataSource** " ruft Datenquellen ab.</span><span class="sxs-lookup"><span data-stu-id="85683-111">The **Get-AzureRmOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="85683-112">Sie können eine Datenquelle angeben, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="85683-112">You can specify a data source to get.</span></span>
<span data-ttu-id="85683-113">Sie können die Ergebnisse basierend auf der Art der Datenquelle filtern.</span><span class="sxs-lookup"><span data-stu-id="85683-113">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="85683-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="85683-114">EXAMPLES</span></span>

## <span data-ttu-id="85683-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="85683-115">PARAMETERS</span></span>

### <span data-ttu-id="85683-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85683-116">-DefaultProfile</span></span>
<span data-ttu-id="85683-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="85683-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85683-118">-Art</span><span class="sxs-lookup"><span data-stu-id="85683-118">-Kind</span></span>
<span data-ttu-id="85683-119">Gibt die Art der abzurufenden Datenquellen an.</span><span class="sxs-lookup"><span data-stu-id="85683-119">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="85683-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="85683-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="85683-121">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="85683-121">AzureActivityLog</span></span> 
- <span data-ttu-id="85683-122">CustomLog</span><span class="sxs-lookup"><span data-stu-id="85683-122">CustomLog</span></span> 
- <span data-ttu-id="85683-123">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="85683-123">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="85683-124">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="85683-124">LinuxSyslog</span></span> 
- <span data-ttu-id="85683-125">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="85683-125">WindowsEvent</span></span> 
- <span data-ttu-id="85683-126">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="85683-126">WindowsPerformanceCounter</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceObjectByKind
Aliases: 
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByKind
Aliases: 
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85683-127">-Name</span><span class="sxs-lookup"><span data-stu-id="85683-127">-Name</span></span>
<span data-ttu-id="85683-128">Gibt den Namen einer Datenquelle an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="85683-128">Specifies the name of a data source to get.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceObjectByName
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByName
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85683-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85683-129">-ResourceGroupName</span></span>
<span data-ttu-id="85683-130">Gibt den Namen einer Ressourcengruppe an, die Datenquellen enthält, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="85683-130">Specifies the name of a resource group that contains data sources to get.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByKind
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85683-131">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="85683-131">-Workspace</span></span>
<span data-ttu-id="85683-132">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="85683-132">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObjectByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObjectByKind
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85683-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="85683-133">-WorkspaceName</span></span>
<span data-ttu-id="85683-134">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="85683-134">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByKind
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85683-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85683-135">CommonParameters</span></span>
<span data-ttu-id="85683-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85683-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85683-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85683-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85683-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="85683-138">INPUTS</span></span>

### <span data-ttu-id="85683-139">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="85683-139">PSWorkspace</span></span>
<span data-ttu-id="85683-140">Der Parameter "Workspace" akzeptiert den Wert vom Typ "PSWorkspace" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="85683-140">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

### <span data-ttu-id="85683-141">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="85683-141">PSWorkspace</span></span>
<span data-ttu-id="85683-142">Der Parameter "Workspace" akzeptiert den Wert vom Typ "PSWorkspace" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="85683-142">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="85683-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="85683-143">OUTPUTS</span></span>

### <span data-ttu-id="85683-144">System. Collections. Generic. List ' 1 [Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource]</span><span class="sxs-lookup"><span data-stu-id="85683-144">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource]</span></span>

### <span data-ttu-id="85683-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="85683-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="85683-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="85683-146">NOTES</span></span>
* <span data-ttu-id="85683-147">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="85683-147">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="85683-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="85683-148">RELATED LINKS</span></span>

[<span data-ttu-id="85683-149">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="85683-149">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="85683-150">Satz-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="85683-150">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


