---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 0a94460105f680efffff36af54bec9936dd0813c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844156"
---
# <span data-ttu-id="572ab-101">Get-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="572ab-101">Get-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="572ab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="572ab-102">SYNOPSIS</span></span>
<span data-ttu-id="572ab-103">Ruft die Informationen zu den Bandbreiten Terminplänen ab</span><span class="sxs-lookup"><span data-stu-id="572ab-103">Gets the information about the Bandwidth schedules</span></span>

## <span data-ttu-id="572ab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="572ab-104">SYNTAX</span></span>

### <span data-ttu-id="572ab-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="572ab-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="572ab-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="572ab-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="572ab-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="572ab-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="572ab-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="572ab-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="572ab-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="572ab-109">DESCRIPTION</span></span>
<span data-ttu-id="572ab-110">Das Cmdlet " **Get-AzDataBoxEdgeBandwidthSchedule** " Ruft die Informationen zu den Bandbreiten Zeitplänen ab.</span><span class="sxs-lookup"><span data-stu-id="572ab-110">The **Get-AzDataBoxEdgeBandwidthSchedule** cmdlet gets the information about the Bandwidth Schedules.</span></span> <span data-ttu-id="572ab-111">Sie können den Namen eines Zeitplans zusammen mit dem Namen der Ressourcengruppe und dem Gerätenamen angeben, um die Informationen zu einem bestimmten Bandbreiten Zeitplan abzurufen.</span><span class="sxs-lookup"><span data-stu-id="572ab-111">You can specify the Name of a Schedule along with the Resource Group name and Device name to get the information about a specific Bandwidth schedule</span></span>

## <span data-ttu-id="572ab-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="572ab-112">EXAMPLES</span></span>

### <span data-ttu-id="572ab-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="572ab-113">Example 1</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name

Name              DaysOfWeek         RateInMbps StartTime StopTime
----              ----------         ---------- --------- --------
schedule-name     Sunday,Saturday    unlimited  13:00:00  14:00:00
Schedule-1        Tuesday,Friday     unlimited  00:00:00  23:59:00
Schedule-2        Thursday           50         00:01:00  05:00:00
```

### <span data-ttu-id="572ab-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="572ab-114">Example 2</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name -Name Schedule-1

Name              DaysOfWeek      RateInMbps StartTime StopTime
----              ----------      ---------- --------- --------
Schedule-1        Sunday,Saturday unlimited  13:00:00  14:00:00
```

## <span data-ttu-id="572ab-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="572ab-115">PARAMETERS</span></span>

### <span data-ttu-id="572ab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="572ab-116">-DefaultProfile</span></span>
<span data-ttu-id="572ab-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="572ab-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="572ab-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="572ab-118">-DeviceName</span></span>
<span data-ttu-id="572ab-119">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="572ab-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="572ab-120">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="572ab-120">-DeviceObject</span></span>
<span data-ttu-id="572ab-121">Bitte geben Sie das entsprechende Device-Objekt an</span><span class="sxs-lookup"><span data-stu-id="572ab-121">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="572ab-122">-Name</span><span class="sxs-lookup"><span data-stu-id="572ab-122">-Name</span></span>
<span data-ttu-id="572ab-123">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="572ab-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="572ab-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="572ab-124">-ResourceGroupName</span></span>
<span data-ttu-id="572ab-125">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="572ab-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="572ab-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="572ab-126">-ResourceId</span></span>
<span data-ttu-id="572ab-127">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="572ab-127">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="572ab-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="572ab-128">CommonParameters</span></span>
<span data-ttu-id="572ab-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="572ab-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="572ab-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="572ab-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="572ab-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="572ab-131">INPUTS</span></span>

### <span data-ttu-id="572ab-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="572ab-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="572ab-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="572ab-133">OUTPUTS</span></span>

### <span data-ttu-id="572ab-134">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="572ab-134">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="572ab-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="572ab-135">NOTES</span></span>

## <span data-ttu-id="572ab-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="572ab-136">RELATED LINKS</span></span>
