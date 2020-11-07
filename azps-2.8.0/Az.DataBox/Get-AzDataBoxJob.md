---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/get-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
ms.openlocfilehash: 9bb1fdd02b77a530f6bf4d8ea47a041f22e38b48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651804"
---
# <span data-ttu-id="21ea5-101">Get-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="21ea5-101">Get-AzDataBoxJob</span></span>

## <span data-ttu-id="21ea5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="21ea5-102">SYNOPSIS</span></span>
<span data-ttu-id="21ea5-103">Ruft Informationen zu DataBox-Aufträgen ab.</span><span class="sxs-lookup"><span data-stu-id="21ea5-103">Gets information about Databox Jobs</span></span>

## <span data-ttu-id="21ea5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="21ea5-104">SYNTAX</span></span>

### <span data-ttu-id="21ea5-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="21ea5-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxJob [-ResourceGroupName <String>] [-Completed] [-CompletedWithError] [-Cancelled] [-Aborted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21ea5-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="21ea5-106">GetByNameParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="21ea5-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="21ea5-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21ea5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="21ea5-108">DESCRIPTION</span></span>
<span data-ttu-id="21ea5-109">Das Cmdlet " **Get-AzDataBoxJobs** " Ruft Informationen zu DataBox-Aufträgen in einem Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="21ea5-109">The **Get-AzDataBoxJobs** cmdlet gets information about databox jobs in an Azure subscription.</span></span>
<span data-ttu-id="21ea5-110">Wenn Sie die Ressourcengruppe angeben, ruft dieses Cmdlet alle DataBox-Aufträge unter dieser Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="21ea5-110">If you specify the Resource Group, this cmdlet gets all the databox jobs under that resource group.</span></span> <span data-ttu-id="21ea5-111">Wenn Sie den Namen des Auftrags zusammen mit dem Namen der Ressourcengruppe angeben, ruft dieses Cmdlet Informationen zu diesem bestimmten DataBox-Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="21ea5-111">If you specify the Name of the job along with the resource group name, this cmdlet gets information about that specific databox job.</span></span>
<span data-ttu-id="21ea5-112">Wenn Sie nichts anderes als die Abonnement-ID angeben, ruft dieses Cmdlet Informationen zu allen DataBox-Aufträgen unter diesem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="21ea5-112">If you do not specify anything other than subscription id, this cmdlet gets information about all of the databox jobs under that subscription.</span></span>

## <span data-ttu-id="21ea5-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="21ea5-113">EXAMPLES</span></span>

### <span data-ttu-id="21ea5-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="21ea5-114">Example 1</span></span>
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

<span data-ttu-id="21ea5-115">Get-AzDataBoxJob ohne Parameter ruft alle DataBox-Aufträge unter dem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="21ea5-115">Get-AzDataBoxJob without any parameter fetches all the databox jobs under the subscription</span></span>

### <span data-ttu-id="21ea5-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="21ea5-116">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1
.
.
.
```

<span data-ttu-id="21ea5-117">Get-AzDataBoxJob mit dem ResourceGroupName-Parameter ruft alle DataBox-Aufträge unter der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="21ea5-117">Get-AzDataBoxJob with ResourceGroupName parameter fetches all the databox jobs under the specified resource group</span></span>

### <span data-ttu-id="21ea5-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="21ea5-118">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1 -Name testtip2

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="21ea5-119">Get-AzDataBoxJob mit ResourceGroupName, und der angegebene Name ruft diesen speziellen DataBox-Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="21ea5-119">Get-AzDataBoxJob with ResourceGroupName and Name specified will fetch that specific databox job</span></span>

### <span data-ttu-id="21ea5-120">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="21ea5-120">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/testtip2"

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="21ea5-121">Mit der angegebenen Get-AzDataBoxJob wird der jeweilige DataBox-Auftrag abgerufen.</span><span class="sxs-lookup"><span data-stu-id="21ea5-121">Get-AzDataBoxJob with ResourceId specified will fetch that specific databox job</span></span>

## <span data-ttu-id="21ea5-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="21ea5-122">PARAMETERS</span></span>

### <span data-ttu-id="21ea5-123">-Abgebrochen</span><span class="sxs-lookup"><span data-stu-id="21ea5-123">-Aborted</span></span>
<span data-ttu-id="21ea5-124">Parameter zum Abrufen von abgebrochenen Aufträgen wechseln</span><span class="sxs-lookup"><span data-stu-id="21ea5-124">Switch Parameter to fetch Aborted jobs</span></span>

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

### <span data-ttu-id="21ea5-125">-Storniert</span><span class="sxs-lookup"><span data-stu-id="21ea5-125">-Cancelled</span></span>
<span data-ttu-id="21ea5-126">Parameter zum Abrufen stornierter Aufträge wechseln</span><span class="sxs-lookup"><span data-stu-id="21ea5-126">Switch Parameter to fetch Cancelled jobs</span></span>

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

### <span data-ttu-id="21ea5-127">-Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="21ea5-127">-Completed</span></span>
<span data-ttu-id="21ea5-128">Parameter wechseln, um abgeschlossene Aufträge abzurufen</span><span class="sxs-lookup"><span data-stu-id="21ea5-128">Switch Parameter to fetch Completed jobs</span></span>

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

### <span data-ttu-id="21ea5-129">-CompletedWithError</span><span class="sxs-lookup"><span data-stu-id="21ea5-129">-CompletedWithError</span></span>
<span data-ttu-id="21ea5-130">Parameter wechseln zum Abrufen von Aufträgen, die mit Fehlern abgeschlossen wurden</span><span class="sxs-lookup"><span data-stu-id="21ea5-130">Switch Parameter to fetch jobs completed with errors</span></span>

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

### <span data-ttu-id="21ea5-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21ea5-131">-DefaultProfile</span></span>
<span data-ttu-id="21ea5-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="21ea5-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21ea5-133">-Name</span><span class="sxs-lookup"><span data-stu-id="21ea5-133">-Name</span></span>
<span data-ttu-id="21ea5-134">DataBox-Auftrags Name</span><span class="sxs-lookup"><span data-stu-id="21ea5-134">Databox Job Name</span></span>

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

### <span data-ttu-id="21ea5-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21ea5-135">-ResourceGroupName</span></span>
<span data-ttu-id="21ea5-136">Datenbox-Auftrags Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="21ea5-136">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="21ea5-137">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="21ea5-137">-ResourceId</span></span>
<span data-ttu-id="21ea5-138">DataBox-Auftrags Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="21ea5-138">Databox Job Resource Id</span></span>

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

### <span data-ttu-id="21ea5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21ea5-139">CommonParameters</span></span>
<span data-ttu-id="21ea5-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21ea5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21ea5-141">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21ea5-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21ea5-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="21ea5-142">INPUTS</span></span>

### <span data-ttu-id="21ea5-143">System. String</span><span class="sxs-lookup"><span data-stu-id="21ea5-143">System.String</span></span>

## <span data-ttu-id="21ea5-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="21ea5-144">OUTPUTS</span></span>

### <span data-ttu-id="21ea5-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="21ea5-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="21ea5-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="21ea5-146">NOTES</span></span>

## <span data-ttu-id="21ea5-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="21ea5-147">RELATED LINKS</span></span>
