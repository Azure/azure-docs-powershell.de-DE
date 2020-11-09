---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: f897c2adfe4154aeff5bd370437ea8b23e4efd36
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298797"
---
# <span data-ttu-id="921ed-101">Invoke-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="921ed-101">Invoke-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="921ed-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="921ed-102">SYNOPSIS</span></span>
<span data-ttu-id="921ed-103">Ruft bestimmte Aktionen auf einem Speichercontainer auf</span><span class="sxs-lookup"><span data-stu-id="921ed-103">Invokes specific actions on a storage container</span></span>

## <span data-ttu-id="921ed-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="921ed-104">SYNTAX</span></span>

### <span data-ttu-id="921ed-105">InvokeByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="921ed-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="921ed-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="921ed-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="921ed-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="921ed-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-RefreshData] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeStorageContainer> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="921ed-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="921ed-108">DESCRIPTION</span></span>
<span data-ttu-id="921ed-109">Das Cmdlet **Invoke-AzDataBoxEdgeStorageContainer** ruft Aktionen auf, um die Daten auf einem Speichercontainer auf einem Daten Feld-Edge-Gerät zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="921ed-109">The **Invoke-AzDataBoxEdgeStorageContainer** cmdlet invokes actions to refresh the data on a storage container on a Data Box Edge device.</span></span> 

## <span data-ttu-id="921ed-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="921ed-110">EXAMPLES</span></span>

### <span data-ttu-id="921ed-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="921ed-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 -PassThru
PS C:\> true
```

### <span data-ttu-id="921ed-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="921ed-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 | Invoke-AzDataBoxEdgeStorageContainer
```

## <span data-ttu-id="921ed-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="921ed-113">PARAMETERS</span></span>

### <span data-ttu-id="921ed-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="921ed-114">-AsJob</span></span>
<span data-ttu-id="921ed-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="921ed-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="921ed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="921ed-116">-DefaultProfile</span></span>
<span data-ttu-id="921ed-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="921ed-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="921ed-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="921ed-118">-DeviceName</span></span>
<span data-ttu-id="921ed-119">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="921ed-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="921ed-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="921ed-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="921ed-121">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="921ed-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="921ed-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="921ed-122">-InputObject</span></span>
<span data-ttu-id="921ed-123">Bereitstellen eines vorhandenen EdgeStorageAccount-Objekts</span><span class="sxs-lookup"><span data-stu-id="921ed-123">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="921ed-124">-Name</span><span class="sxs-lookup"><span data-stu-id="921ed-124">-Name</span></span>
<span data-ttu-id="921ed-125">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="921ed-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="921ed-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="921ed-126">-PassThru</span></span>
<span data-ttu-id="921ed-127">gibt "true" zurück, wenn erfolgreich</span><span class="sxs-lookup"><span data-stu-id="921ed-127">returns true if successful</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="921ed-128">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="921ed-128">-RefreshData</span></span>
<span data-ttu-id="921ed-129">Aktualisieren von Container Metadaten mit den Daten aus der Cloud</span><span class="sxs-lookup"><span data-stu-id="921ed-129">Refresh Container Metadata with the data from the cloud</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="921ed-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="921ed-130">-ResourceGroupName</span></span>
<span data-ttu-id="921ed-131">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="921ed-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="921ed-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="921ed-132">-ResourceId</span></span>
<span data-ttu-id="921ed-133">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="921ed-133">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="921ed-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="921ed-134">-Confirm</span></span>
<span data-ttu-id="921ed-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="921ed-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="921ed-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="921ed-136">-WhatIf</span></span>
<span data-ttu-id="921ed-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="921ed-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="921ed-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="921ed-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="921ed-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="921ed-139">CommonParameters</span></span>
<span data-ttu-id="921ed-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="921ed-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="921ed-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="921ed-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="921ed-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="921ed-142">INPUTS</span></span>

### <span data-ttu-id="921ed-143">System. String</span><span class="sxs-lookup"><span data-stu-id="921ed-143">System.String</span></span>

### <span data-ttu-id="921ed-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="921ed-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="921ed-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="921ed-145">OUTPUTS</span></span>

### <span data-ttu-id="921ed-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="921ed-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="921ed-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="921ed-147">NOTES</span></span>

## <span data-ttu-id="921ed-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="921ed-148">RELATED LINKS</span></span>
