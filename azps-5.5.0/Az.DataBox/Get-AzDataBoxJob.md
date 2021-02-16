---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/get-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
ms.openlocfilehash: 8669ee676f3f2be1f1a0064ed9fbbe88f3d113ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144404"
---
# <span data-ttu-id="22223-101">Get-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="22223-101">Get-AzDataBoxJob</span></span>

## <span data-ttu-id="22223-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22223-102">SYNOPSIS</span></span>
<span data-ttu-id="22223-103">Ruft Informationen zu Databox-Aufträgen ab.</span><span class="sxs-lookup"><span data-stu-id="22223-103">Gets information about Databox Jobs</span></span>

## <span data-ttu-id="22223-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22223-104">SYNTAX</span></span>

### <span data-ttu-id="22223-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="22223-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxJob [-ResourceGroupName <String>] [-Completed] [-CompletedWithError] [-Cancelled] [-Aborted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22223-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="22223-106">GetByNameParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="22223-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22223-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22223-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="22223-108">DESCRIPTION</span></span>
<span data-ttu-id="22223-109">Das **Cmdlet "Get-AzDataBoxJobs"** ruft Informationen zu Databoxaufträgen in einem Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="22223-109">The **Get-AzDataBoxJobs** cmdlet gets information about databox jobs in an Azure subscription.</span></span>
<span data-ttu-id="22223-110">Wenn Sie die Ressourcengruppe angeben, ruft dieses Cmdlet alle Databoxaufträge unter dieser Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="22223-110">If you specify the Resource Group, this cmdlet gets all the databox jobs under that resource group.</span></span> <span data-ttu-id="22223-111">Wenn Sie den Namen des Auftrags zusammen mit dem Namen der Ressourcengruppe angeben, ruft dieses Cmdlet Informationen zu diesem bestimmten Datenfeldauftrag ab.</span><span class="sxs-lookup"><span data-stu-id="22223-111">If you specify the Name of the job along with the resource group name, this cmdlet gets information about that specific databox job.</span></span>
<span data-ttu-id="22223-112">Wenn Sie nichts anderes als die Abonnement-ID angeben, ruft dieses Cmdlet Informationen zu allen Databoxaufträgen unter diesem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="22223-112">If you do not specify anything other than subscription id, this cmdlet gets information about all of the databox jobs under that subscription.</span></span>

## <span data-ttu-id="22223-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="22223-113">EXAMPLES</span></span>

### <span data-ttu-id="22223-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="22223-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxJob

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1
cleanbox                DataBox              Aborted             04-12-2018 16:07:41   westus               TestRg2
cleanbox-Clone          DataBox              Cancelled           25-04-2019 11:31:36   westus               TestRg2
.
.
.
```

<span data-ttu-id="22223-115">Get-AzDataBoxJob ohne Parameter ruft alle Databoxaufträge unter dem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="22223-115">Get-AzDataBoxJob without any parameter fetches all the databox jobs under the subscription</span></span>

### <span data-ttu-id="22223-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="22223-116">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1
.
.
.
```

<span data-ttu-id="22223-117">Get-AzDataBoxJob mit dem Parameter "ResourceGroupName" ruft alle Databoxaufträge unter der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="22223-117">Get-AzDataBoxJob with ResourceGroupName parameter fetches all the databox jobs under the specified resource group</span></span>

### <span data-ttu-id="22223-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="22223-118">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1 -Name testtip2

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="22223-119">Get-AzDataBoxJob mit "ResourceGroupName" und "Name" angegeben werden, wird dieser spezifische Datenfeldauftrag abgerufen.</span><span class="sxs-lookup"><span data-stu-id="22223-119">Get-AzDataBoxJob with ResourceGroupName and Name specified will fetch that specific databox job</span></span>

### <span data-ttu-id="22223-120">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="22223-120">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/testtip2"

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="22223-121">Get-AzDataBoxJob angegebenen Wert "ResourceId" den jeweiligen Datenfeldauftrag abruft</span><span class="sxs-lookup"><span data-stu-id="22223-121">Get-AzDataBoxJob with ResourceId specified will fetch that specific databox job</span></span>

## <span data-ttu-id="22223-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22223-122">PARAMETERS</span></span>

### <span data-ttu-id="22223-123">-Abgebrochen</span><span class="sxs-lookup"><span data-stu-id="22223-123">-Aborted</span></span>
<span data-ttu-id="22223-124">Parameter zum Abrufen abgebrochener Aufträge wechseln</span><span class="sxs-lookup"><span data-stu-id="22223-124">Switch Parameter to fetch Aborted jobs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22223-125">-Storniert</span><span class="sxs-lookup"><span data-stu-id="22223-125">-Cancelled</span></span>
<span data-ttu-id="22223-126">Parameter zum Abrufen abgebrochener Aufträge wechseln</span><span class="sxs-lookup"><span data-stu-id="22223-126">Switch Parameter to fetch Cancelled jobs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22223-127">-Completed</span><span class="sxs-lookup"><span data-stu-id="22223-127">-Completed</span></span>
<span data-ttu-id="22223-128">Parameter zum Abrufen abgeschlossener Aufträge wechseln</span><span class="sxs-lookup"><span data-stu-id="22223-128">Switch Parameter to fetch Completed jobs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22223-129">-CompletedWithError</span><span class="sxs-lookup"><span data-stu-id="22223-129">-CompletedWithError</span></span>
<span data-ttu-id="22223-130">Parameter zum Abrufen von Aufträgen wechseln, die mit Fehlern abgeschlossen wurden</span><span class="sxs-lookup"><span data-stu-id="22223-130">Switch Parameter to fetch jobs completed with errors</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22223-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22223-131">-DefaultProfile</span></span>
<span data-ttu-id="22223-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="22223-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22223-133">-Name</span><span class="sxs-lookup"><span data-stu-id="22223-133">-Name</span></span>
<span data-ttu-id="22223-134">Name des Datenfeldauftrags</span><span class="sxs-lookup"><span data-stu-id="22223-134">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22223-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22223-135">-ResourceGroupName</span></span>
<span data-ttu-id="22223-136">Name der Databox-Auftragsressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="22223-136">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22223-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22223-137">-ResourceId</span></span>
<span data-ttu-id="22223-138">Databox Job Resource Id</span><span class="sxs-lookup"><span data-stu-id="22223-138">Databox Job Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22223-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22223-139">CommonParameters</span></span>
<span data-ttu-id="22223-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22223-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22223-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22223-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22223-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="22223-142">INPUTS</span></span>

### <span data-ttu-id="22223-143">System.String</span><span class="sxs-lookup"><span data-stu-id="22223-143">System.String</span></span>

## <span data-ttu-id="22223-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="22223-144">OUTPUTS</span></span>

### <span data-ttu-id="22223-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="22223-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="22223-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="22223-146">NOTES</span></span>

## <span data-ttu-id="22223-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="22223-147">RELATED LINKS</span></span>
